## Информация о своём аккаунте
> GET /v1/users/me

То же, что и `GET /v1/users/{userId}`, при этом `{userId}` - ID текущего пользователя


---


## Обновление информации о своём аккаунте
> PUT /v1/users/me

## Запрос

Параметр | Обязательный | Описание
-|-|-
username | Нет | Псевдоним
surname | Нет | Фамилия
name | Нет | Имя

> NOTE: Хотя бы один из параметров должен быть указан

## Ответ

### 200 OK
> Информация обновлена

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