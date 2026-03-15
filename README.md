# Credit Score Analysis Tool

## Overview

The **Credit Score Analysis Tool** is a microservices-based backend application designed to evaluate and manage customer credit scores.
The system analyzes financial attributes such as income, credit history, and loan information to determine a customer's creditworthiness.

The application is built using **Java and Spring Boot** and follows a **microservices architecture** with an API Gateway for routing requests between services.

This project demonstrates how modern backend systems used in banking and financial institutions are designed using **Spring Cloud components, REST APIs, and distributed services**.

---

## Problem Statement

Financial institutions need a reliable system to analyze customer credit profiles and determine eligibility for loans or financial services.
This project simulates a simplified credit evaluation platform that manages user data and computes credit scores based on financial parameters.

---

## Architecture

The application follows a **microservices architecture** where each service is responsible for a specific functionality.

Client requests pass through the **API Gateway**, which routes them to the appropriate microservice.

Architecture Flow:

Client → API Gateway → Microservices → Database

Services communicate using REST APIs.

---

## Microservices

### 1. Cloud Gateway

The **API Gateway** acts as the single entry point for all client requests.

Responsibilities:

* Routes incoming requests to appropriate microservices
* Centralizes API access
* Enables future integration of security, logging, and rate limiting

---

### 2. User Management Service (userms)

This service manages all customer-related data.

Responsibilities:

* Register new users
* Retrieve user information
* Maintain user profiles
* Provide user data to other services

---

### 3. Credit Score Service (credit)

The credit service calculates and analyzes customer credit scores.

Responsibilities:

* Evaluate credit scores
* Analyze financial parameters
* Determine credit risk levels
* Provide credit score insights

---

## Technology Stack

Backend

* Java
* Spring Boot
* Spring MVC
* Spring Data JPA

Microservices

* Spring Cloud Gateway

Database

* MySQL / H2 (depending on configuration)

Build Tool

* Maven

---

## Key Features

* Microservices-based architecture
* API Gateway for centralized request routing
* RESTful API design
* Layered architecture (Controller, Service, Repository)
* Credit score calculation logic
* Scalable backend design

---

## Project Structure

```
CreditScoreAnalysisTool
│
├── cloudgateway
│   └── API Gateway Service
│
├── userms
│   └── User Management Microservice
│
├── credit
│   └── Credit Score Analysis Microservice
│
└── README.md
```

---

## How to Run the Project

1. Clone the repository

```
git clone https://github.com/faizanGeek/CreditScoreAnalysisTool.git
```

2. Navigate to each microservice

```
cd cloudgateway
cd userms
cd credit
```

3. Build the project

```
mvn clean install
```

4. Run each service

```
mvn spring-boot:run
```

---

## API Flow Example

Example request to calculate credit score:

POST /credit/score

Request Flow:

Client → Gateway → Credit Service → Database → Response

---

## Future Improvements

* Implement JWT-based authentication
* Add service discovery using Eureka
* Introduce Kafka for event-driven communication
* Implement circuit breakers using Resilience4j
* Add centralized logging and monitoring
* Containerize services using Docker

---

## Learning Objectives

This project demonstrates:

* Microservices architecture design
* Spring Boot REST API development
* API Gateway implementation
* Service-to-service communication
* Backend system design for financial applications

---

## Author

Shekhar Reddy Alugubelli
