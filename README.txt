# User Management Web Application

## 📋 Project Overview

This is a **Java-based web application** built using the following technologies:

- Java Servlet & JSP (Java EE)
- JDBC for database connectivity
- MySQL for backend database
- Apache Tomcat 8.5 as the server
- JSP Standard Tag Library (JSTL)
- Eclipse IDE for development

The application supports basic CRUD (Create, Read, Update, Delete) operations for managing users.

---

## 📁 Features

- List all users from the database
- Add a new user
- Edit existing user details
- Delete a user
- Display meaningful error messages

---

## 🚀 How to Run the Project

1. **Clone or download** the project source code into your Eclipse workspace.
2. **Import** it as a *Dynamic Web Project* in Eclipse.
3. **Configure Apache Tomcat 8.5** in Eclipse if not already done.
4. **Add MySQL JDBC driver (mysql-connector-j)** to your project’s `lib` folder or Build Path.
5. **Start MySQL Server** and create a schema:
    ```sql
    CREATE DATABASE users_db;
    ```
6. **Create the `users` table** with the following structure:
    ```sql
    CREATE TABLE users (
        id INT PRIMARY KEY AUTO_INCREMENT,
        name VARCHAR(100) NOT NULL,
        email VARCHAR(100) NOT NULL,
        country VARCHAR(100) NOT NULL
    );
    ```
7. **Deploy the project** to Tomcat server from Eclipse.
8. **Visit in browser**:  
   [http://localhost:8080/UserManagementApp](http://localhost:8080/UserManagementApp)

---

## 🛠 Configuration

Edit the following credentials in `UserDao.java` based on your MySQL setup:

```java
private static String jdbcURL = "jdbc:mysql://localhost:3306/users_db";
private static String jdbcUsername = "root";
private static String jdbcPassword = "your_password";
```

---

## 📦 Folder Structure

```
WebContent/
├── user-list.jsp
├── user-form.jsp
├── Error.jsp
└── WEB-INF/
    └── web.xml

src/
└── com.xadmin.usermanagement/
    ├── model/
    │   └── User.java
    ├── dao/
    │   └── UserDao.java
    └── web/
        └── UserServlet.java
```

---

## 📌 Author

Created by Varsha | Java learner

Project implemented by following a guided tutorial.

---

## 📃 License

This project is open-source and free to use for learning or modification.