# Вход в аккаунт
> POST /v1/account/singin

## Запрос

Параметр | Обязательный | Описание
-|-|-
username | Да | Псевдоним
password | Да | Пароль

## Ответ

### 200 OK
> Выход успешно произведён

Поле | Тип | Описание
-|-|-
token | STRING | Уникальный идентификатор сессии
expires | NUMBER | Время действия токена

```json
{
    'token': STRING,
    'expires': TIMESTAMP
}
```

### 403 Forbidden
> Учётные данные не найдены

Поле | Тип | Описание
-|-|-
error | STRING | Сообщение об ошибке

```json
{
    'error': STRING
}
```