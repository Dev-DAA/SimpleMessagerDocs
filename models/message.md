# Message (Сообщение)
Поле | Тип | Описание
-|-|-
id | NUMBER | Уникальный ID сообщения
roomId | NUMBER | ID чат-комнаты
userId | NUMBER | ID пользователя (автора)
type | NUMBER | Тип сообщения
content | STRING | Текст, ссылка или Base64-кодированное содержимое
timestamp | NUMBER | Метка времени
deleted | BOOL | Признак удалённого сообщения

```json
{
    id:        NUMBER,
    roomId:    NUMBER,
    userId:    NUMBER,
    type:      NUMBER,
    content:   STRING,
    timestamp: NUMBER,
    deleted:   BOOL
}
```

## Типы сообщений
Значение | Описание
-|-
1 | Простой текст
2 | Файл
3 | Изображение
4 | Видео
5 | Системное сообщение