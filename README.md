# 📒 Address Book API

## 📝 Overview
The Address Book API is a Spring Boot-based application designed to securely manage contacts with user authentication, JWT-based security, and CRUD operations. It follows RESTful principles and includes Swagger documentation for easy API exploration.

## 🚀 Tech Stack
- **Spring Boot** 🛠️
- **Spring Security** 🔒
- **JWT Authentication** 🔑
- **Spring Data JPA** 🗄️
- **Lombok** 📌
- **RabbitMQ** 📨
- **Redis Cache** ⚡
- **Swagger OpenAPI** 📃
- **H2/MySQL Database** 💾
- **JUnit & Mockito** (API Testing) ✅
- **Maven** 🏗️

## 📚 Key Features & Learning Topics
- Secure REST API development with Spring Boot
- User authentication & authorization (JWT-based)
- Spring Security for API protection
- CRUD operations for contacts
- Data validation using `@Valid`
- Password encryption with BCrypt
- Role-based access control (RBAC)
- Environment-based configurations (dev, prod, staging)
- Redis caching for improved performance
- RabbitMQ for message queuing
- Unit & integration testing with JUnit & Mockito
- API documentation with Swagger

## 🌐 API Endpoints

### 🔑 Authentication & User Management
| Method | Endpoint | Description | Access |
|--------|-------------|-------------|--------|
| **POST** | `/auth/register` | Register a new user | Public |
| **POST** | `/auth/login` | Login & receive JWT token | Public |
| **GET** | `/auth/verify` | Verify email via token | Public |
| **POST** | `/auth/forget-password` | Request password reset | Public |
| **POST** | `/auth/reset-password` | Reset password using token | Public |
| **POST** | `/auth/logout` | Logout and invalidate JWT token | Private |

### 📖 Address Book APIs
| Method | Endpoint | Description | Access |
|--------|-------------|-------------|--------|
| **POST** | `/addressbook/add` | Add a new contact | Private |
| **GET** | `/addressbook/get` | Retrieve all contacts (Cached) | Private |
| **GET** | `/addressbook/get/{id}` | Retrieve a contact by ID (Cached) | Private |
| **PUT** | `/addressbook/update/{id}` | Update a contact by ID | Private |
| **DELETE** | `/addressbook/delete/{id}` | Delete a contact by ID | Private |

## ⚡ Redis Caching
This application leverages **Redis** to cache contact data, reducing database load and improving performance.

### 🛠️ Redis Configuration (application.properties)
```properties
spring.cache.type=redis
spring.redis.host=localhost
spring.redis.port=6379
```

## 📌 API Documentation
Explore the API using **Swagger UI**:
🔗 [Swagger UI](http://localhost:8080/swagger-ui.html)

## 📬 RabbitMQ Integration
The project utilizes **RabbitMQ** for background task processing. You can access the RabbitMQ dashboard at:
🔗 [RabbitMQ Management](http://localhost:15672)

---
🚀 **Get started today and build secure, scalable, and efficient contact management solutions!**

