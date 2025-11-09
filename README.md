

## 📖 Project Description
HRMS (Human Resource Management System) is a **Spring Boot-based web service** application designed for managing **job postings, applications, employer, and candidate information**.  

It follows **REST API architecture** and incorporates modern software development practices such as:  
- **DTOs (Data Transfer Objects)**  
- **Request-Response Pattern**  
- **Validation**  
- **Global Exception Handling**  

---

## ✨ Features
- **City Management**: Add and list cities.  
- **Job Position Management**: Add and list job positions.  
- **Employer Management**: Register and list employers.  
- **Candidate Management**: Register and list job seekers.  
- **Job Advertisement Management**: Add, list, and filter job ads.  
- **Job Application Management**: Allow candidates to apply for jobs.  
- **Validation**: Field validation using annotations like `@NotBlank`, `@Size`.  
- **Error Handling**: Global exception handling via `@ControllerAdvice`.  

---

## 🛠 Technologies Used
- **Java 17**  
- **Spring Boot**  
- **Spring Data JPA (Hibernate)**  
- **PostgreSQL**  
- **Lombok**  
- **Validation API (Jakarta Validation)**  
- **Jackson**  
- **Postman** (for API testing)  

---

## 🏗 Project Architecture
- **Entity**: Represents database tables.  
- **DTO**: Data Transfer Objects for API responses.  
- **Request**: Classes for incoming API requests.  
- **Service**: Business logic layer.  
- **Repository (DAO)**: Database access layer.  
- **Controller**: REST API endpoints.  
- **Core Utilities**: Standard response classes like `Result`, `DataResult`, `SuccessResult`, `ErrorResult`.  

**Result Structure:**  
- `Result`: Success/failure status + message.  
- `DataResult<T>`: Success/failure status + data.  
- `SuccessResult` / `ErrorResult`: Predefined classes for easy success/error responses.  

---

## 🔗 API Endpoints

| HTTP | Endpoint | Description |
|------|----------|-------------|
| POST | `/api/employers/register` | Register a new employer |
| GET  | `/api/employers/getAll` | Get all employers |
| POST | `/api/candidates/register` | Register a new candidate |
| GET  | `/api/candidates/getAll` | Get all candidates |
| POST | `/api/jobAdvertisements/add` | Add a new job advertisement |
| GET  | `/api/jobAdvertisements/getAll` | Get all job advertisements |
| POST | `/api/jobApplications/apply` | Apply for a job advertisement |

---

## 📝 Sample JSON Requests

**Employer Registration:**
```json
{
  "companyName": "Tech Solutions Ltd.",
  "companyWebPage": "https://techsolutions.com",
  "email": "contact@techsolutions.com",
  "phoneNumber": "+1-555-123-4567",
  "password": "password123",
  "confirmPassword": "password123"
}
