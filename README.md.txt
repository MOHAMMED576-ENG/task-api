# Task Management REST API

A simple REST API for managing tasks built with Java, Spring Boot, MySQL, and Spring Data JPA.

## Features

- Create a new task
- Get all tasks
- Get a task by ID
- Update a task
- Delete a task
- Store tasks in MySQL
- Handle missing tasks with 404 Not Found

## Technologies

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- MySQL
- Maven
- Postman

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/tasks` | Get all tasks |
| GET | `/api/tasks/{id}` | Get task by ID |
| POST | `/api/tasks` | Create a task |
| PUT | `/api/tasks/{id}` | Update a task |
| DELETE | `/api/tasks/{id}` | Delete a task |

## Example Request

POST `/api/tasks`

```json
{
  "title": "Learn Spring Boot",
  "description": "Complete the REST API project",
  "status": "PENDING",
  "priority": "HIGH",
  "dueDate": "2026-09-30"
}
```

## Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE task_api;
```

The application uses an environment variable for the database password:

```properties
spring.datasource.password=${DB_PASSWORD}
```

Example for PowerShell:

```powershell
$env:DB_PASSWORD="YOUR_PASSWORD"
```

Then run the application:

```powershell
.\mvnw.cmd spring-boot:run
```

The API will be available at:

`http://localhost:8080/api/tasks`

## What I Learned

Through this project I practiced:

- Building REST APIs with Spring Boot
- HTTP methods and status codes
- CRUD operations
- Spring Data JPA
- Connecting Spring Boot to MySQL
- Working with JSON requests and responses
- Testing APIs with Postman
- Handling 404 Not Found responses
