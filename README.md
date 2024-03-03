REST API for Bus Reservation System Portal
We have developed this REST API for a Bus Reservation System Portal Application. This API performs all the fundamental CRUD operations of any Bus Reservation Application platform with user validation at every step.
Tech Stack
Java
Spring Framework
Spring Boot
Spring Data JPA
Hibernate
MySQL
Modules
Login, Logout Module
Admin Module
User Module
Route Module
Bus Module
Reservation Module
Feedback Module
Features
User and Admin authentication & validation with session uuid.
Admin Features:
Administrator Role of the entire application
Only registered admins with valid session token can add/update/delete route and bus from main database
Admin can access the details of different users and reservations.
User Features:
Registering themselves with application, and logging in to get the valid session token
Viewing list of available buses and booking a reservation
Only logged in user can access his reservations, profile updation and other features.
Contributors
Nikhil Bhardwaj
Sandhya Potadar
Yuvraj Rajarawal
Dheeraj Pandey
Installation & Run
Before running the API server, you should update the database config inside the application.properties file.
Update the port number, username and password as per your local database config.
    server.port=8888

    spring.datasource.url=jdbc:mysql://localhost:3306/busdb
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=root

API Root Endpoint
https://localhost:8888/

http://localhost:8888/swagger-ui/

API Module Endpoints
Login Module
POST //login/admin : Admin can login with mobile number and password provided at the time of registation
Sample API Response for Admin Login
POST   localhost:8888/login/admin

Request Body
    {
        "mobileNo": "8651060999",
        "password": "Clickme@007"
    }
Response
   CurrentAdminSession( adminId=10, uuid=ZaVLaK,localDatetime=2022-10-01 12:29:52.376508)
   
E-R Diagram Of Bus Application
Bus Reservation System Portal ER Diagram

Swagger UI


User and User Login Controller


Admin and Admin Login Controller


Bus Controller


Reservation Controller


Route Controller


Feedback Controller


THANK YOU EVERYONE FOR VISITING OUR PROJECT
