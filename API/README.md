# Postman API Tests - CenterFish.ru

## 📋 Информация
| | |
|---|---|
| **Проект** | CenterFish.ru |
| **Тестировщик** | Мария Самотканова |
| **Дата** | Март 2026 |
| **Инструмент** | Postman |

---

## 🎯 Цель
Проверка доступности и корректности работы сайта через HTTP запросы.

---

## 📝 Тесты в коллекции

| № | Название | Метод | Ожидаемый результат |
|---|----------|-------|---------------------|
| 1 | Site Availability | GET | Status 200, время < 3000ms |
| 2 | Homepage Content | GET | Status 200, есть "Рыболовный центр" |
| 3 | Search Functionality | GET | Status 200, поиск работает |
| 4 | 404 Page Check | GET | Status 404 или 200 |
| 5 | HTTPS Redirect | GET | Redirect на HTTPS |

---

## 🔄 Как запустить тесты

### 1. Установите Postman
Скачайте с [postman.com](https://www.postman.com/)

### 2. Импортируйте коллекцию
1. Откройте Postman
2. Нажмите **Import** (левый верхний угол)
3. Выберите файл `centerfish.postman_collection.json`
4. Нажмите **Import**

### 3. Запустите тесты
1. Откройте коллекцию "CenterFish.ru Tests"
2. Нажмите **Run** (кнопка Play)
3. Выберите количество итераций
4. Нажмите **Run CenterFish.ru Tests**

---

## ✅ Результаты тестов

| Тест | Статус | Время ответа |
|------|--------|--------------|
| Site Availability | ✅ Pass | ~500ms |
| Homepage Content | ✅ Pass | ~600ms |
| Search Functionality | ✅ Pass | ~800ms |
| 404 Page Check | ✅ Pass | ~400ms |
| HTTPS Redirect | ✅ Pass | ~300ms |

---

## 🛠 Навыки продемонстрированы

- ✅ Создание HTTP запросов (GET)
- ✅ Проверка status codes (200, 301, 302, 404)
- ✅ Написание тестов на JavaScript для Postman
- ✅ Проверка производительности
- ✅ Работа с коллекциями
