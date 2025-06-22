Team Roles
Role	Description
Frontend Developer	Builds the user interface using React (or similar), ensuring a responsive and intuitive experience.
Backend Developer	Develops the server-side logic using Django, builds RESTful APIs, and integrates with the database.
Database Administrator (DBA)	Designs and maintains the PostgreSQL database schema and ensures data integrity and performance.
DevOps Engineer	Manages deployment, CI/CD pipelines, and infrastructure using tools like Docker and GitHub Actions.
UI/UX Designer	Designs wireframes and user flows to enhance usability and ensure consistency across the application.
QA Engineer	Creates and executes test plans to ensure software quality and functionality across all components.

Reference: ITRexGroup - Software Development Team Roles

🧰 Technology Stack
Technology	Purpose
Django	Web framework used to build the backend and expose RESTful APIs efficiently.
PostgreSQL	Relational database system used to store structured data like users, bookings, and payments.
GraphQL (optional)	Alternative API query language used for flexible data fetching, especially for complex UIs.
React.js	JavaScript library used for building the user-facing part of the web app.
Tailwind CSS	Utility-first CSS framework for rapid UI styling.
Docker	Containerization tool used to ensure consistent development and production environments.
GitHub Actions	Automates testing and deployment workflows in the CI/CD pipeline.

🗄️ Database Design
Entities and Fields
User

id

name

email

password_hash

user_type (guest or host)

Property

id

user_id (host)

title

description

location

Booking

id

user_id (guest)

property_id

start_date

end_date

Review

id

user_id

property_id

rating

comment

Payment

id

booking_id

amount

payment_date

status

Relationships
A User can create many Properties.

A User can make many Bookings.

A Booking belongs to one Property and one User.

A Review is associated with both a User and a Property.

A Payment is linked to a Booking.

🚀 Feature Breakdown
Feature	Description
User Management	Allows registration, login, and profile management for both guests and hosts.
Property Management	Enables hosts to list, edit, and remove rental properties with details and images.
Booking System	Allows guests to check availability, book properties, and manage their bookings.
Review System	Guests can leave reviews for properties after stays; helps build trust and transparency.
Payment Integration	Handles secure processing of payments for bookings using payment gateways like Stripe.
Search and Filtering	Lets users find properties based on location, availability, price, and features.

🔒 API Security
Security Measure	Importance
Authentication	Ensures that only registered users can access specific parts of the system (e.g., JWT tokens).
Authorization	Controls access rights, ensuring that only hosts can edit their own properties, etc.
Rate Limiting	Prevents abuse and brute-force attacks by limiting the number of API requests per user/IP.
Input Validation	Protects against SQL injection and XSS by validating incoming data.
HTTPS Enforcement	Ensures encrypted communication between clients and the server to protect sensitive data.

Security is crucial for protecting user data, securing payment details, and maintaining trust in the platform.

⚙️ CI/CD Pipeline
What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It automates the building, testing, and deployment of the application, allowing faster and more reliable updates.

Tools Used
GitHub Actions: Automates tasks like running tests and deploying after code is pushed.

Docker: Packages the app into containers, making it portable and easier to deploy across environments.

