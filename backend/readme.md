# Todo-app backend

## Setup

1. rename **.keys.js** to **keys.js**
2. enter your mongodb clustor url in **url** variable

### Note

/todo : name of databases

##end-points

## 1. Get all items

```
  GET /todos
```

> output

```
{
    "todos": [
        {
            "_id": "randomId1",
            "title": "todo app",
            "description": "backend",
            "__v": 0,
            "completed": true
        },
        {
            "_id": "randomId1",
            "title": "lorem",
            "description": "Lorem ipsum dolor sit",
            "__v": 0,
            "completed": true
        }
    ]
}
```

## 2. add todo

```
  POST /todo

  body : {
    title: $String,
    description: $String,
  }
```

> output

1. success

```
{
    "msg": "Todo created"
}
```

2. Fail

```
{
    "msg": "Invalid inputs"
}
```

## 3. mark as completed

```
  PUT /completed

  body : {
    id: $createdTodoID
  }
```

> output

1. success

```
{
    "msg": "completed"
}
```

2. Fail

```
{
    "msg": "Invalid Id"
}
```

## 4. On server serror

-   status code : 500

```
{
  msg: "Server Error"
}
```
