
# Book Management System

An Go-based api for interacting with a mysql database through http requests. It is centred around managing book entries in the mySql database with fields "Name", "Author", and "Publication"

## Libraries Used

[gorm.io/driver/mysql](https://gorm.io) - For mapping JSON data and interacting with the mySql database

[gorilla/mux](https://github.com/gorilla/mux) - For making development easier/faster easier HTTP-routing and URL matching

## API Reference
Requests to the api and their arguments/required bodies
#### Get all books

```http
GET http://host:port/0.0.0.0:3000/book/
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `None` | `None` | **Required**. None |

#### Get book

```http
GET http://host:port/0.0.0.0:3000/book/{bookID}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `ID`      | `string` | **Required**. Id of item to fetch |

#### Create book
```http
POST http://host:port/0.0.0.0:3000/book/
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Book`      | `JSON` | **Required**. Fields: Name: string, Author: string, Publication: string  |

#### Update book
```http
PUT http://host:port/0.0.0.0:3000/book/{bookID} 
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Book`      | `JSON` | **Required**. Fields: Name: string, Author: string, Publication: string  |

#### Delete book
```http
DELETE http://host:port/0.0.0.0:3000/book/{bookID} 
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `ID`      | `string` | **Required**. Id of item to delete |
