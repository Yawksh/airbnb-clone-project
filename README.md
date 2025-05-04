# 📌 Airbnb Clone Project
Welcome to the Airbnb Clone Backend Project – a simplified replica of the real Airbnb platform, focused on backend development. This project simulates building a full-scale booking platform that supports user registration, property listings, booking, and payment processing.

### 🎯 Project Goals
Build a scalable and secure backend system using Django.

Design and manage relational databases with Postgesql.

Integrate GraphQL for efficient data fetching.

Implement CI/CD pipelines for streamlined deployments.

Focus on modularity, documentation, and team collaboration.

## 🧑‍💻 Team Roles
### Role	Responsibility
Backend Developer 	Designs and implements RESTful and GraphQL APIs using Django. Manages application logic and handles integrations.
Database Administrator (DBA)	 Designs the MySQL schema, optimizes queries, and ensures data consistency and integrity.
DevOps Engineer      	Sets up Docker, CI/CD pipelines using GitHub Actions, and manages deployments.
Security Engineer	   Implements authentication, authorization, and protection mechanisms like rate limiting, input validation, and token handling.
Documentation Lead   	Maintains README.md, API docs, database schemas, and records team decisions.


## 🛠️ Technology Stack                                           Technology	Purpose
Django	                                                Backend web framework used to create APIs, handle business logic, and manage ORM.
postgresql                                             	Relational database to store users, bookings, properties, and reviews.
GraphQL                                               	Query language for APIs that allows clients to request only the data they need.
Docker                                                	Containerizes the app to ensure consistency across development and production environments.
GitHub Actions                                        	Automates testing, building, and deployment tasks through CI/CD workflows.
JWT                                                     (JSON Web Tokens)	Manages authentication and session handling securely.



## 🧩 Database Design
### 🔑 Key Entities & Attributes
#### Users
id (Primary Key)
name
email
password_hash
is_host

#### Properties
id (Primary Key)
host_id (Foreign Key to Users)
title
location
price_per_night
#### Bookings

id (Primary Key)
property_id (Foreign Key to Properties)
user_id (Foreign Key to Users)
start_date
end_date

#### Reviews

id (Primary Key)
user_id
property_id
rating
comment
#### Payments

id (Primary Key)
booking_id
amount
payment_method
status

## 🚀 Feature Breakdown
### Feature	                                                         Description 
User Management	                                            Handles user registration, login, logout, and profile management. Guests and hosts have different privileges.
Property Management                                        	Hosts can list properties with details like price, location, and availability.
Booking System	                                            Allows users to book available properties for a specific date range and view booking history.
Review System	                                             Guests can leave reviews after their stay; ratings affect property visibility.
Payment System	                                           Simulates a payment process and records the status of transactions.
Search & Filtering	                                       Users can search properties by location, price range, and ratings.
Admin Panel (Optional)	                                   Admins can oversee users, properties, and reported listings.

## 🔐 API Security
### Key Security Measures:
JWT Authentication:  Ensures that only logged-in users access secured routes.

Role-Based Access Control:  Hosts can manage listings; guests can book and review.

Rate Limiting:   Prevents brute-force attacks on login or signup endpoints.

Data Validation:  Input is sanitized and validated to prevent injection attacks.

HTTPS (on deployment):   Ensures data-in-transit is encrypted.
 ## 🔄 CI/CD Pipeline
###  What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It automates the process of building, testing, and deploying code changes. This ensures bugs are caught early and deployment is consistent.

### Tools:
GitHub Actions — Automates testing and deployment pipelines.

Docker — Containers make the environment predictable.
