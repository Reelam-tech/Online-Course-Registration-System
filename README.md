# Online Course Registration System

A desktop application developed for the **Advanced Programming Language (CS313)** course. The system allows students, professors, and administrators to manage university course registration through role-based dashboards.

## Project Overview

The Online Course Registration System was developed using JavaFX and connected to an Oracle database through JDBC.

The application provides different features based on the logged-in user's role:

* Student
* Professor
* Administrator

## Features

### Student Dashboard

Students can:

* View available courses.
* Register for open courses.
* Drop registered courses.
* View their current course schedule.
* Check course information and availability.

### Professor Dashboard

Professors can:

* View their assigned courses.
* View students enrolled in each course.
* Update course information.
* Open or close course registration.
* Manage course availability.

### Administrator Dashboard

Administrators can:

* Add, edit, and delete users.
* Add, edit, and delete courses.
* Assign professors to courses.
* Manage students and professors.
* Control course registration availability.

## Technologies Used

* Java
* JavaFX
* FXML
* CSS
* Oracle Database
* JDBC
* SQL
* NetBeans IDE

## Programming Concepts Applied

The project demonstrates several concepts covered in the Advanced Programming Language course:

* Object-Oriented Programming
* Inheritance
* Encapsulation
* Polymorphism
* Interfaces
* Composition
* Exception Handling
* Java Collections
* Generic Collections
* JavaFX Graphical User Interface
* FXML Controllers
* Database Programming using JDBC
* Prepared Statements and Result Sets
* Data Access Object Design Pattern
* Model-View-Controller Architecture

## Object-Oriented Design

The system contains a main `User` class with specialized user types:

* `Student`
* `Professor`
* `Admin`

Inheritance is used to share common user information while allowing each role to have its own functions and permissions.

## Project Structure

```text
OnlineCourseRegistrationSystemApp1/
│
├── src/
│   └── onlinecourseregistrationsystemapp1/
│       ├── controller/
│       │   ├── AdminDashboardController.java
│       │   ├── LoginController.java
│       │   ├── ProfessorDashboardController.java
│       │   └── StudentDashboardController.java
│       │
│       ├── dao/
│       │   ├── CourseDAO.java
│       │   ├── DatabaseConnection.java
│       │   ├── EnrollmentDAO.java
│       │   └── UserDAO.java
│       │
│       ├── model/
│       │   ├── Admin.java
│       │   ├── Course.java
│       │   ├── Enrollment.java
│       │   ├── Professor.java
│       │   ├── Student.java
│       │   └── User.java
│       │
│       ├── sql/
│       │   └── database_setup.sql
│       │
│       ├── util/
│       │   ├── AlertUtil.java
│       │   ├── NavigationUtil.java
│       │   └── SessionManager.java
│       │
│       ├── view/
│       │   ├── AdminDashboard.fxml
│       │   ├── Login.fxml
│       │   ├── ProfessorDashboard.fxml
│       │   ├── StudentDashboard.fxml
│       │   └── styles.css
│       │
│       └── OnlineCourseRegistrationSystemApp1.java
│
├── build.xml
├── manifest.mf
└── README.md
```

## Database Structure

The Oracle database contains three main tables:

### USERS

Stores user account information, including:

* User ID
* Username
* Password
* Role
* First name
* Last name
* Email

### COURSES

Stores course information, including:

* Course ID
* Course code
* Course name
* Description
* Credit hours
* Capacity
* Assigned professor
* Registration status

### ENROLLMENTS

Stores student course registrations, including:

* Enrollment ID
* Student ID
* Course ID
* Enrollment date

## Requirements

To run the application, the following software is required:

* Java Development Kit with JavaFX support
* NetBeans IDE
* Oracle Database
* Oracle SQL Developer or SQL*Plus
* Oracle JDBC Driver, such as `ojdbc8.jar`

## Installation and Setup

### 1. Download the Project

Clone or download the repository:

```bash
git clone https://github.com/USERNAME/online-course-registration-system.git
```

Replace `USERNAME` with the GitHub username that owns the repository.

### 2. Open the Project

1. Open NetBeans IDE.
2. Select **File**.
3. Select **Open Project**.
4. Choose the project folder.
5. Wait for NetBeans to load the project.

### 3. Add the Oracle JDBC Driver

1. Right-click the project in NetBeans.
2. Select **Properties**.
3. Open the **Libraries** section.
4. Select **Add JAR/Folder**.
5. Add the Oracle JDBC driver file, such as `ojdbc8.jar`.

### 4. Set Up the Database

1. Start the Oracle database.
2. Open Oracle SQL Developer or SQL*Plus.
3. Connect to the Oracle database.
4. Open the following file:

```text
src/onlinecourseregistrationsystemapp1/sql/database_setup.sql
```

5. Run the SQL script to create the tables, sequences, and sample data.

### 5. Configure the Database Connection

Open:

```text
src/onlinecourseregistrationsystemapp1/dao/DatabaseConnection.java
```

Update the database URL, username, and password according to the local Oracle Database configuration.

Example connection URL:

```java
jdbc:oracle:thin:@//localhost:1521/orcl12
```

### 6. Run the Application

Run the following main class:

```text
OnlineCourseRegistrationSystemApp1.java
```

## Demo Accounts

The database setup script creates the following sample accounts:

| Role          | Username | Password   |
| ------------- | -------- | ---------- |
| Administrator | admin    | admin123   |
| Professor     | prof1    | prof123    |
| Professor     | prof2    | prof123    |
| Student       | student1 | student123 |
| Student       | student2 | student123 |
| Student       | student3 | student123 |

These accounts are provided for testing and demonstration purposes.

## Security Notice

Database connection credentials should be changed before publishing or deploying the application.

For a production system:

* Do not store passwords directly in the source code.
* Use environment variables or a secure configuration file.
* Encrypt user passwords before storing them.
* Do not use an administrator database account for the application.
* Create a dedicated database user with limited permissions.

## Course Information

**Course:** Advanced Programming Language
**Course Code:** CS313
**Project Type:** Term Project
**Academic Year:** 2025–2026

## Purpose

This project was created for educational purposes to demonstrate advanced Java programming concepts, JavaFX graphical interfaces, object-oriented design, database connectivity, and role-based application development.
