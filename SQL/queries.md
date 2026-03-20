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

---

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
