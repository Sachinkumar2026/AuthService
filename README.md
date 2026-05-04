# 🔐 Auth Service (JWT) - Expense Tracker Microservices

This repository contains the **Authentication Service** for a microservices-based **Expense Tracker** application.
It handles user authentication, authorization, and secure token management using **JWT (JSON Web Tokens)**.

---

## 🚀 Features

* 🔑 User Registration & Login
* 🔐 JWT-based Authentication
* 🛡️ Role-based Authorization
* ♻️ Token Validation & Refresh (optional if implemented)
* 📦 REST APIs for authentication workflows
* 🧩 Designed for Microservices Architecture

---

## 🏗️ Tech Stack

* **Backend:** Spring Boot
* **Security:** Spring Security
* **Authentication:** JWT (JSON Web Tokens)
* **Database:** MySQL
* **Build Tool:** Maven / Gradle
* **Containerization:** Docker (if used)

---

## 📁 Project Structure

```
auth-service/
│── src/main/java/com/example/authservice
│   ├── config/        # Security & JWT configuration
│   ├── controller/    # REST controllers
│   ├── service/       # Business logic
│   ├── repository/    # Database access
│   ├── model/         # Entities
│   └── dto/           # Data Transfer Objects
│
│── src/main/resources/
│   └── application.properties
│
│── pom.xml / build.gradle
│── Dockerfile (if applicable)
│── README.md
```

---

## 🔑 API Endpoints

### 🧾 Authentication APIs

| Method | Endpoint         | Description         |
| ------ | ---------------- | ------------------- |
| POST   | `/auth/register` | Register a new user |
| POST   | `/auth/login`    | Login & get JWT     |
| GET    | `/auth/validate` | Validate token      |

---

## ⚙️ Setup & Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/auth-service.git
cd auth-service
```

---

### 2️⃣ Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/authservice
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

### 3️⃣ Run the Application

```bash
./mvnw spring-boot:run
```

or

```bash
mvn spring-boot:run
```

---

### 4️⃣ Run with Docker

```bash
docker build -t auth-service .
docker run -p 8080:8080 auth-service
```

---

## 🔐 JWT Flow

1. User logs in with credentials
2. Server validates user
3. JWT token is generated
4. Client stores token
5. Token is sent with each request
6. Server validates token before granting access

---

## 🧪 Testing

You can test APIs using:

* Postman
* cURL

---

## 🌐 Role in Microservices Architecture

This service acts as:

* 🔑 Central Authentication Server
* 🛡️ Security Gateway for other services
* 📡 Token provider for inter-service communication

---

## 📌 Future Improvements

* OAuth2 Integration
* API Gateway Integration
* Rate Limiting
* Logging & Monitoring

---

## 👨‍💻 Author

Sachin

---

## 📄 License

This project is licensed under the MIT License.

---
