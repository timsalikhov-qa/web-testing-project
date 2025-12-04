# Примеры баг-репортов

## Bug-001: Кнопка Login неактивна в темной теме

**Status:** Open
**Priority:** High
**Severity:** Major
**Environment:** Safari 26.1, MacOs Tahoe 26.1 (25B78)

**Description:**
При переключении на темную тему и вводе корректных данных кнопка Login остается неактивной.

**Steps to Reproduce:**
1. Открыть https://opensource-demo.orangehrmlive.com/
2. Переключиться на темную тему (если доступно)
3. Ввести "Admin" в поле Username
4. Ввести "admin123" в поле Password
5. Наблюдать за состоянием кнопки входа

**Expected Result:**
Кнопка входа становится активной и кликабельной

**Actual Result:**
Кнопка входа остается отключенной

**Attachments:**
- Журналы консоли показывают: `button[disabled] CSS property override issue`
- Скриншот доступен во вложении в Jira

**Reproduction Rate:** 100% (5/5 attempts)

---

## Bug-002: Session timeout не показывает уведомление

**Status:** Fixed
**Priority:** Medium  
**Severity:** Minor
**Environment:** Safari 26.1, MacOs Tahoe 26.1 (25B78)

**Description:**
При истечении сессии пользователь автоматически разлогинивается без предупреждения.

**Steps:**
1. Войти с валидными учетными данными
2. Подождать 5 минут (session timeout)
3. Попробовать перейти на любую другую страницу

**Expected:**
Появится всплывающее окно "Your session will expire in 5 minutes"

**Actual:**
Пользователя разлогинивает из системы и перенаправляет на страницу входа
