# 🏡 Airbnb Clone Project

A full-stack Airbnb clone where users can list, book, and manage properties.  
Features include authentication, image uploads, booking management, and a responsive UI.  
Built to demonstrate proficiency in full-stack development, database design, and REST API integration.

---

## 🚀 Features
- 🔐 User authentication and authorization (JWT/OAuth)
- 🏠 Property listings with image uploads
- 📅 Booking and reservation management
- 💬 Reviews and ratings
- 📱 Responsive and modern UI design
- 🌐 Deployed on AWS/Vercel/Render

---
## 🧰 Technology Stack

Below is an overview of the technologies used in the **Airbnb Clone Project**, along with their purpose and role within the system architecture.

### 🐍 Django
A high-level Python web framework used to build secure and scalable backend services.  
- Provides structure for handling requests, routing, and responses.  
- Simplifies development with built-in authentication, ORM, and admin panel.  
- Used to create RESTful APIs for managing listings, users, and bookings.

### 🗄️ PostgreSQL
A robust, open-source relational database used for storing structured data.  
- Stores user accounts, property details, and booking records.  
- Ensures data integrity and supports complex queries efficiently.  
- Integrates seamlessly with Django through its ORM.

### ⚙️ GraphQL
An API query language that enables flexible data retrieval.  
- Allows clients to request only the data they need.  
- Reduces over-fetching and under-fetching of data.  
- Simplifies communication between frontend and backend.

### 🖥️ React.js
A JavaScript library for building interactive and responsive user interfaces.  
- Powers the frontend for users to browse, book, and manage listings.  
- Connects to backend APIs to display real-time data.  
- Enhances UX through reusable components and dynamic rendering.

### 🎨 Tailwind CSS
A utility-first CSS framework used to design responsive and modern layouts.  
- Provides pre-defined styling utilities to build clean, consistent UI.  
- Accelerates design workflow and ensures mobile responsiveness.  

### ☁️ AWS (Amazon Web Services)
Used for hosting, deployment, and cloud storage.  
- Hosts both backend and frontend for global accessibility.  
- Provides secure, scalable infrastructure and data storage solutions.  
- Ensures reliability and performance for live users.

### 🧪 Postman
A tool for API development and testing.  
- Used to test API endpoints, verify responses, and debug issues.  
- Ensures that backend services work as expected before frontend integration.

## 🔒 API Security

Security is a critical part of the **Airbnb Clone Project** to ensure that user data, transactions, and platform operations remain safe and trustworthy.  
The project integrates multiple layers of protection across authentication, authorization, and data management.

---

### 🔐 Authentication
Implements **JWT (JSON Web Tokens)** to verify user identity and secure API access.  
- Ensures that only registered users can log in and interact with protected endpoints.  
- Prevents unauthorized access and session hijacking.  
**Why it matters:** Protects user accounts and personal information from being compromised.

---

### 🧩 Authorization
Defines user roles (e.g., guest, host, admin) with specific access permissions.  
- Hosts can manage their properties; guests can book; admins oversee the system.  
- Enforces role-based access control (RBAC) to prevent privilege escalation.  
**Why it matters:** Maintains data integrity and ensures users can only perform allowed actions.

---

### 🚫 Rate Limiting
Applies rate limiting on API requests to prevent abuse and denial-of-service (DoS) attacks.  
- Restricts the number of requests per user/IP per time interval.  
- Helps maintain system performance and availability.  
**Why it matters:** Protects backend resources and ensures fair use for all users.

---

### 🔑 Data Encryption
All sensitive data (e.g., passwords, payment information) is encrypted using secure algorithms.  
- Passwords are hashed using **bcrypt** or similar methods.  
- Communication between client and server uses **HTTPS/TLS** encryption.  
**Why it matters:** Prevents data leaks, man-in-the-middle attacks, and identity theft.

---

### 🧱 Input Validation & Sanitization
All incoming data is validated and sanitized before being processed.  
- Prevents common vulnerabilities such as SQL Injection and Cross-Site Scripting (XSS).  
**Why it matters:** Ensures data integrity and prevents malicious payloads from compromising the system.

---

### 💳 Payment Security
Integrates trusted payment gateways (e.g., Stripe, PayPal, or M-Pesa API).  
- Tokens are used instead of storing card details locally.  
- Follows PCI-DSS compliance standards.  
**Why it matters:** Protects financial transactions and user trust.

---

### 🧠 Logging & Monitoring
Maintains detailed logs of user actions, authentication attempts, and system errors.  
- Supports audit trails and early detection of suspicious activity.  
**Why it matters:** Helps in tracking incidents and maintaining accountability.

---

---

## ⚙️ Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/airbnb-clone.git
   cd airbnb-clone
## 👥 Team Roles

Below are the key roles and their responsibilities in the Airbnb Clone Project.  
These roles reflect a collaborative software development team structure inspired by industry practices (as outlined by ITRex Group).

### 🧑‍💻 Backend Developer
Responsible for building and maintaining the server-side logic of the application.  
- Designs and implements RESTful APIs  
- Manages authentication, authorization, and data validation  
- Integrates with databases and external services  
- Ensures scalability, performance, and security

### 🗄️ Database Administrator (DBA)
Manages data integrity, performance, and reliability.  
- Designs the database schema  
- Optimizes queries and handles migrations  
- Monitors database performance and backup routines  
- Ensures data consistency and availability

### 🎨 Frontend Developer
Creates intuitive, responsive, and accessible user interfaces.  
- Implements designs using modern frameworks (React, Next.js, etc.)  
- Connects the frontend to backend APIs  
- Ensures responsive and cross-browser compatibility  
- Focuses on user experience (UX) and usability

### 🧠 Project Manager
Oversees planning, coordination, and timely delivery of project milestones.  
- Defines scope, goals, and timelines  
- Facilitates communication among team members  
- Manages version control, issues, and sprint reviews  
- Ensures that project objectives align with stakeholder requirements

### 🧪 QA Engineer (Tester)
Ensures the product meets quality standards before deployment.  
- Creates and runs test cases (unit, integration, end-to-end)  
- Identifies and documents bugs  
- Works closely with developers to resolve issues  
- Verifies that new features do not break existing functionality

### ☁️ DevOps Engineer
Automates and maintains deployment pipelines and infrastructure.  
- Manages CI/CD workflows  
- Handles deployment environments (AWS, Render, Vercel)  
- Monitors app performance and logs  
- Ensures high availability and system reliability
- 


## 🗄️ Database Design

The **Airbnb Clone Project** database is designed to manage users, properties, bookings, reviews, and payments.  
It follows a relational structure where entities are linked through primary and foreign keys to ensure data consistency and integrity.

---

### 🧑‍💻 Users
Represents all registered users — both hosts and guests.

**Key Fields:**
- `user_id` (Primary Key)
- `full_name`
- `email`
- `password_hash`
- `role` (e.g., host, guest)

**Relationships:**
- A user **can list multiple properties**.
- A user **can make multiple bookings**.
- A user **can write reviews** for properties they booked.

---

### 🏠 Properties
Represents all listed accommodations available for booking.

**Key Fields:**
- `property_id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `title`
- `description`
- `location`
- `price_per_night`

**Relationships:**
- A property **belongs to one user (host)**.
- A property **can have many bookings**.
- A property **can receive multiple reviews**.

---

### 📅 Bookings
Tracks reservations made by guests for specific properties.

**Key Fields:**
- `booking_id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `check_in_date`
- `check_out_date`
- `total_price`
- `status` (e.g., confirmed, cancelled, completed)

**Relationships:**
- A booking **belongs to one property**.
- A booking **is made by one user (guest)**.

---

### 💬 Reviews
Stores feedback and ratings from users after their stay.

**Key Fields:**
- `review_id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `rating` (1–5)
- `comment`
- `created_at`

**Relationships:**
- A review **belongs to one user**.
- A review **is associated with one property**.

---

### 💳 Payments
Handles payment information for completed bookings.

**Key Fields:**
- `payment_id` (Primary Key)
- `booking_id` (Foreign Key → Bookings)
- `amount`
- `payment_method` (e.g., credit card, PayPal)
- `payment_status` (e.g., successful, failed)
- `transaction_date`

**Relationships:**
- A payment **is linked to one booking**.
- A booking **has one corresponding payment**.

---

### 🔗 Entity Relationships Summary
- **User ⇄ Property:** One-to-Many (a host can list many properties)  
- **Property ⇄ Booking:** One-to-Many (a property can have many bookings)  
- **User ⇄ Booking:** One-to-Many (a user can make many bookings)  
- **Property ⇄ Review:** One-to-Many (a property can have many reviews)  
- **Booking ⇄ Payment:** One-to-One (each booking has one payment)

## ✨ Feature Breakdown

The **Airbnb Clone Project** includes a collection of core features designed to simulate real-world property rental functionality.  
Each feature contributes to providing a seamless, user-friendly, and scalable booking experience.

---

### 👤 User Management
Allows users to register, log in, and manage their profiles securely.  
Includes authentication and authorization (via JWT or OAuth) to differentiate between hosts and guests, ensuring data privacy and secure access control.

---

### 🏠 Property Management
Hosts can list new properties with images, descriptions, prices, and availability details.  
This feature enables property owners to edit or remove listings and view booking histories for better management and control.

---

### 📅 Booking System
Enables guests to browse available properties, select dates, and make reservations.  
It includes features like availability validation, price calculation, and automatic booking confirmations to provide a smooth and reliable booking experience.

---

### 💬 Review and Rating System
Allows guests to leave feedback and rate properties after their stay.  
This feature builds trust between users, improves listing quality, and enhances the overall transparency of the platform.

---

### 💳 Payment Integration
Handles secure transactions for property bookings.  
Supports different payment methods (e.g., card, PayPal, M-Pesa) and provides payment status updates to ensure reliability and confidence for both hosts and guests.

---

### 🔍 Advanced Search and Filtering
Lets users search for properties based on location, price, property type, and availability.  
Enhances usability by helping guests find listings that match their preferences quickly and efficiently.

---

### 📱 Responsive User Interface
Ensures a consistent and engaging experience across desktop, tablet, and mobile devices.  
Built with React.js (and Tailwind CSS) to deliver fast, interactive pages and intuitive navigation.

---

### ⚙️ Admin Dashboard *(optional enhancement)*
Provides administrators with insights into platform performance, user activity, and reported issues.  
Supports moderation, analytics, and maintenance tasks to keep the system running efficiently.

---

