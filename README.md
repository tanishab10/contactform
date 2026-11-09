# Maincrafts Java Full Stack Internship

## Project Overview

The Contact Management System is a Java Full Stack application developed as part of the Maincrafts Java Full Stack Internship.

The application allows users to submit their contact details through a web form. The submitted information is stored in a MySQL database and can be viewed by an authenticated administrator through a secure Contact Management Dashboard.

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
- VS Code

## Features

### Task 2 – Contact Form

- User-friendly contact form.
- Accepts name, email and message.
- Saves submitted details into MySQL.
- Uses Spring Boot to handle form submissions.

### Task 3 – Contact Management Dashboard

- REST API endpoint: GET /contacts
- Retrieves all saved contacts from MySQL.
- Returns contact details in JSON format.
- Uses JavaScript Fetch API to retrieve backend data.
- Displays contacts dynamically in an HTML table.

### Task 4 – Authentication and Authorization

- Admin login using Spring Security.
- Role-Based Access Control (RBAC).
- BCrypt password encryption.
- Protected contacts endpoint.
- Only ADMIN users can access the dashboard.
- Custom admin login page.
- Logout functionality.
- Unauthorized access restriction.

## Project Structure

```text
contactform/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── contactform/
│   │   │       ├── Contact.java
│   │   │       ├── ContactController.java
│   │   │       ├── ContactRepository.java
│   │   │       ├── ContactformApplication.java
│   │   │       ├── User.java
│   │   │       ├── UserRepository.java
│   │   │       ├── SecurityConfig.java
│   │   │       └── DataInitializer.java
│   │   │
│   │   └── resources/
│   │       ├── static/
│   │       │   ├── index.html
│   │       │   ├── contacts.html
│   │       │   └── login.html
│   │       └── application.properties
│   │
│   └── test/
│
├── pom.xml
└── README.md
```

## Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE contactdb;
```

Configure database credentials using environment variables.

In application.properties:

```properties
spring.datasource.username=${DB_USERNAME:root}
spring.datasource.password=${DB_PASSWORD}
```

Set the environment variables before running the application.

## Admin Credentials

The initial admin account is created automatically by DataInitializer.java.

- Username: As configured in DataInitializer.java.
- Password: As configured in DataInitializer.java.
- Role: ADMIN.

Passwords are stored using BCrypt hashing.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | /contact | Submit contact form |
| POST | /submit | Submit contact form |
| GET | /contacts | Retrieve all contacts (ADMIN only) |
| POST | /login | Admin authentication |
| POST | /logout | Logout |

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone <your-github-repository-url>
```

### Step 2: Open the Project

Open the project folder in VS Code or IntelliJ IDEA.

### Step 3: Configure MySQL

Create the contactdb database and configure your database credentials.

### Step 4: Build the Project

On Windows, run:

```powershell
.\mvnw.cmd clean install
```

### Step 5: Run the Application

```powershell
.\mvnw.cmd spring-boot:run
```

### Step 6: Open the Application

Contact Form:

http://localhost:8080/

Admin Login:

http://localhost:8080/login.html

Admin Dashboard:

http://localhost:8080/contacts.html

## Security

- Passwords are encrypted using BCrypt.
- Only authenticated ADMIN users can access the contacts dashboard.
- Unauthorized users cannot access protected resources.
- Spring Security manages login and logout.

## Screenshots

The submission includes screenshots of:

1. Admin Login Page.
2. Unauthorized Access Page.
3. Admin Dashboard displaying submitted contacts.

## Internship Details

Organization: Maincrafts

Internship: Java Full Stack Internship

Tasks: Task 2, Task 3 and Task 4

---

Developed by Tanisha Behera.