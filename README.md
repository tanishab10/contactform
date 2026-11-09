# Maincrafts Java Full Stack Internship – Task 4

## Project Overview

This project implements Login Authentication and Role-Based Access Control (RBAC) using Spring Security.

The application allows only authenticated ADMIN users to access the contact dashboard and view submitted contact information.

## Technologies Used

- Java 17
- Spring Boot 3.5.6
- Spring Security
- Spring Data JPA
- MySQL
- HTML
- CSS
- JavaScript
- Maven

## Features

1. Admin Login Authentication.
2. BCrypt Password Encryption.
3. Role-Based Access Control.
4. Protected Admin Dashboard.
5. Contact Form Submission.
6. Contact Data Storage in MySQL.
7. Secure Logout Functionality.
8. Unauthorized Access Restriction.

## Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE contactdb;
```

Update the database credentials in:

`src/main/resources/application.properties`

## Admin Credentials

Use the credentials configured in DataInitializer.java.

Example:

- Username: Your configured admin username.
- Password: Your configured admin password.
- Role: ADMIN.

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Open the Project

Open the project folder in VS Code.

### Step 3: Build the Project

```bash
.\mvnw.cmd clean install
```

### Step 4: Run the Application

```bash
.\mvnw.cmd spring-boot:run
```

### Step 5: Open the Application

Contact Form:

http://localhost:8080/

Admin Login:

http://localhost:8080/login.html

Admin Dashboard:

http://localhost:8080/contacts.html

## Security

- Passwords are stored using BCrypt hashing.
- Only ADMIN users can access the contacts dashboard.
- Unauthorized users are redirected to the login page.
- Logout functionality terminates the authenticated session.

## Internship

Maincrafts Java Full Stack Internship – Task 4