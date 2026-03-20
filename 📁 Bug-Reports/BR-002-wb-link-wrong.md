# BR-002: Ссылка "наши товары на WB" ведёт на OZON вместо Wildberries

**Project:** CenterFish.ru  
**Related Test Case:** [TC-015](../Test-Cases/header-tests.md#tc-015)  
**Session ID:** [RUN-001](../Test-Runs/RUN-001-header-analysis.md)  
**Severity:** Medium  
**Priority:** High  
**Environment:** Chrome 120.0, Windows 10  
**Date Reported:** 11.03.2026  
**Status:** Open

---

## 📝 Описание
При клике на ссылку "наши товары на WB" (Wildberries) происходит переход на магазин компании на OZON вместо Wildberries.

## Preconditions
- Открыта главная страница centerfish.ru

## 🔄 Steps to Reproduce
1. Нажать на ссылку "наши товары на WB"
2. Проверить переход

## ✅ Expected Result
Открывается магазин компании на Wildberries

## ❌ Actual Result
Открывается магазин на OZON вместо Wildberries

## 💡 Impact
Пользователи не могут перейти на магазин Wildberries, что приводит к потере продаж на этой площадке.

## 🔧 Suggested Fix
Исправить URL ссылки "наши товары на WB" на корректную ссылку магазина Wildberries.
