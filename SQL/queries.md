# SQL Практика - QA Engineer

## 📋 Информация
| | |
|---|---|
| **Выполнил** | Мария Самотканова |
| **Дата** | Март 2026 |
| **Уровень** | Junior / Trainee |

---

## 🔹 SELECT - Выборка данных

```sql
-- 1. Получить всех пользователей
SELECT * FROM users;

-- 2. Получить имена и email активных пользователей
SELECT name, email FROM users WHERE status = 'active';

-- 3. Получить товары дороже 1000 рублей
SELECT name, price FROM products WHERE price > 1000 ORDER BY price DESC;

-- 4. Получить первые 10 заказов
SELECT * FROM orders LIMIT 10;


-- 5. Поиск товаров по названию (для centerfish.ru)
SELECT * FROM products WHERE name LIKE '%катушка%';
```
## 🔹 INSERT - Добавление данных

```sql
-- 1. Добавить нового пользователя
INSERT INTO users (name, email, status, city) VALUES ('Иван', 'ivan@example.com', 'active', 'Москва');

-- 2. Добавить товар в каталог
INSERT INTO products (name, price, category, description) VALUES ('Катушка', 1500, 'equipment', 'Рыболовная катушка');

-- 3. Добавить заказ
INSERT INTO orders (user_id, product_id, quantity, total, status) VALUES (1, 5, 2, 3000, 'new');

-- 4. Добавить категорию товаров
INSERT INTO categories (name, description) VALUES ('accessories', 'Аксессуары для рыбалки');

-- 5. Добавить несколько пользователей сразу
INSERT INTO users (name, email, status) VALUES 
    ('Пётр', 'petr@example.com', 'active'),
    ('Анна', 'anna@example.com', 'active'),
    ('Олег', 'oleg@example.com', 'inactive');
```

## 🔹 UPDATE - Обновление данных

```sql
-- 1. Обновить статус пользователя
UPDATE users SET status = 'inactive' WHERE id = 5;

-- 2. Изменить цену товара
UPDATE products SET price = 1200 WHERE name = 'Катушка';

-- 3. Обновить статус заказа
UPDATE orders SET status = 'shipped' WHERE id = 10;

-- 4. Обновить категорию товара
UPDATE products SET category = 'accessories' WHERE id = 3;

-- 5. Обновить несколько полей одновременно
UPDATE users SET status = 'active', city = 'Москва' WHERE id = 1;

-- 6. Обновить все товары в категории (скидка 10%)
UPDATE products SET price = price * 0.9 WHERE category = 'equipment';
```

## 🔹 DELETE - Удаление данных

```sql
-- 1. Удалить пользователя
DELETE FROM users WHERE id = 5;

-- 2. Удалить все отменённые заказы
DELETE FROM orders WHERE status = 'cancelled';

-- 3. Удалить товар из категории
DELETE FROM products WHERE category = 'discontinued';

-- 4. Удалить неактивных пользователей
DELETE FROM users WHERE status = 'inactive' AND created_at < '2025-01-01';

-- 5. Удалить заказ по ID
DELETE FROM orders WHERE id = 15;
```

## 🔹 JOIN - Объединение таблиц

```sql
-- 1. INNER JOIN - пользователи и их заказы
SELECT u.name, o.product, o.price FROM users u INNER JOIN orders o ON u.id = o.user_id;

-- 2. LEFT JOIN - все пользователи + их заказы (если есть)
SELECT u.name, o.product FROM users u LEFT JOIN orders o ON u.id = o.user_id;

-- 3. JOIN трёх таблиц (users + orders + products + categories)
SELECT u.name, p.name AS product, c.name AS category 
FROM users u 
INNER JOIN orders o ON u.id = o.user_id 
INNER JOIN products p ON o.product_id = p.id 
INNER JOIN categories c ON p.category_id = c.id;

-- 4. Для centerfish.ru - клиенты и их заказы товаров
SELECT u.name, u.email, p.name AS product, o.quantity, o.total 
FROM users u 
INNER JOIN orders o ON u.id = o.user_id 
INNER JOIN products p ON o.product_id = p.id 
WHERE u.status = 'active';

-- 5. RIGHT JOIN - все заказы + пользователи (если есть)
SELECT u.name, o.total FROM users u RIGHT JOIN orders o ON u.id = o.user_id;
```

## 🔹 Агрегатные функции

```sql
-- 1. COUNT - количество пользователей
SELECT COUNT(*) AS total_users FROM users;

-- 2. SUM - общая сумма всех заказов
SELECT SUM(total) AS total_amount FROM orders;

-- 3. AVG - средняя цена товара
SELECT AVG(price) AS average_price FROM products;

-- 4. MIN/MAX - минимальная и максимальная цена
SELECT MIN(price) AS min_price, MAX(price) AS max_price FROM products;

-- 5. GROUP BY - количество заказов по пользователю
SELECT u.name, COUNT(o.id) AS order_count 
FROM users u 
LEFT JOIN orders o ON u.id = o.user_id 
GROUP BY u.id, u.name;

-- 6. GROUP BY - сумма заказов по категории товара
SELECT c.name AS category, SUM(o.total) AS total_sales 
FROM orders o 
INNER JOIN products p ON o.product_id = p.id 
INNER JOIN categories c ON p.category_id = c.id 
GROUP BY c.id, c.name;

-- 7. COUNT с WHERE - количество активных пользователей
SELECT COUNT(*) AS active_users FROM users WHERE status = 'active';

-- 8. AVG с GROUP BY - средняя цена по категории
SELECT category, AVG(price) AS avg_price FROM products GROUP BY category;
```
