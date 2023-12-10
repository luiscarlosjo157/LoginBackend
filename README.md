# User Management CRUD with Spring Boot and Spring Security

### Overview

The User Management CRUD application, built with Spring Boot and secured by Spring Security, empowers developers to implement a robust and secure system for handling user-related operations. This application provides a seamless experience for creating, reading, updating, and deleting user records while ensuring the integrity and confidentiality of user data.

### Key Features

- **Create Users:** The application allows the creation of new user accounts with essential information such as username, password, and role. Leveraging Spring Boot's simplicity, the process is straightforward and secure.
- **Read Users:** Users can be queried from the system, enabling administrators to access detailed information about each user. The Read functionality provides a snapshot of user data, promoting effective user management.
- **Update Users:** Administrators can update user details, ensuring that user information remains accurate and up-to-date. Spring Boot's flexibility makes the update process seamless, guaranteeing data consistency.
- **Delete Users:** When necessary, administrators can delete user accounts securely. The application handles deletions gracefully, adhering to best practices for data integrity.
- **Secure Authentication and Authorization:** With Spring Security, the application ensures secure authentication and authorization mechanisms. Passwords are securely hashed, and access control is enforced based on user roles, preventing unauthorized access to sensitive functionalities.

### Technology Stack

- **Spring Boot:** A powerful and convention-over-configuration framework that simplifies the development of Java-based applications. It streamlines the setup and deployment process, allowing developers to focus on business logic.
- **Spring Security:** An industry-standard framework for securing Java applications. It provides comprehensive security services for Java EE-based enterprise software applications.
- **Hibernate:** The de-facto standard for object-relational mapping (ORM) in Java. Hibernate simplifies database interactions, allowing developers to work with objects in their application code.

- **MySQL:** One of the most robust relational databases on the market, supported by ORACLE.

## Table of Contents

- [Requirements](#requirements)
- [Recommendations](#recommendations)
- [Configuration](#configuration)
- [Endpoints](#endpoints)
- [Contributing](#contributing)
- [License](#license)

## Requirements

- Java v17
- Spring boot ^3
- Any database (recommended **MySQL**)
- Use IntelliJ IDEA for running the project

## Recommendations

- If you can use vscode to run the project, only download the [spring boot extension for vscode](https://code.visualstudio.com/docs/java/java-spring-boot)

## Configuration

- In **`application.properties`** you can set up the database, custom in base your preferences
```
spring.datasource.url=jdbc:mysql://localhost:3306/db_user_spring_boot
spring.datasource.username=user
spring.datasource.password=password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
logging.level.org.hibernate.SQL=debug
```
## Endpoints

You can consult the swagger docs in [localhost:8080/swagger-ui/index.html](localhost:8080/swagger-ui/index.html) after in explorer put `/api-docs`

### Create User

* **Endpoint:** `/users`
* **Method:** POST
* **Request Body:**
`{  "username": "3", "password": "some password", "email": "email@gmail.com }`
* **Response:**
`200 status code`

### Get Users

**Endpoint:** `/users`
**Method:** GET
**Request Body**:
`[{  "username":  "john_doe", password":  "secure password", "roles":  "admin"  }]`

### Get User

* **Endpoint:** `/users/<id>`
* **Method:** GET
* **Request Body**:
`{"id": 3}`
* **Response**:
`{  "username":  "john_doe", password":  "secure password", "roles":  "admin"  }`

### Update User

* **Endpoint:** `/users`
* **Method:** PUT
* **Request Body:**
`{  "username": "new name" }`
* **Response:**
`{  "username": "new name", "password": "secure password", "roles": "admin" }`

### Delete User

* **Endpoint:** `/users`
* **Method:** DELETE
* **Request Body:**
`{  "id": "3" }`
* **Response:**
`204 No Content`

## Contributing

Feel free to contribute to the project by submitting issues or pull requests.

## License

This project is licensed under the Apache license 2.0 `Apache-2.0`.
