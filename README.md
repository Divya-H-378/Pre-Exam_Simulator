# VTU Pre-Examination Portal – Prexam Simulator

A web-based examination application developed to simulate and manage the **VTU semester examination registration process**. The application provides functionality for student profile management, subject selection, application processing, approval tracking, and hall-ticket generation.

## Problems It Solves

The project addresses common challenges involved in managing examination registration and application processing:

- **Manual examination registration:** Provides a digital platform for students to complete and manage examination registrations.
- **Subject selection management:** Allows students to select and process subjects through a structured application workflow.
- **Application processing:** Organizes examination applications through different processing and approval stages.
- **Status tracking:** Provides status information for submitted applications, reducing the need for manual follow-up.
- **Hall-ticket management:** Supports hall-ticket generation after the required application processing and approval stages.
- **Data management:** Stores and manages student, subject, and examination-related information using a relational database.

## Features

- **Student Profile Management:** Maintains student information required for examination registration.
- **Semester Examination Registration:** Allows students to register for semester examinations.
- **Subject Selection:** Provides functionality for selecting subjects during examination registration.
- **Multi-Stage Approval:** Processes applications through defined approval stages.
- **Application Status Tracking:** Tracks the current status of examination applications.
- **Hall-Ticket Generation:** Generates hall tickets after successful application processing.
- **Database Integration:** Stores and retrieves application data using MySQL.
- **Web-Based Interface:** Provides a simple interface for managing examination-related activities.

## Technologies Used

- **Programming Language:** Java
- **Backend Framework:** Spring Boot
- **Template Engine:** Thymeleaf
- **Frontend:** HTML, Bootstrap
- **Database:** MySQL
- **Database Access:** Spring JDBC / JdbcTemplate
- **Development Environment:** IntelliJ IDEA

## System Workflow

The application follows a structured examination registration workflow:

```text
                 ┌──────────────────────┐
                 │     Student Login     │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │  Student Profile     │
                 │      Management      │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │ Semester & Subject   │
                 │      Selection       │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │ Examination          │
                 │ Registration         │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │ Application         │
                 │ Processing & Approval│
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │ Application Status   │
                 │      Tracking        │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │   Hall-Ticket        │
                 │     Generation       │
                 └──────────────────────┘
```

## Database

The application uses **MySQL** to store and manage examination-related information.

The database handles:

- Student profiles
- Semester information
- Subject details
- Examination registrations
- Selected subjects
- Application status
- Approval information
- Hall-ticket-related data

Database operations are implemented using **Spring JDBC (`JdbcTemplate`)** for executing queries and processing application data.

## Application Architecture

The application follows a layered Spring Boot structure to separate different responsibilities:

```text
        ┌──────────────────────┐
        │      Thymeleaf       │
        │    + Bootstrap UI    │
        └──────────┬───────────┘
                   ▼
        ┌──────────────────────┐
        │      Controller      │
        └──────────┬───────────┘
                   ▼
        ┌──────────────────────┐
        │       Service        │
        │    Business Logic    │
        └──────────┬───────────┘
                   ▼
        ┌──────────────────────┐
        │    JDBC / Repository │
        │      JdbcTemplate    │
        └──────────┬───────────┘
                   ▼
        ┌──────────────────────┐
        │        MySQL         │
        └──────────────────────┘
```

## Project Outcome

The project provided practical experience in developing a **Java-based web application using Spring Boot**, including database integration, CRUD/database operations, application logic, workflow implementation, status tracking, and server-side web page rendering using Thymeleaf.

## Future Improvements

- Add role-based access for students, faculty, and administrators.
- Implement secure authentication and authorization.
- Add email/SMS notifications for application status updates.
- Provide an administrator dashboard for managing examination applications.
- Improve validation and error handling.
- Add automated testing for application workflows and database operations.
