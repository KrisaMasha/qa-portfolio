# SQL Практика - QA Engineer

## 📋 Информация
| | |
|---|---|
| **Выполнил** | Мария Самотканова |
| **Дата** | Март 2026 |
| **Уровень** | Junior / Trainee |

---

## 🔹 SELECT - Выборка данных

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

-- ============================================
-- INSERT - Добавление данных
-- ============================================

-- 1. Добавить нового пользователя
INSERT INTO users (name, email, status) VALUES ('Иван', 'ivan@example.com', 'active');

-- 2. Добавить товар в каталог
INSERT INTO products (name, price, category) VALUES ('Катушка', 1500, 'equipment');

-- 3. Добавить заказ
INSERT INTO orders (user_id, product_id, quantity, total) VALUES (1, 5, 2, 3000);

-- ============================================
-- UPDATE - Обновление данных
-- ============================================

-- 1. Обновить статус пользователя
UPDATE users SET status = 'inactive' WHERE id = 5;

-- 2. Изменить цену товара
UPDATE products SET price = 1200 WHERE name = 'Катушка';

-- 3. Обновить статус заказа
UPDATE orders SET status = 'shipped' WHERE id = 10;

-- ============================================
-- DELETE - Удаление данных
-- ============================================

-- 1. Удалить пользователя
DELETE FROM users WHERE id = 5;

-- 2. Удалить все отменённые заказы
DELETE FROM orders WHERE status = 'cancelled';

-- 3. Удалить товар из категории
DELETE FROM products WHERE category = 'discontinued';

-- ============================================
-- JOIN - Объединение таблиц
-- ============================================

-- 1. INNER JOIN - пользователи и их заказы
SELECT u.name, o.product, o.price FROM users u INNER JOIN orders o ON u.id = o.user_id;

-- 2. LEFT JOIN - все пользователи + их заказы (если есть)
SELECT u.name, o.product FROM users u LEFT JOIN orders o ON u.id = o.user_id;

-- 3. JOIN трёх таблиц (users + orders + products)
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

-- ============================================
-- Агрегатные функции
-- ============================================

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
