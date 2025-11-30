
# Student CRUD REST API (Spring Boot)

A simple **Spring Boot REST API** that performs **CRUD operations** on a `Student` entity using **Spring Data JPA** and **MySQL** (or any supported database).


## 🚀 Features

-   Create a new student
-   Get all students
-   Get a student by ID
-   Update student details
-   Delete student
-   Uses Spring Boot + JPA Repository
-   JSON-based REST API

## 🛠 Technologies Used

-   Java 17
-   Spring Boot
-   Spring Web
-   Spring Data JPA
-   MySQL (or H2)
-   Maven

## Project Structure

src/main/java/com/jules/restapi
 ├── controller
 │     └── StudentController.java
 ├── entity
 │     └── Student.java
 └── repository
       └── StudentRepository.java
# ⚙️ Setup & Run

## 1. Clone the Repository

`git clone https://github.com/your-username/your-repo-name.git`
`cd your-repo-name`

## 2. Configure Database

Inside `src/main/resources/application.properties`:

    spring.application.name=SpringBootRestAPIProject
    spring.datasource.url=jdbc:mysql://localhost:3306/studentdatabase
    spring.datasource.username=root
    spring.datasource.password=
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true

## 3. Run the Application

`mvn spring-boot:run`

# API Endpoints

### Get all students
`GET /students`
### Get student by ID
`GET /students/{id}`
### Add new student
    POST /student/add
    Content-Type: application/json
Body:

    {
      "name": "Jules",
      "percentage": 92.5,
      "branch": "IT"
    }
### Update student

    PUT /student/update/{id}
    Content-Type: application/json
### Delete student
`DELETE /student/delete/{id}`

## Student Entity

    private int rollNo;
    private String name;
    private float percentage;
    private String branch;

## Notes

-   `rollNo` is auto-generated.
-   The API returns JSON.
-   You can test easily using **Postman** or **cURL**.
