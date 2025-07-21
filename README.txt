# 👤 User Management System (JSP + Servlet + JDBC + MySQL)

This is a simple **web-based User Management System** built using **JSP**, **Servlet**, **JDBC**, and **MySQL**, deployed on **Apache Tomcat**. The application allows CRUD operations (Create, Read, Update, Delete) on user data through a browser interface.

---

## 📋 Features

- Add new users with name, email, and country
- Edit existing user information
- Delete a user from the system
- View list of users in a styled HTML table
- Structured MVC architecture
- Uses JDBC with `PreparedStatement` for secure DB interactions

---

## 🛠️ Technologies Used

- Java (JDK 8+)
- JSP (JavaServer Pages)
- Servlet API
- JDBC (Java Database Connectivity)
- MySQL (Database)
- Apache Tomcat 8.5 (Web Server)
- Eclipse IDE

---

## 🗃️ Database Schema

Create a MySQL database `users_db` with the following table:

### `users`

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    country VARCHAR(100) NOT NULL
);
```

---

## 📁 Project Structure

```
WebContent/
├── user-list.jsp
├── user-form.jsp
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

## ▶️ How to Run

1. Clone or download this repository.
2. Import it as a **Dynamic Web Project** in **Eclipse**.
3. Configure **Apache Tomcat 8.5** in Eclipse.
4. Add **MySQL JDBC Driver** (`mysql-connector-j-8.x.x.jar`) to your project's `lib` or Build Path.
5. Create the database and table in MySQL using the above schema.
6. Update DB credentials in `UserDao.java`:

```java
private static String jdbcURL = "jdbc:mysql://localhost:3306/users_db";
private static String jdbcUsername = "your_mysql_username";
private static String jdbcPassword = "your_mysql_password";
```

7. Run the project on Tomcat Server.
8. Visit `http://localhost:8080/UserManagementApp` in your browser.

---

## 🚫 Notes

- This is a beginner-level project for educational purposes.
- Database credentials are hardcoded — secure them properly in real deployments.
- Can be extended to use MVC frameworks like Spring.

---

## 🙌 Author

Created by Varsha SP  
| Java learner/Java Web App Developer

---

## 📄 License

Free to use for learning and educational purposes.
