# Airbnb Clone Project

## About the Project
The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.

## Learning Objectives
By completing this project, learners will:
- Master collaborative team workflows using GitHub.
- Deepen understanding of backend architecture and database design principles.
- Implement advanced security measures for API development.
- Gain proficiency in designing and managing CI/CD pipelines for efficient deployment.
- Strengthen ability to document and plan complex software projects effectively.
- Develop understanding of integrating technologies like Django, MySQL, and GraphQL in a unified ecosystem.

## Requirements
- GitHub account to create and manage repositories.
- Familiarity with Markdown syntax for README.md file creation.
- Prior experience with backend frameworks like Django and database systems such as MySQL.
- Understanding of software development lifecycle practices, including security, CI/CD, and database design.
- Comfort with modern tools such as Docker, GitHub Actions, or similar CI/CD platforms.

## Key Highlights
- **Hands-on GitHub Repository Management:** Initialize and structure a project repository following industry best practices.
- **Team Role Documentation:** Understand and articulate responsibilities of team members for effective collaboration.
- **Technology Stack Breakdown:** Explore the technologies used in a scalable project and their role in achieving project goals.
- **Database Design Proficiency:** Plan and document a relational database structure with entities, attributes, and relationships.
- **Feature-Driven Development:** Identify and describe core features of the application, focusing on user experience and business logic.
- **API Security Fundamentals:** Implement key security measures to safeguard application data.
- **CI/CD Pipeline Integration:** Gain insights into setting up automated development pipelines for efficient deployment.

## Technology Stack
- **Backend Framework:** Django  
- **Database:** MySQL / PostgreSQL  
- **API:** Django REST Framework, GraphQL  
- **Containerization:** Docker  
- **CI/CD:** GitHub Actions / Jenkins  
- **Version Control:** Git / GitHub 
## Database Design

The Airbnb Clone project requires the following key entities:

### 1. Users
**Fields:** 
- id (Primary Key)  
- name  
- email  
- password  
- date_joined  

**Relationships:**  
- A user can create multiple properties.  
- A user can have multiple bookings.  
- A user can leave multiple reviews.  

---

### 2. Properties
**Fields:**  
- id (Primary Key)  
- title  
- description  
- price_per_night  
- owner_id (Foreign Key → Users.id)  

**Relationships:**  
- Each property belongs to a single user (owner).  
- A property can have multiple bookings.  
- A property can have multiple reviews.  

---

### 3. Bookings
**Fields:**  
- id (Primary Key)  
- user_id (Foreign Key → Users.id)  
- property_id (Foreign Key → Properties.id)  
- start_date  
- end_date  

**Relationships:**  
- Each booking belongs to one user.  
- Each booking is for one property.  

---

### 4. Reviews
**Fields:**  
- id (Primary Key)  
- user_id (Foreign Key → Users.id)  
- property_id (Foreign Key → Properties.id)  
- rating  
- comment  

**Relationships:**  
- Each review is written by a user.  
- Each review is for a specific property.  

---

### 5. Payments
**Fields:**  
- id (Primary Key)  
- booking_id (Foreign Key → Bookings.id)  
- amount  
- payment_date  
- status  

**Relationships:**  
- Each payment is linked to a booking.  
- A booking can have one payment.  

## Team Roles

### Backend Developer
Responsible for implementing API endpoints, business logic, and handling server-side functionality. Ensures that data flows correctly between the database and frontend.

### Database Administrator (DBA)
Designs, implements, and maintains the database. Ensures data integrity, performance optimization, and proper indexing for efficient queries.

### DevOps Engineer
Handles deployment, CI/CD pipelines, server configuration, monitoring, and scaling of backend services.

### QA Engineer
Tests all functionalities of the backend to ensure quality, identifies bugs, and verifies that fixes are effective.

### Project Manager (Optional)
Oversees the project timeline, coordinates team members, and ensures milestones are met. 
