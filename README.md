# airbnb-clone-project

##  Project Overview
The Airbnb Clone Project is a backend-focused application designed to simulate a booking platform like Airbnb.  
It will help us understand backend development, database design, and API security while building a scalable web application.

## Goals
- Learn GitHub collaboration workflows.
- Practice backend architecture with Django.
- Design and document a relational database using MySQL.
- Implement API security best practices.
- Explore CI/CD automation for deployment.

## Tech Stack
- **Backend Framework**: Django  
- **Database**: MySQL  
- **API**: GraphQL & REST  
- **Containerization**: Docker  
- **CI/CD**: GitHub Actions  
- **Version Control**: Git & GitHub  

---
This repository is part of the StayBackend project for learning modern backend development practices.

## Team Roles

### 1. Project Manager
- **Responsibility:** Oversees the project, manages timelines, coordinates the team, and ensures project goals are met.

### 2. Backend Developer
- **Responsibility:** Develops the server-side logic, APIs, and handles data processing for the application.

### 3. Frontend Developer
- **Responsibility:** Builds the user interface, integrates frontend with backend APIs, and ensures a smooth user experience.

### 4. Database Administrator (DBA)
- **Responsibility:** Designs, manages, and maintains the database. Ensures data integrity, security, and efficient storage.

### 5. QA Engineer / Tester
- **Responsibility:** Tests the application for bugs and issues, writes test cases, and ensures the project meets quality standards.

### 6. DevOps Engineer
- **Responsibility:** Manages deployment, server infrastructure, and automates workflows to ensure continuous integration and delivery.

## Technology Stack

- **Python:** Programming language used for backend logic and data handling.
- **Django:** Web framework for building the backend and RESTful APIs.
- **Flask:** Lightweight web framework (optional, depending on project phase).
- **HTML, CSS, JavaScript:** Frontend technologies for creating user interfaces.
- **PostgreSQL / MySQL:** Relational database for storing and managing application data.
- **Git & GitHub:** Version control system for tracking changes and collaborating.
- **Docker (optional):** Containerization tool for consistent deployment environments.
- **GraphQL (optional):** Query language for APIs (used for fetching specific data efficiently).

##  Database Design

### Key Entities

1. **Users**
   - **Fields:** id, name, email, password, phone_number
   - **Relationships:** A user can have multiple properties and bookings; a user can write multiple reviews.

2. **Properties**
   - **Fields:** id, owner_id, title, description, location, price_per_night
   - **Relationships:** Belongs to a user (owner); can have multiple bookings and reviews.

3. **Bookings**
   - **Fields:** id, user_id, property_id, start_date, end_date, total_price
   - **Relationships:** Belongs to a user; belongs to a property; may have a payment associated.

4. **Reviews**
   - **Fields:** id, user_id, property_id, rating, comment
   - **Relationships:** Written by a user; belongs to a property.

5. **Payments**
   - **Fields:** id, booking_id, amount, payment_date, status
   - **Relationships:** Linked to a booking; ensures payment completion for property bookings.



## Feature Breakdown

### 1. User Management
Allows users to create accounts, log in, and manage their profiles. Users can also view their booking history and write reviews for properties.

### 2. Property Management
Enables property owners to list new properties, update details, and manage availability. Helps ensure accurate and up-to-date property information for potential renters.

### 3. Booking System
Allows users to search for available properties, make bookings, and track upcoming reservations. Ensures smooth coordination between property availability and user requests.

### 4. Payment Processing
Handles payments securely for bookings. Ensures proper tracking of payment status and allows refunds if necessary.

### 5. Review System
Allows users to leave ratings and feedback on properties they have stayed in. Helps maintain transparency and trust within the platform.


## API Security

### Key Security Measures

1. **Authentication**
   - Users must log in with secure credentials (username/password or OAuth tokens).  
   - Ensures only registered users can access the system, protecting personal data.

2. **Authorization**
   - Restricts access based on user roles (e.g., admin, property owner, guest).  
   - Prevents unauthorized users from modifying or viewing sensitive data.

3. **Rate Limiting**
   - Limits the number of API requests a user can make in a given time.  
   - Protects the system from abuse or denial-of-service attacks.

4. **Data Encryption**
   - Sensitive data such as passwords and payment info is encrypted in storage and transit.  
   - Ensures confidentiality and prevents data breaches.

5. **Input Validation**
   - All user input is validated and sanitized before processing.  
   - Protects against injection attacks and maintains system integrity.


##  CI/CD Pipeline

### Overview
CI/CD (Continuous Integration / Continuous Deployment) pipelines automate the process of testing, building, and deploying applications. They ensure that changes to the codebase are quickly and reliably integrated into the project and deployed to production.

### Importance
- **Consistency:** Automates testing and deployment, reducing human error.  
- **Speed:** Accelerates development by allowing faster feedback on code changes.  
- **Quality:** Ensures code is tested before deployment, improving reliability.  

### Tools
- **GitHub Actions:** Automates workflows for testing, building, and deploying code.  
- **Docker:** Packages applications into containers for consistent deployment.  
- **Jenkins / CircleCI (optional):** Can be used as alternative CI/CD tools for automation.

