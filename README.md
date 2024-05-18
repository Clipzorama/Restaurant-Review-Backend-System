# Restaurant Review Backend-System

## Project Overview

Restaurant Review Backend-System is a backend database system for a restaurant service application. It leverages Spring Boot, Spring Data JPA, and Hibernate to manage and persist data related to users, restaurants, reviews, and responses. The application is designed to automate the process of converting data in database tables into Java objects using an object-relational mapping (ORM) system.

## Technologies Used

- **Spring Boot**: Framework for building production-ready applications.
- **Spring Data JPA**: Simplifies data access using the Java Persistence API (JPA) and Hibernate ORM.
- **Hibernate**: An ORM framework that automates the conversion of database data into Java objects.
- **Postman**: Tool for testing API endpoints.
- **SQL**: Database management.

## Project Structure

The project is organized into the following packages:

- `edu.lawrence.reviews.models`: Contains entity classes representing the database tables.
  - `Response.java`
  - `Restaurant.java`
  - `Review.java`
  - `User.java`
- `edu.lawrence.reviews.interfaces`: Contains controller interfaces for handling HTTP requests.
  - `ResponseController.java`
  - `RestaurantController.java`
  - `ReviewController.java`
  - `UserController.java`
- `edu.lawrence.reviews.interfaces.dtos`: Contains Data Transfer Object (DTO) classes.
  - `AvgRating.java`
  - `ResponseDTO.java`
  - `RestaurantDTO.java`
  - `ReviewDTO.java`
  - `UserDTO.java`
- `edu.lawrence.reviews.repositories`: Contains repository interfaces extending Spring Data JPA repositories.
  - `ResponseRepository.java`
  - `RestaurantRepository.java`
  - `ReviewRepository.java`
  - `UserRepository.java`
- `edu.lawrence.reviews.services`: Contains service classes for business logic.
  - `PasswordService.java`
  - `ResponseService.java`
  - `RestaurantService.java`
  - `ReviewService.java`
  - `UserService.java`

## Key Features

- **UUIDs**: Unique identifiers for users, restaurants, reviews, and responses.
- **Repository Abstraction**: Simplified data access using repository interfaces.
- **CRUD Operations**: Basic Create, Read, Update, Delete operations for all entities.
- **Custom Queries**: Supports JPQL and native SQL queries for advanced data retrieval.
- **Password Hashing**: The PasswordService class handles password hashing using the BCrypt library. This ensures that passwords are 	        	stored securely and can be validated safely.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 22 or later
- Maven
- Spring Boot
- PostgreSQL or any preferred SQL database
- Run as SpringBoot App


## Pom.xml dependencies

<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>


## Set up the database in SQL and configure the connection in application.properties:

spring.application.name=reviews
server.port=8085
spring.datasource.url=jdbc:mysql://localhost:3306/reviews
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver


# Testing

Use Postman to test the API endpoints. The controllers are designed to handle CRUD operations for each entity.

# Contribution

Contributions are welcome! Please fork the repository and create a pull request with your changes.
