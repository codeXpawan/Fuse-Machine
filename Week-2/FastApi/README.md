# 📘 FastAPI Student Management API

This project is a **FastAPI-based RESTful API** that demonstrates how to build a student management system using various FastAPI features such as:

- Path, Query, Body parameters
- Request validation with Pydantic models
- CRUD operations
- Cookies and Headers
- OpenAPI/Swagger documentation
- Nested JSON
- Parameter aliases, deprecation, and metadata

---

## Getting Started

### Installation

Make sure you have FastAPI installed:

```bash
pip install fastapi 
```

### Run the API
To run the API, use the following command:

```bash
fastapi dev myapi.py
```
### API Endpoints Summary
#### GET /
Description: Welcome route

#### GET /get-student/{student_id}
Description: Get student by ID

#### GET /get-by-name
Description: Get student by name (via query)

Example:
```
/get-by-name?item-query=pawan
```

#### GET /get-multiple-query
Description: Get multiple students by name list

Example:
```
GET /get-multiple-query?names=pawan&names=ram
```

#### GET /get-data/{student_id}
Description: Get student using both path and query

Example:

```
GET /get-data/1?name=pawan
```

#### POST /create-student/{student_id}
Description: Create a new student

Example:
```
POST /create-student/2
Content-Type: application/json

{
  "name": "ram",
  "age": 22,
  "year": "year 13",
  "tags": ["math"]
}
```

#### PUT /update-student/{student_id}
Description: Update an existing student

Example:
```
PUT /update-student/2
Content-Type: application/json

{
  "name": "ram_updated"
}
```

#### DELETE /delete-student/{student_id}
Description: Delete a student

Example:
```
DELETE /delete-student/2
```

#### POST /index-weights/
Description: Send dictionary with int keys & float values

Example:
```
POST /index-weights/
Content-Type: application/json

{
  "1": 0.8,
  "2": 0.2
}
```

#### GET /cookie-student/
Description: Get value of ads_id from cookies

Example Header:
```
Cookie: ads_id=abc123
```
