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
