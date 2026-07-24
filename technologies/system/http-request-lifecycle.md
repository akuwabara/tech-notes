# HTTP Request Lifecycle

## Overview

A typical HTTP request flows through the application in the following order.

### Request

```text
Browser
    ▼
Frontend
    ▼ HTTP Request
Router
    ▼
Use Case
    ▼
Repository
    ▼
Database
```

### Response

```text
Database
    ▼
Repository
    ▼
Use Case
    ▼
Router
    ▼ HTTP Response
Frontend
    ▼
Browser
```

---

## Layer Responsibilities

### Browser

The browser is where users interact with the application.

Typical responsibilities include:

- Rendering the application
- Receiving user input
- Displaying updated content

---

### Frontend

The frontend handles user interactions and communicates with the backend.

Typical responsibilities include:

- Rendering the user interface
- Managing application state
- Validating user input
- Sending HTTP requests
- Updating the user interface based on API responses

---

### Router

The router maps incoming requests to the appropriate endpoint and delegates processing to the corresponding use case.

Example:

```http
GET /users/123
```

maps to

```python
@router.get("/users/{user_id}")
```

The router should contain little or no business logic.

---

### Use Case

The use case contains the application's business logic.

Typical responsibilities include:

- Applying business rules
- Coordinating repositories
- Calling external services
- Handling application workflows

Business logic should be implemented here rather than in the router or repository.

---

### Repository

The repository is responsible for accessing persistent data.

Typical responsibilities include:

- Creating records
- Reading records
- Updating records
- Deleting records

Repositories should focus on data access and should not contain business logic.

---

### Database

The database stores application data permanently.

Examples include:

- PostgreSQL
- MySQL
- SQLite

---

## Example

```text
User clicks "Save"
    ▼
Frontend
    ▼ POST /users
Router
    ▼
Use Case
    ▼
Repository
    ▼
Database
    ▼
Repository
    ▼
Use Case
    ▼
Router
    ▼ HTTP Response (201 Created)
Frontend
    ▼
Browser
```

---

## Notes

- Keep each layer focused on a single responsibility.
- Do not implement business logic in the router.
- Do not implement business logic in the repository.
- Use the use case layer to coordinate business workflows.
- Separating responsibilities improves maintainability, readability, and testability.