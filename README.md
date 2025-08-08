# SpringBoot CRUD Assignments

Java Spring Boot **CRUD** web app for **PROG32758 – Enterprise Java Development** (Assignments **3 & 4**).  
Implements create/read/update/delete operations with a simple HTML/Thymeleaf UI and an H2 in-memory database.

> **Author:** Krushali Chauhan • **Student ID:** 991772564

---

## ✨ Features

- **CRUD UI**: `index.html` (list), `insert.html`, `update.html`, `delete.html`
- **Spring Boot + Maven** with embedded server
- **H2 in-memory database** with console
- **Validation & error handling** (basic)
- **Docs** in `/doc` (HTML)

---

## 🧱 Tech Stack

- **Java** 17
- **Spring Boot** (Web, Thymeleaf, H2, Validation)
- **Maven** (with wrapper `mvnw`)
- **Thymeleaf** templates

---

## 🗂 Project Structure
SpringBoot-CRUD-Assignments/
├─ src/
│ ├─ main/
│ │ ├─ java/
│ │ │ └─ [your/package]/ # controllers, models, repositories, services
│ │ ├─ resources/
│ │ │ ├─ static/ # css/js (if any)
│ │ │ ├─ templates/
│ │ │ │ ├─ index.html
│ │ │ │ ├─ insert.html
│ │ │ │ ├─ update.html
│ │ │ │ └─ delete.html
│ │ │ └─ application.properties
│ └─ test/java/ # JUnit tests (if included)
├─ doc/ # assignment docs (HTML)
├─ pom.xml
├─ mvnw / mvnw.cmd
└─ .gitignore / README.md

---

## ⚙️ Configuration

`src/main/resources/application.properties` (example):

```properties
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

spring.datasource.url=jdbc:h2:mem:demo;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

H2 Console: http://localhost:8080/h2-console

JDBC URL: jdbc:h2:mem:demo

User: sa, Password: (blank)

Run Locally
Using the Maven wrapper:

bash
Copy code
# From project root
./mvnw spring-boot:run     # macOS/Linux
mvnw.cmd spring-boot:run   # Windows
Then open: http://localhost:8080

Build a JAR
bash
Copy code
./mvnw clean package
java -jar target/*.jar


🧭 App Navigation
GET / → Home/list page (index.html)

GET /insert → Show create form (insert.html)

POST /insert → Create record

GET /update/{id} → Show update form (update.html)

POST /update/{id} → Update record

POST /delete/{id} → Delete record

GET /h2-console → H2 DB console

🧪 Testing
bash
Copy code
./mvnw test
📑 Assignment Mapping
Assignment 3:

Build Spring Boot web app with forms

Implement server-side handling & validation

Display results and lists via Thymeleaf

Assignment 4:

Full CRUD (Create, Read, Update, Delete)

H2 database integration and console access

Clean controller/service/repository layering

🙌 Credits
Spring Boot Team & Guides

H2 Database

Thymeleaf
