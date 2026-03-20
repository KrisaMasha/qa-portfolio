# Test Run: RUN-003

## 📋 Общая информация
| | |
|---|---|
| **Session ID** | RUN-003 |
| **Date** | 11.03.2026 |
| **Session Name** | Функциональное: поисковая строка |
| **Tester** | Мария Самотканова |
| **Project** | [CenterFish.ru](https://centerfish.ru) |

---

## 📊 Результаты

| Total | Pass | Fail | Blocked | Pass Rate |
|-------|------|------|---------|-----------|
| 10 | 6 | 4 | 0 | 60% |

---

## 📝 Детальные результаты

### ✅ Passed (6)

| Case ID | Title | Result | Comment |
|---------|-------|--------|---------|
| [TC-001](../Test-Cases/search-tests.md#tc-001) | Поиск "катушка" | ✅ Pass | Результаты найдены корректно |
| [TC-003](../Test-Cases/search-tests.md#tc-003) | Поиск "удоч" | ✅ Pass | Находит "удочка" и производные |
| [TC-004](../Test-Cases/search-tests.md#tc-004) | Поиск "инстр" | ✅ Pass | Находит "инструменты" и производные |
| [TC-007](../Test-Cases/search-tests.md#tc-007) | Несуществующее "клуб" | ✅ Pass | Сообщение "Не найдено" |
| [TC-008](../Test-Cases/search-tests.md#tc-008) | Несуществующее "черешня" | ✅ Pass | Сообщение "Не найдено" |

### ❌ Failed (4)

| Case ID | Title | Result | Bug ID |
|---------|-------|--------|--------|
| [TC-002](../Test-Cases/search-tests.md#tc-002) | Поиск "чехлы" | ❌ Fail | [BR-004](../Bug-Reports/BR-004-search-no-exact-match.md) |
| [TC-005](../Test-Cases/search-tests.md#tc-005) | Опечатка "лезки" | ❌ Fail | [BR-005](../Bug-Reports/BR-005-search-no-typo-handling.md) |
| [TC-006](../Test-Cases/search-tests.md#tc-006) | Опечатка "прианки" | ❌ Fail | [BR-005](../Bug-Reports/BR-005-search-no-typo-handling.md) |
| [TC-009](../Test-Cases/search-tests.md#tc-009) | Пустой запрос | ❌ Fail | [BR-006](../Bug-Reports/BR-006-empty-search-issue.md) |
| [TC-010](../Test-Cases/search-tests.md#tc-010) | Запрос с пробелом | ❌ Fail | [BR-006](../Bug-Reports/BR-006-empty-search-issue.md) |

---

## 🐛 Найденные баги

1. **[BR-004](../Bug-Reports/BR-004-search-no-exact-match.md)** — Поиск не находит товары по точному названию "чехлы"
2. **[BR-005](../Bug-Reports/BR-005-search-no-typo-handling.md)** — Поиск не обрабатывает опечатки
3. **[BR-006](../Bug-Reports/BR-006-empty-search-issue.md)** — Пустой запрос и запрос с пробелом некорректно обрабатываются
