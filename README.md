```bash
go run main.go
```

- **SIGNUP FUNCTION API CALL (POST REQUEST)**

http://localhost:8000/users/signup

```json
{
    "First_name": "Artem",
    "Last_name": "Popov",
    "Password": "12345678",
    "Email": "art.popov@gmail.com",
    "Phone": "87056570364",
    "User_type": "ADMIN"
}
```

Response:

```json
{
    "InsertedID": "65d73a9d7d5a7c77d0a924b7"
}
```

- **LOGIN FUNCTION API CALL (POST REQUEST)**

  http://localhost:8000/users/login

```json
{
    "Password": "12345678",
    "Email": "art.popov@gmail.com"
}
```

Response:

```json
{
    "ID": "65d73a9d7d5a7c77d0a924b7",
    "first_name": "Artem",
    "last_name": "Popov",
    "Password": "$2a$14$at1gG1uJG6rdAKiPzj5whORoFUt0F/MggURmr5rPybA53kTdJm0c2",
    "email": "art.popov@gmail.com",
    "avatar": null,
    "phone": "87056570364",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6ImFydC5wb3BvdkBnbWFpbC5jb20iLCJGaXJzdF9uYW1lIjoiQXJ0ZW0iLCJMYXN0X25hbWUiOiIiLCJVaWQiOiI2NWQ3M2E5ZDdkNWE3Yzc3ZDBhOTI0YjciLCJleHAiOjE3MDg2OTA0NjF9.OO-pPJ2DjNRwtUY4Aa8wS_BNuU4tiHYgR8yeBIHtyXE",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6IiIsIkZpcnN0X25hbWUiOiIiLCJMYXN0X25hbWUiOiIiLCJVaWQiOiIiLCJleHAiOjE3MDkyMDg4NjF9.ZnmDz-X3v4UR_ea7YHWSS9ZrFyREmL5u4f4JBQy7mZo",
    "created_at": "2024-02-22T12:14:21Z",
    "updated_at": "2024-02-22T12:14:21Z",
    "user_id": "65d73a9d7d5a7c77d0a924b7"
}
```

- **View all the Users in db GET REQUEST**

  http://localhost:8000/users

Response:

```json
{
    "total_count": 3,
    "user_items": [
        {
            "_id": "6530a490ce02c4c8c1893f86",
            "avatar": null,
            "created_at": "2023-10-19T03:37:52Z",
            "email": "a.popov@gmail.com",
            "first_name": "Artem",
            "last_name": "Popov",
            "password": "$2a$14$nAQSdXxuV4m7F.ZOf7380eLUBfsrjOVJLdwUlyLGMTdOlc4TnEihK",
            "phone": "87056570362",
            "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6IiIsIkZpcnN0X25hbWUiOiIiLCJMYXN0X25hbWUiOiIiLCJVaWQiOiIiLCJleHAiOjE2OTkxOTA2OTB9.ai39ef7j-yzhw_IHy55iYAzVfHr7TqzoeZkYLazeByU",
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6ImEucG9wb3ZAZ21haWwuY29tIiwiRmlyc3RfbmFtZSI6IkFydGVtIiwiTGFzdF9uYW1lIjoiIiwiVWlkIjoiNjUzMGE0OTBjZTAyYzRjOGMxODkzZjg2IiwiZXhwIjoxNjk4NjcyMjkwfQ.YFK3ifqT9jJK3WbS6EtXxIaBoIyzmQhbS_uCKQ25ue0",
            "updated_at": "2023-10-29T13:24:50Z",
            "user_id": "6530a490ce02c4c8c1893f86"
        },
        {
            "_id": "65bb126eb3914760af218495",
            "avatar": null,
            "created_at": "2024-02-01T03:39:26Z",
            "email": "artem.popov@gmail.com",
            "first_name": "Artem",
            "last_name": "Popov",
            "password": "$2a$14$H3lvp/LENAsyeRMutdtXAekvtbyTQOsCZxy7PfP3bV6kq7nOaUibC",
            "phone": "87056570363",
            "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6IiIsIkZpcnN0X25hbWUiOiIiLCJMYXN0X25hbWUiOiIiLCJVaWQiOiIiLCJleHAiOjE3MDczNjM1OTF9.fBIlr9v5bYhCi1JbDKwenJ8qL_P0advHu8ahj1cS5Ms",
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6ImFydGVtLnBvcG92QGdtYWlsLmNvbSIsIkZpcnN0X25hbWUiOiJBcnRlbSIsIkxhc3RfbmFtZSI6IiIsIlVpZCI6IjY1YmIxMjZlYjM5MTQ3NjBhZjIxODQ5NSIsImV4cCI6MTcwNjg0NTE5MX0.laClkvnAdzbQm9B0RrInZkhBCOPyL7D1GDt4k7eNzK4",
            "updated_at": "2024-02-01T03:39:51Z",
            "user_id": "65bb126eb3914760af218495"
        },
        {
            "_id": "65d73a9d7d5a7c77d0a924b7",
            "avatar": null,
            "created_at": "2024-02-22T12:14:21Z",
            "email": "art.popov@gmail.com",
            "first_name": "Artem",
            "last_name": "Popov",
            "password": "$2a$14$at1gG1uJG6rdAKiPzj5whORoFUt0F/MggURmr5rPybA53kTdJm0c2",
            "phone": "87056570364",
            "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6IiIsIkZpcnN0X25hbWUiOiIiLCJMYXN0X25hbWUiOiIiLCJVaWQiOiIiLCJleHAiOjE3MDkyMDkwNjV9.mZYPRit31E1blO4gjWmdF4Nvw-KQw3x8Qx309sobmnU",
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6ImFydC5wb3BvdkBnbWFpbC5jb20iLCJGaXJzdF9uYW1lIjoiQXJ0ZW0iLCJMYXN0X25hbWUiOiIiLCJVaWQiOiI2NWQ3M2E5ZDdkNWE3Yzc3ZDBhOTI0YjciLCJleHAiOjE3MDg2OTA2NjV9.ym_bdPbY1nUQc0ZmHmW6IF3aqM5CX0ASq30G6ab9-SI",
            "updated_at": "2024-02-22T12:17:45Z",
            "user_id": "65d73a9d7d5a7c77d0a924b7"
        }
    ]
}
```

- **View User by ID in db GET REQUEST**

  http://localhost:8000/users/6530a490ce02c4c8c1893f86

Response:

```json
{
    "ID": "6530a490ce02c4c8c1893f86",
    "first_name": "Artem",
    "last_name": "Popov",
    "Password": "$2a$14$nAQSdXxuV4m7F.ZOf7380eLUBfsrjOVJLdwUlyLGMTdOlc4TnEihK",
    "email": "a.popov@gmail.com",
    "avatar": null,
    "phone": "87056570362",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6ImEucG9wb3ZAZ21haWwuY29tIiwiRmlyc3RfbmFtZSI6IkFydGVtIiwiTGFzdF9uYW1lIjoiIiwiVWlkIjoiNjUzMGE0OTBjZTAyYzRjOGMxODkzZjg2IiwiZXhwIjoxNjk4NjcyMjkwfQ.YFK3ifqT9jJK3WbS6EtXxIaBoIyzmQhbS_uCKQ25ue0",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJFbWFpbCI6IiIsIkZpcnN0X25hbWUiOiIiLCJMYXN0X25hbWUiOiIiLCJVaWQiOiIiLCJleHAiOjE2OTkxOTA2OTB9.ai39ef7j-yzhw_IHy55iYAzVfHr7TqzoeZkYLazeByU",
    "created_at": "2023-10-19T03:37:52Z",
    "updated_at": "2023-10-29T13:24:50Z",
    "user_id": "6530a490ce02c4c8c1893f86"
}
```

- **View all the Menus in db GET REQUEST**

  http://localhost:8000/menus

Response:

```json
[
    {
        "_id": "6530a531ce02c4c8c1893f88",
        "category": "food",
        "created_at": "2023-10-19T03:40:33Z",
        "end_date": null,
        "menu_id": "6530a531ce02c4c8c1893f88",
        "name": "slider-menu",
        "start_date": null,
        "updated_at": "2023-10-19T03:40:33Z"
    }
]
```

- **View Menu by ID in db GET REQUEST**

  http://localhost:8000/menus/6530a531ce02c4c8c1893f88

Response:

```json
{
    "ID": "6530a531ce02c4c8c1893f88",
    "name": "slider-menu",
    "category": "food",
    "start_date": null,
    "end_date": null,
    "created_at": "2023-10-19T03:40:33Z",
    "updated_at": "2023-10-19T03:40:33Z",
    "food_id": "6530a531ce02c4c8c1893f88"
}
```

- **add Menu Function (POST REQUEST)**

  http://localhost:8000/menus

```json
{
    "Name": "vegan's menu",
    "Category": "food"
}
```

Response: 

```json
{
    "InsertedID": "65d7492b0de35f61a8ffc9d5"
}
```

- **update Menu Function (POST REQUEST)**

  http://localhost:8000/menus/65d7492b0de35f61a8ffc9d5

```json
{
    "Name": "tea menu",
    "Category": "drinks",
    "Start_date": "2024-02-22T19:28:05Z",
    "End_date": "2024-05-25T22:00:05Z"
}
```

Response: "menu updated successfully"


- **View all the Foods in db GET REQUEST**

  http://localhost:8000/foods

Response:

```json
{
    "food_items": [
        {
            "_id": "6530a5f7ce02c4c8c1893f8a",
            "created_at": "2023-10-19T03:43:51Z",
            "food_id": "6530a5f7ce02c4c8c1893f8a",
            "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
            "menu_id": "6530a531ce02c4c8c1893f88",
            "name": "veghan-slider",
            "price": 2500,
            "updated_at": "2023-10-19T03:43:51Z"
        }
    ],
    "total_count": 1
}
```

- **View Food by ID in db GET REQUEST**

  http://localhost:8000/foods/6530a5f7ce02c4c8c1893f8a

Response:

```json
{
    "ID": "6530a5f7ce02c4c8c1893f8a",
    "name": "veghan-slider",
    "price": 2500,
    "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
    "created_at": "2023-10-19T03:43:51Z",
    "updated_at": "2023-10-19T03:43:51Z",
    "food_id": "6530a5f7ce02c4c8c1893f8a",
    "menu_id": "6530a531ce02c4c8c1893f88"
}
```

- **add Food Function (POST REQUEST)**

  http://localhost:8000/foods

```json
{
    "Name": "Hinkaly",
    "Price": 10,
    "Food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
    "Menu_id": "6530a531ce02c4c8c1893f88"
}
```

Response: 

```json
{
    "InsertedID": "65d746afdf3baf635a35e2be"
}
```

- **update Food Function (POST REQUEST)**

  http://localhost:8000/foods/6530a5f7ce02c4c8c1893f8a

```json
{
    "Name": "Hachapuri",
    "Price": 15,
    "Food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
    "Menu_id": "6530a531ce02c4c8c1893f88"
}
```

Response: "food item updated succesfully"

- **View all the Tables in db GET REQUEST**

  http://localhost:8000/tables

Response:

```json
[
    {
        "_id": "6530a7afce02c4c8c1893f8c",
        "created_at": "2023-10-19T03:51:11Z",
        "number_of_guests": 4,
        "table_id": "6530a7afce02c4c8c1893f8c",
        "table_number": 11,
        "updated_at": "2023-10-19T03:51:11Z"
    }
]
```

- **View Table by ID in db GET REQUEST**

  http://localhost:8000/tables/6530a7afce02c4c8c1893f8c

Response:

```json
{
    "ID": "6530a7afce02c4c8c1893f8c",
    "number_of_guests": 4,
    "table_number": 11,
    "created_at": "2023-10-19T03:51:11Z",
    "updated_at": "2023-10-19T03:51:11Z",
    "table_id": "6530a7afce02c4c8c1893f8c"
}
```

- **add Table Function (POST REQUEST)**

  http://localhost:8000/tables

```json
{
    "Number_of_guests": 2,
    "Table_number": 7
}
```

Response: 

```json
{
    "InsertedID": "65d74f8b100d014dd72c4c51"
}
```

- **update Table Function (POST REQUEST)**

  http://localhost:8000/tables/6530a7afce02c4c8c1893f8c

```json
{
    "Number_of_guests": 3,
    "Table_number": 5
}
```

Response: "table item updated succesfully"

- **View all the Orders in db GET REQUEST**

  http://localhost:8000/orders

Response:

```json
[
    {
        "_id": "6530a879ce02c4c8c1893f8e",
        "created_at": "2023-10-19T03:54:33Z",
        "order_date": "2023-10-19T09:53:00Z",
        "order_id": "6530a879ce02c4c8c1893f8e",
        "table_id": "6530a7afce02c4c8c1893f8c",
        "updated_at": "2023-10-19T03:54:33Z"
    },
    {
        "_id": "6530a906ce02c4c8c1893f90",
        "created_at": "2023-10-19T03:56:54Z",
        "order_date": "2023-10-19T03:56:54Z",
        "order_id": "6530a906ce02c4c8c1893f90",
        "table_id": null,
        "updated_at": "2023-10-19T03:56:54Z"
    },
    {
        "_id": "6530a96da5e7349779526c52",
        "created_at": "2023-10-19T03:58:37Z",
        "order_date": "2023-10-19T03:58:37Z",
        "order_id": "6530a96da5e7349779526c52",
        "table_id": null,
        "updated_at": "2023-10-19T03:58:37Z"
    }
]
```

- **View Order by ID in db GET REQUEST**

  http://localhost:8000/orders/6530a906ce02c4c8c1893f90

Response:

```json
{
    "ID": "6530a906ce02c4c8c1893f90",
    "order_date": "2023-10-19T03:56:54Z",
    "created_at": "2023-10-19T03:56:54Z",
    "updated_at": "2023-10-19T03:56:54Z",
    "order_id": "6530a906ce02c4c8c1893f90",
    "table_id": null
}
```

- **add Order Function (POST REQUEST)**

  http://localhost:8000/orders

```json
{
    "Order_date": "2024-02-22T09:53:00.000Z",
    "Table_id": "65d74f8b100d014dd72c4c51"
}
```

Response: 

```json
{
    "InsertedID": "65d75915a3f58da59e2a87ca"
}
```

- **update Order Function (POST REQUEST)**

  http://localhost:8000/orders/6530a906ce02c4c8c1893f90

```json
{
    "Order_date": "2024-02-22T10:53:00.000Z",
    "Table_id": "65d74f8b100d014dd72c4c51"
}
```

Response: "order item updated succesfully"

- **View all the OrderITEMS in db GET REQUEST**

  http://localhost:8000/orderItems

Response:

```json
[
    {
        "_id": "65d75bff4f07e877e98a4151",
        "created_at": "2024-02-22T14:36:47Z",
        "food_id": "65d746afdf3baf635a35e2be",
        "order_id": "65d75bff4f07e877e98a414f",
        "order_item_id": "65d75bff4f07e877e98a4151",
        "quantity": "M",
        "unit_price": 100000,
        "updated_at": "2024-02-22T14:36:47Z"
    },
    {
        "_id": "65d75bff4f07e877e98a4152",
        "created_at": "2024-02-22T14:36:47Z",
        "food_id": "65d746afdf3baf635a35e2be",
        "order_id": "65d75bff4f07e877e98a414f",
        "order_item_id": "65d75bff4f07e877e98a4152",
        "quantity": "S",
        "unit_price": 75000,
        "updated_at": "2024-02-22T14:36:47Z"
    }
]
```

- **View OrderItem by ID in db GET REQUEST**

  http://localhost:8000/orderItems/65d75bff4f07e877e98a4151

Response:

```json
{
    "ID": "65d75bff4f07e877e98a4151",
    "quantity": "M",
    "unit_price": 100000,
    "created_at": "2024-02-22T14:36:47Z",
    "updated_at": "2024-02-22T14:36:47Z",
    "food_id": "65d746afdf3baf635a35e2be",
    "order_item_id": "65d75bff4f07e877e98a4151",
    "order_id": "65d75bff4f07e877e98a414f"
}
```

- **View OrderItems by ORDER in db GET REQUEST**

  http://localhost:8000/orderItems-order/65d75bff4f07e877e98a414f

Response:

```json
[
    {
        "_id": {
            "order_id": "65d75bff4f07e877e98a414f"
        },
        "order_items": [
            {
                "_id": "65d75bff4f07e877e98a4151",
                "created_at": "2024-02-22T14:36:47Z",
                "food": {
                    "_id": "65d746afdf3baf635a35e2be",
                    "created_at": "2024-02-22T13:05:51Z",
                    "food_id": "65d746afdf3baf635a35e2be",
                    "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
                    "menu_id": "6530a531ce02c4c8c1893f88",
                    "name": "Hinkaly",
                    "price": 1000,
                    "updated_at": "2024-02-22T13:05:51Z"
                },
                "food_id": "65d746afdf3baf635a35e2be",
                "order": {
                    "_id": "65d75bff4f07e877e98a414f",
                    "created_at": "2024-02-22T14:36:47Z",
                    "order_date": "2024-02-22T14:36:47Z",
                    "order_id": "65d75bff4f07e877e98a414f",
                    "table_id": "65d74f8b100d014dd72c4c51",
                    "updated_at": "2024-02-22T14:36:47Z"
                },
                "order_id": "65d75bff4f07e877e98a414f",
                "order_item_id": "65d75bff4f07e877e98a4151",
                "quantity": "M",
                "table": {
                    "_id": "65d74f8b100d014dd72c4c51",
                    "created_at": "2024-02-22T13:43:39Z",
                    "number_of_guests": 2,
                    "table_id": "65d74f8b100d014dd72c4c51",
                    "table_number": 7,
                    "updated_at": "2024-02-22T13:43:39Z"
                },
                "unit_price": 100000,
                "updated_at": "2024-02-22T14:36:47Z"
            },
            {
                "_id": "65d75bff4f07e877e98a4152",
                "created_at": "2024-02-22T14:36:47Z",
                "food": {
                    "_id": "65d746afdf3baf635a35e2be",
                    "created_at": "2024-02-22T13:05:51Z",
                    "food_id": "65d746afdf3baf635a35e2be",
                    "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
                    "menu_id": "6530a531ce02c4c8c1893f88",
                    "name": "Hinkaly",
                    "price": 1000,
                    "updated_at": "2024-02-22T13:05:51Z"
                },
                "food_id": "65d746afdf3baf635a35e2be",
                "order": {
                    "_id": "65d75bff4f07e877e98a414f",
                    "created_at": "2024-02-22T14:36:47Z",
                    "order_date": "2024-02-22T14:36:47Z",
                    "order_id": "65d75bff4f07e877e98a414f",
                    "table_id": "65d74f8b100d014dd72c4c51",
                    "updated_at": "2024-02-22T14:36:47Z"
                },
                "order_id": "65d75bff4f07e877e98a414f",
                "order_item_id": "65d75bff4f07e877e98a4152",
                "quantity": "S",
                "table": {
                    "_id": "65d74f8b100d014dd72c4c51",
                    "created_at": "2024-02-22T13:43:39Z",
                    "number_of_guests": 2,
                    "table_id": "65d74f8b100d014dd72c4c51",
                    "table_number": 7,
                    "updated_at": "2024-02-22T13:43:39Z"
                },
                "unit_price": 75000,
                "updated_at": "2024-02-22T14:36:47Z"
            }
        ],
        "payment_due": 175000,
        "total_count": 2
    }
]
```

- **add OrderItems Function (POST REQUEST)**

  http://localhost:8000/orderItems

```json
{
    "Table_id": "65d74f8b100d014dd72c4c51",
    "Order_items": 
    [
        {
            "Quantity": "M",
            "Unit_price": 1000,
            "Food_id": "65d746afdf3baf635a35e2be",
            "Order_id": "6530a906ce02c4c8c1893f90"
        },
        {
            "Quantity": "S",
            "Unit_price": 750,
            "Food_id": "65d746afdf3baf635a35e2be",
            "Order_id": "6530a906ce02c4c8c1893f90"
        }
    ]
}
```

Response: 

```json
{
    "InsertedIDs": [
        "65d75bff4f07e877e98a4151",
        "65d75bff4f07e877e98a4152"
    ]
}
```

- **update OrderItem Function (POST REQUEST)**

  http://localhost:8000/orderItems/65d75bff4f07e877e98a4151

```json
{
    "Quantity": "L",
    "Unit_price": 1500,
    "Food_id": "65d746afdf3baf635a35e2be",
    "Order_id": "6530a906ce02c4c8c1893f90"
}
```

Response: "orderItem updated succesfully"

- **View all the Invoices in db GET REQUEST**

  http://localhost:8000/invoices

```json
[
    {
        "_id": "6530aaf5bf2fe5dde0bcad6e",
        "created_at": "2023-10-19T04:05:09Z",
        "invoice_id": "6530aaf5bf2fe5dde0bcad6e",
        "order_id": "6530a879ce02c4c8c1893f8e",
        "payment_due_date": "2023-10-20T04:05:09Z",
        "payment_method": "CARD",
        "payment_status": "PENDING",
        "updated_at": "2023-10-19T04:07:12Z"
    },
    {
        "_id": "65d766fc64083147e0db46ca",
        "created_at": "2024-02-22T15:23:40Z",
        "invoice_id": "65d766fc64083147e0db46ca",
        "order_id": "65d75bff4f07e877e98a414f",
        "payment_due_date": "2024-02-23T15:23:40Z",
        "payment_method": "CASH",
        "payment_status": "PENDING",
        "updated_at": "2024-02-22T15:23:40Z"
    }
]
```

- **View Invoice by ID in db GET REQUEST**

  http://localhost:8000/invoices/65d766fc64083147e0db46ca

Response:

```json
{
    "Invoice_id": "65d766fc64083147e0db46ca",
    "Payment_method": "CASH",
    "Order_id": "65d75bff4f07e877e98a414f",
    "Payment_status": "PENDING",
    "Payment_due": 76500,
    "Table_number": null,
    "Payment_due_date": "0001-01-01T00:00:00Z",
    "Order_details": [
        {
            "_id": "65d75bff4f07e877e98a4151",
            "created_at": "2024-02-22T14:36:47Z",
            "food": {
                "_id": "65d746afdf3baf635a35e2be",
                "created_at": "2024-02-22T13:05:51Z",
                "food_id": "65d746afdf3baf635a35e2be",
                "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
                "menu_id": "6530a531ce02c4c8c1893f88",
                "name": "Hinkaly",
                "price": 1000,
                "updated_at": "2024-02-22T13:05:51Z"
            },
            "food_id": "65d746afdf3baf635a35e2be",
            "order": {
                "_id": "65d75bff4f07e877e98a414f",
                "created_at": "2024-02-22T14:36:47Z",
                "order_date": "2024-02-22T14:36:47Z",
                "order_id": "65d75bff4f07e877e98a414f",
                "table_id": "65d74f8b100d014dd72c4c51",
                "updated_at": "2024-02-22T14:36:47Z"
            },
            "order_id": "65d75bff4f07e877e98a414f",
            "order_item_id": "65d75bff4f07e877e98a4151",
            "quantity": "L",
            "table": {
                "_id": "65d74f8b100d014dd72c4c51",
                "created_at": "2024-02-22T13:43:39Z",
                "number_of_guests": 2,
                "table_id": "65d74f8b100d014dd72c4c51",
                "table_number": 7,
                "updated_at": "2024-02-22T13:43:39Z"
            },
            "unit_price": 1500,
            "updated_at": "2024-02-22T15:18:38Z"
        },
        {
            "_id": "65d75bff4f07e877e98a4152",
            "created_at": "2024-02-22T14:36:47Z",
            "food": {
                "_id": "65d746afdf3baf635a35e2be",
                "created_at": "2024-02-22T13:05:51Z",
                "food_id": "65d746afdf3baf635a35e2be",
                "food_image": "https://unsplash.com/photos/zW8wA4QwS2M",
                "menu_id": "6530a531ce02c4c8c1893f88",
                "name": "Hinkaly",
                "price": 1000,
                "updated_at": "2024-02-22T13:05:51Z"
            },
            "food_id": "65d746afdf3baf635a35e2be",
            "order": {
                "_id": "65d75bff4f07e877e98a414f",
                "created_at": "2024-02-22T14:36:47Z",
                "order_date": "2024-02-22T14:36:47Z",
                "order_id": "65d75bff4f07e877e98a414f",
                "table_id": "65d74f8b100d014dd72c4c51",
                "updated_at": "2024-02-22T14:36:47Z"
            },
            "order_id": "65d75bff4f07e877e98a414f",
            "order_item_id": "65d75bff4f07e877e98a4152",
            "quantity": "S",
            "table": {
                "_id": "65d74f8b100d014dd72c4c51",
                "created_at": "2024-02-22T13:43:39Z",
                "number_of_guests": 2,
                "table_id": "65d74f8b100d014dd72c4c51",
                "table_number": 7,
                "updated_at": "2024-02-22T13:43:39Z"
            },
            "unit_price": 75000,
            "updated_at": "2024-02-22T15:13:17Z"
        }
    ]
}
```

- **add Invoice Function (POST REQUEST)**

  http://localhost:8000/invoices

```json
{
    "Payment_method":"CASH",
    "Payment_status":"PENDING",
    "Order_id":"65d75bff4f07e877e98a414f"
}
```

Response: 

```json
{
    "InsertedID": "65d766fc64083147e0db46ca"
}
```

- **update Order Function (POST REQUEST)**

  http://localhost:8000/invoices/65d766fc64083147e0db46ca

```json
{
    "Payment_method":"CARD",
    "Payment_status":"PAID",
    "Order_id":"6530a879ce02c4c8c1893f8e"
}
```

Response: "invoice updated succesfully"
