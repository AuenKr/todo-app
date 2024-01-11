
# Todo-app backend

### Setup
1. rename **.keys.js** to **keys.js**
2. enter your mongodb clustor url in **url** variable

#### Note
/todo : name of databases

## end-points

#### Get all items

```http
  GET /todos
```
#### add todo

```http
  POST /todo

  body : {
    title: $String,
    description: $String,
  }
```

#### mark as completed

```http
  PUT /completed

  body : {
    id: $createdTodoID
  }
```