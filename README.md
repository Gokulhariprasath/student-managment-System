🎓 Student Management System - Spring Boot REST API

A Spring Boot REST API project to manage student records.
It allows you to create, retrieve, and delete student details stored in a MySQL database.
All endpoints have been tested using Postman.

🧠 Overview

This API helps perform basic CRUD operations for managing student data.
The application uses:

Spring Boot for backend logic

MySQL for data storage

Jackson (JsonNode) for flexible JSON handling

Postman for API testing

🛠️ Tech Stack

Language: Java

Framework: Spring Boot

Database: MySQL

Testing Tool: Postman

Build Tool: Maven

📁 Project Structure
student_management/
│
├── controller/
│   └── StudentController.java
├── service/
│   └── StudentService.java
├── model/
│   └── Student.java
├── repository/
│   └── StudentRepository.java
├── resources/
│   └── application.properties
└── StudentManagementApplication.java

⚙️ MySQL Configuration

Add your database credentials in
📄 src/main/resources/application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
server.port=8080

🧩 API Endpoints

Base URL:

http://localhost:8080/student

Method     	Endpoint   	       Description	
POST	     /create	      Create a new student record	
GET	       /getAll	      Get all students	
GET	       /{studentId}   Get details of a student by ID	
DELETE  	 /{studentId}	  Delete a student by ID	
🧪 Example API Testing (Postman)
➕ Create a Student

POST → http://localhost:8080/student/create
Body (JSON):

{
"studentName":"Minato",
"emailId":"minat@gmail.com",
"phoneNo":"2023101905"
}


Response:

{"status":"success","message":"data saved successfully","studentId":4}
