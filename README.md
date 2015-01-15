# REST API Starter

A RESTful API template built with Go's standard library.

## Features

- Full CRUD operations for User resource
- JSON request/response handling
- RESTful routing
- In-memory storage
- Error handling

## Usage

```bash
go run main.go
```

## API Endpoints

### Users

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /users   | Get all users |
| POST   | /users   | Create new user |
| GET    | /users/{id} | Get user by ID |
| PUT    | /users/{id} | Update user |
| DELETE | /users/{id} | Delete user |

## Examples

### Get all users
```bash
curl http://localhost:8080/users
```

### Create a user
```bash
curl -X POST http://localhost:8080/users \
  -H "Content-Type: application/json" \
  -d '{"name":"Bob Wilson","email":"bob@example.com"}'
```

### Get a specific user
```bash
curl http://localhost:8080/users/1
```

### Update a user
```bash
curl -X PUT http://localhost:8080/users/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"John Updated","email":"john.new@example.com"}'
```

### Delete a user
```bash
curl -X DELETE http://localhost:8080/users/1
```