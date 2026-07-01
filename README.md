# Project Day-2





....................

A backend-based Banking Management System built using Spring Boot that allows users to manage bank accounts and perform secure financial transactions through RESTful APIs.

---

## 🚀 Features

* Create, update, delete, and fetch bank accounts
* Deposit and withdraw money with validation
* Transfer funds between accounts
* Input validation and global exception handling
* DTO-based architecture for secure data transfer

---

## 🏗️ Architecture

This project follows a layered architecture:

* **Controller Layer** → Handles HTTP requests and responses
* **Service Layer** → Contains business logic
* **Repository Layer** → Interacts with the database

---

## 🛠️ Tech Stack

* Backend: Spring Boot
* Language: Java
* Database: MySQL
* ORM: Spring Data JPA / Hibernate
* Build Tool: Maven
* API Testing: Postman

---

## 📂 Project Structure

src/
├── controller/
├── service/
├── repository/
├── entity/
├── dto/
└── exception/

---

## 🔐 API Endpoints

### 📌 Account APIs

| Method | Endpoint       | Description       |
| ------ | -------------- | ----------------- |
| POST   | /accounts      | Create account    |
| GET    | /accounts/{id} | Get account by ID |
| PUT    | /accounts/{id} | Update account    |
| DELETE | /accounts/{id} | Delete account    |

---

### 💰 Transaction APIs

| Method | Endpoint                | Description    |
| ------ | ----------------------- | -------------- |
| POST   | /accounts/{id}/deposit  | Deposit money  |
| POST   | /accounts/{id}/withdraw | Withdraw money |
| POST   | /accounts/transfer      | Transfer funds |

---

## ⚙️ Setup & Run

1. Clone the repository

```
git clone https://github.com/your-username/banking-management-system.git
```

2. Navigate to project folder

```
cd banking-management-system
```

3. Configure MySQL in `application.properties`

```
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

4. Run the application

```
mvn spring-boot:run
```

---

## 📌 Sample JSON Request

### Create Account

```
{
  "name": "John Doe",
  "balance": 5000
}
```

---

## ⚠️ Validations

* Prevents withdrawal if balance is insufficient
* Ensures valid account data input
* Handles exceptions using global exception handler

---

## 📈 Future Enhancements

* Add authentication & authorization (JWT)
* Implement transaction history
* Add frontend UI (React / Angular)
* Docker deployment

---

