# BR-003: Поле поиска недоступно при прокрутке страницы

**Project:** CenterFish.ru  
**Related Test Case:** [TC-020](../Test-Cases/header-tests.md#tc-020)  
**Session ID:** [RUN-001](../Test-Runs/RUN-001-header-analysis.md)  
**Severity:** Low  
**Priority:** Medium  
**Environment:** Chrome 120.0, Windows 10  
**Date Reported:** 11.03.2026  
**Status:** Open

---

## 📝 Описание
Поле поиска НЕ доступно для ввода при прокрутке страницы вниз, хотя должно оставаться доступным.

## Preconditions
- Открыта главная страница centerfish.ru

## 🔄 Steps to Reproduce
1. Начать прокрутку страницы вниз
2. Попытаться ввести текст в поле поиска

## ✅ Expected Result
Поле поиска остаётся доступным для ввода

## ❌ Actual Result
Поле поиска НЕ доступно при прокрутке

## 📎 Attachments
- Скриншот: https://skrinshoter.ru/saUwzzag8db

## 💡 Impact
Пользователи не могут воспользоваться поиском после прокрутки страницы, что ухудшает навигацию по сайту.

## 🔧 Suggested Fix
Сделать поле поиска фиксированным или доступным в фиксированной шапке при прокрутке.
