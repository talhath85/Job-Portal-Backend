# Job Portal Backend

A RESTful backend API for a Job Portal application built with **Java** and **Spring Boot**. This service provides the core business logic and data access layer for managing job listings, user accounts, and applications.

---

## Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Running Tests](#running-tests)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The Job Portal Backend exposes a set of REST APIs that power a job portal platform. It handles job postings, user authentication, and application management, making it easy to connect employers with job seekers.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 17+ |
| Framework | Spring Boot |
| Build Tool | Maven |
| Database | MySQL / PostgreSQL (configurable) |
| ORM | Spring Data JPA / Hibernate |
| Security | Spring Security |

---

## Project Structure

```
Job-Portal-Backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/jobportal/
│   │   │       ├── controller/       # REST controllers
│   │   │       ├── model/            # JPA entities
│   │   │       ├── repository/       # Spring Data repositories
│   │   │       ├── service/          # Business logic
│   │   │       └── JobPortalApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/                     # Unit and integration tests
├── .mvn/wrapper/
├── pom.xml
├── mvnw
└── mvnw.cmd
```

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

- **Java 17** or higher — [Download](https://adoptium.net/)
- **Maven 3.6+** (or use the included `mvnw` wrapper)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/talhath85/Job-Portal-Backend.git
cd Job-Portal-Backend
```

2. Install dependencies:

```bash
./mvnw install
```

### Configuration

Update `src/main/resources/application.properties` with your database credentials:

```properties
# Server
server.port=8080
```

### Running the Application

Using the Maven wrapper:

```bash
# Linux / macOS
./mvnw spring-boot:run

# Windows
mvnw.cmd spring-boot:run
```

The server will start at `http://localhost:8080`.

---

## API Endpoints

Below is a general overview of the available API routes. All endpoints return JSON.

### Jobs

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/jobPosts` | Get all job listings |
| `GET` | `/jobPosts/{postId}` | Get a job by ID |
| `POST` | `jobPosts` | Create a new job posting |
| `PUT` | `jobPosts` | Update a job posting |
| `DELETE` | `/jobPosts/{postId}` | Delete a job posting |

---

## Running Tests

```bash
./mvnw test
```

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a Pull Request
