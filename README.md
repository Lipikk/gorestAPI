# GoRESTAPI
бесплатный фиктивный сервис REST API, предназначенный для тестирования

## Оглавление

Для объекта COMMENTS:
1. Выполнить GET запрос для вывода всех комментариев;
2. Выполнить GET запрос для одного комментария;
3. Выполнить POST запрос для создания комментария;
4. Выполнить PUT|PATCH (на выбор) для изменения комментария;
5. Выполнить DELETE для удаления комментария;
6. Выполнить GET запрос для фильтрации комментария по определенному посту через Nested Resources; 
7. Выполнить POST запрос для создания комментария к определенному посту через Nested Resources;
   Для объекта POSTS:
8. Выполнить GET запрос для вывода всех постов;

## Описание проекта 
**https://gorest.co.in/** данный сайт представляет собой сервис для тестирования API. Для выполнения запросов необходим token, который можно получить автоматически после регистрации на сайте. В качестве тестирования взят объект **Comments** и **Posts**. 

### COMMENTS 
_____
#### GET/AllComments
Возвращает список всех комментариев к постам

**Response Body**:
```javascript
{
id: number
post_id:number
name: string
email: string
body: string
}
```

#### GET/OneComments
Возвращает по запросу указанный комментарий

**Response Body**:
```javascript
{
id: number
post_id:number
name: string
email: string
body: string
}
```

#### POST/CreateComments
Создает новой комментарий и Возвращает данные о комментарии

**Request Body**:

```javascript
{
post_id: number
name: string
email: string
body: string
post: number
}
```
**Response Body**:

```javascript
{
id: number
post_id: number
name: string
email: string
body: string
}
```

#### PUT/ChangeComments
Редактирует новый комментарий и Возвращает данные о комментарии

**Request Body**:

```javascript
{
post_id: number
name: string
email: string
body: string
post: number
}
```
**Response Body**:

```javascript
{
id: number
post_id: number
name: string
email: string
body: string
}
```

#### DELETE/DeleteComments
Создает новой комментарий и Возвращает данные о комментарии

**Response Body**:
возвращает статус код 204 No Content 


#### FilterCommentsByPost
Фильтрует комментарии по определенному посту через связанные ресурсы Nested Resources


#### CreateCommentsByPost
Создает комментарий к определенному посту через связанные ресурсы Nested Resources

**Request Body**:

```javascript
{
name: string
email: string
body: string
post: number
}
```
**Response Body**:

```javascript
{
id: number
post_id: number
name: string
email: string
body: string
}
```

### POSTS 
_____
#### GET/posts
Возвращает список постов
**Response Body**:

```javascript
{
id: number
user_id: number
title: string
body: string
}
```

