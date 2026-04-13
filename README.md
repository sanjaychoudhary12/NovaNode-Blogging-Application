# 🚀 NovaNode Blog Platform (Backend)

> A production-ready blogging backend built with Spring Boot, featuring JWT authentication, role-based access control, and scalable REST APIs.

---

## 📌 Overview

NovaNode Blog Platform is a backend system designed to power a modern blogging application similar to Medium.
It provides secure, scalable, and well-structured REST APIs for managing users, posts, categories, and comments.

---

## 🧠 Architecture

This project follows **Layered Architecture** with clean separation of concerns:

```
Controller → Service → Repository → Database
```

* **Controller** → Handles HTTP requests
* **Service** → Business logic
* **Repository** → Database operations (JPA)
* **DTO** → Secure data transfer

---

## 🛠️ Tech Stack

| Layer      | Technology            |
| ---------- | --------------------- |
| Backend    | Java, Spring Boot     |
| Security   | Spring Security + JWT |
| ORM        | Hibernate (JPA)       |
| Database   | MySQL                 |
| Build Tool | Maven                 |
| API Docs   | Swagger               |

---

## 🔥 Features

### 🔐 Authentication & Authorization

* JWT-based authentication
* Role-based access (USER / ADMIN)

### 📝 Blog Management

* Create, update, delete posts
* Upload images (extendable to S3)

### 📂 Category Management

* Organize posts by category

### 💬 Comment System

* Add and delete comments

### 🔍 Pagination & Sorting

* Optimized APIs for large datasets

### ⚠️ Global Exception Handling

* Consistent error responses

---

## 📁 Project Structure

```
src/main/java/com/novanode/blog

├── controller      # REST APIs
├── service         # Business logic
├── repository      # JPA repositories
├── entity          # Database models
├── dto             # Request/Response models
├── config          # Security configuration
├── exception       # Global exception handling
```

---

## ⚙️ Local Setup

### ✅ Prerequisites

* Java 17+
* MySQL installed
* Maven installed

---

### 🗄️ Database Setup

```sql
CREATE DATABASE blog_app;
```

---

### 🔧 Configuration

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/blog_app
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

### ▶️ Run Application

```
mvn spring-boot:run
```

or run:

```
BlogAppApisApplication.java
```

---

## 📡 API Endpoints (Sample)

| Method | Endpoint        | Description   |
| ------ | --------------- | ------------- |
| POST   | /api/auth/login | User login    |
| POST   | /api/posts      | Create post   |
| GET    | /api/posts      | Get all posts |
| POST   | /api/comments   | Add comment   |

---

## 🧪 API Testing

Use tools like:

* Postman
* Swagger UI (`/swagger-ui/`)

---

## 🚀 Future Enhancements

* 🐳 Docker containerization
* ☁️ AWS deployment (EC2 + RDS + S3)
* ⚡ Redis caching
* 🔁 CI/CD pipeline (Jenkins/GitHub Actions)
* 📊 Logging & monitoring (ELK stack)

---

## 📈 Scalability Considerations

* Stateless JWT authentication
* Pagination for large datasets
* Layered architecture for maintainability

---

## 👨‍💻 Author

**Sanjay Kumar**
Backend Java Developer

---

## ⭐ Contribution

Feel free to fork, improve, and raise pull requests.

---

## 📜 License

This project is for learning and demonstration purposes.
