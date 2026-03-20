# Test Run: RUN-001

## 📋 Общая информация
| | |
|---|---|
| **Session ID** | RUN-001 |
| **Date** | 11.03.2026 |
| **Session Name** | Детальный анализ шапки: centerfish.ru |
| **Tester** | Мария Самотканова |
| **Project** | [CenterFish.ru](https://centerfish.ru) |

---

## 📊 Результаты

| Total | Pass | Fail | Blocked | Pass Rate |
|-------|------|------|---------|-----------|
| 25 | 22 | 3 | 0 | 88% |

---

## 📝 Детальные результаты

### ✅ Passed (22)

| Case ID | Title | Result | Comment |
|---------|-------|--------|---------|
| [TC-001](../Test-Cases/header-tests.md#tc-001) | Ховер-эффект "Главная" | ✅ Pass | Цвет меняется с серого на голубой |
| [TC-002](../Test-Cases/header-tests.md#tc-002) | Ховер-эффект "Адреса и контакты" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-003](../Test-Cases/header-tests.md#tc-003) | Ховер-эффект "Заказ" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-004](../Test-Cases/header-tests.md#tc-004) | Ховер-эффект "Оплата" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-005](../Test-Cases/header-tests.md#tc-005) | Ховер-эффект "Получение" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-006](../Test-Cases/header-tests.md#tc-006) | Ховер-эффект "Гарантия и возврат" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-007](../Test-Cases/header-tests.md#tc-007) | Ховер-эффект "Прочее" | ✅ Pass | Цвет меняется, курсор pointer |
| [TC-008](../Test-Cases/header-tests.md#tc-008) | Клик по логотипу | ✅ Pass | Переход на главную страницу |
| [TC-009](../Test-Cases/header-tests.md#tc-009) | Клик по адресу | ✅ Pass | Открывается Яндекс Карта |
| [TC-011](../Test-Cases/header-tests.md#tc-011) | WhatsApp иконка | ✅ Pass | Открывается мессенджер |
| [TC-012](../Test-Cases/header-tests.md#tc-012) | VK иконка | ✅ Pass | Открывается группа VK |
| [TC-013](../Test-Cases/header-tests.md#tc-013) | YouTube иконка | ✅ Pass | Открывается канал |
| [TC-014](../Test-Cases/header-tests.md#tc-014) | Ссылка OZON | ✅ Pass | Открывается магазин на OZON |
| [TC-016](../Test-Cases/header-tests.md#tc-016) | Корзина | ✅ Pass | Открывается страница корзины |
| [TC-017](../Test-Cases/header-tests.md#tc-017) | Фиксация шапки | ✅ Pass | Шапка зафиксирована при прокрутке |
| [TC-018](../Test-Cases/header-tests.md#tc-018) | Скрытие/появление шапки | ✅ Pass | Скрывается вниз, появляется вверх |
| [TC-019](../Test-Cases/header-tests.md#tc-019) | Изменение высоты шапки | ✅ Pass | Высота уменьшается при скролле |
| [TC-021](../Test-Cases/header-tests.md#tc-021) | Размер шрифта | ✅ Pass | 14-16px, текст читается |
| [TC-022](../Test-Cases/header-tests.md#tc-022) | Контрастность | ✅ Pass | Соответствует стандартам |
| [TC-023](../Test-Cases/header-tests.md#tc-023) | Тип шрифта | ✅ Pass | Шрифт без засечек |
| [TC-024](../Test-Cases/header-tests.md#tc-024) | Межбуквенный интервал | ✅ Pass | Достаточный для чтения |
| [TC-025](../Test-Cases/header-tests.md#tc-025) | Цвет текста | ✅ Pass | Не сливается с фоном |

### ❌ Failed (3)

| Case ID | Title | Result | Bug ID |
|---------|-------|--------|--------|
| [TC-010](../Test-Cases/header-tests.md#tc-010) | Номер телефона не кликабелен | ❌ Fail | [BR-001](../Bug-Reports/BR-001-phone-not-clickable.md) |
| [TC-015](../Test-Cases/header-tests.md#tc-015) | Ссылка WB ведёт на OZON | ❌ Fail | [BR-002](../Bug-Reports/BR-002-wb-link-wrong.md) |
| [TC-020](../Test-Cases/header-tests.md#tc-020) | Поиск недоступен при прокрутке | ❌ Fail | [BR-003](../Bug-Reports/BR-003-search-not-available.md) |

---

## 🐛 Найденные баги

1. **[BR-001](../Bug-Reports/BR-001-phone-not-clickable.md)** — Номер телефона не кликабелен
2. **[BR-002](../Bug-Reports/BR-002-wb-link-wrong.md)** — Ссылка WB ведёт на OZON
3. **[BR-003](../Bug-Reports/BR-003-search-not-available.md)** — Поиск недоступен при прокрутке
