## Информация о конкретном пользователе
> GET /v1/users/{user-id}

## Запрос

Параметр | Обязательный | Описание
-|-|-

## Ответ

### 200 OK
> Информация о пользователе с указанным `{user-id}`

Поле | Тип | Описание
-|-|-
id | NUMBER | Уникальный ID пользователя
username | STRING | Псевдоним
surname | STRING | Фамилия
name | STRING | Имя

```json
{
    id:       NUMBER,
    username: STRING,
    surname:  STRING,
    name:     STRING
}
```
> NOTE: Смотри описание модели `User`

### 403 Forbidden
> Доступ запрещён. Указан недействительный токен

Поле | Тип | Описание
-|-|-
error | STRING | Сообщение об ошибке

```json
{
    'error': STRING
}
```

### 404 Not Found
> Не найдено записей, удовлетворяющих запросу (некоректный `{user-id}`)

Поле | Тип | Описание
-|-|-
error | STRING | Сообщение об ошибке

```json
{
    'error': STRING
}