
# Contact Management System

A Java Full Stack project developed as part of the Maincrafts Java Full Stack Internship.

## Project Overview

The Contact Management System allows users to submit their contact details through a web form. The submitted information is stored in a MySQL database and can be viewed by an admin through a Contact Management Dashboard.

## Technologies Used

- Java
- Spring Boot
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
- REST API endpoint: `GET /contacts`
- Retrieves all saved contacts from MySQL.
- Returns contact details in JSON format.
- Uses JavaScript Fetch API to retrieve backend data.
- Displays contacts dynamically in an HTML table.

## Project Structure

```text
contactform/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── contactform/
│       │       ├── Contact.java
│       │       ├── ContactController.java
│       │       ├── ContactRepository.java
│       │       └── ContactformApplication.java
│       │
│       └── resources/
│           ├── static/
│           │   ├── index.html
│           │   └── contacts.html
│           └── application.properties
│
├── pom.xml
└── README.md
```

## API Endpoint

| Method | Endpoint | Description |
|---|---|---|
| GET | `/contacts` | Retrieves all saved contacts |

## How to Run the Project

1. Clone the repository.

```bash
git clone https://github.com/tanishab10/contactform.git
```

2. Open the project in VS Code or IntelliJ IDEA.

3. Configure your MySQL database in `application.properties`.

4. Run the Spring Boot application.

```bash
.\mvnw.cmd spring-boot:run
```

5. Open the contact form:

`http://localhost:8080/`

6. Open the Contact Management Dashboard:

`http://localhost:8080/contacts.html`

7. View the JSON response:

`http://localhost:8080/contacts`

## Screenshots

Screenshots of the Contact Form, Contact Management Dashboard and REST API response are available in the `screenshots` folder.

## Internship

**Organization:** Maincrafts

**Internship:** Java Full Stack Internship

**Tasks Completed:** Task 2 and Task 3

---

Developed by **Tanisha Behera**
