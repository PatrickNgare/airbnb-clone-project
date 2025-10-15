# 🏡 Airbnb Clone Project

A full-stack Airbnb clone where users can list, book, and manage properties.  
Features include authentication, image uploads, booking management, and a responsive UI.  
Built to demonstrate proficiency in full-stack development, database design, and REST API integration.

---

## 🚀 Features Overview
- 🔐 User authentication and authorization (JWT/OAuth)
- 🏠 Property listings with image uploads
- 📅 Booking and reservation management
- 💬 Reviews and ratings
- 💳 Payment integration
- 📱 Responsive and modern UI design
- 🌐 Deployed on AWS/Vercel/Render

---

## 🧰 Technology Stack

Below is an overview of the technologies used in the **Airbnb Clone Project**, along with their purpose and role within the system architecture.

### 🐍 Django
A high-level Python web framework used to build secure and scalable backend services.  
Provides structure for routing, authentication, and RESTful APIs.

### 🗄️ PostgreSQL
A robust, open-source relational database used to store structured data such as users, properties, and bookings.  
Ensures data integrity and supports complex relationships.

### ⚙️ GraphQL
A query language that enables flexible and efficient data retrieval, reducing over-fetching and simplifying frontend-backend communication.

### 🖥️ React.js
A JavaScript library for building interactive and responsive user interfaces.  
Connects to backend APIs and delivers dynamic, real-time experiences.

### 🎨 Tailwind CSS
A utility-first CSS framework that ensures consistent, responsive, and modern UI design.

### ☁️ AWS (Amazon Web Services)
Used for hosting, deployment, and cloud storage to ensure scalability, reliability, and global accessibility.

### 🧪 Postman
A testing tool used for API validation and debugging during backend development.

---

## ✨ Feature Breakdown

### 👤 User Management
Secure user registration, login, and profile management.  
Includes authentication and authorization to distinguish between guests and hosts.

### 🏠 Property Management
Hosts can list, edit, and manage their properties with details and images.  
Improves the experience for property owners and enhances platform engagement.

### 📅 Booking System
Allows guests to search, book, and manage reservations with real-time availability validation and total cost calculation.

### 💬 Review and Rating System
Guests can rate and review properties after their stay, improving transparency and helping others make informed choices.

### 💳 Payment Integration
Handles secure payments via trusted gateways like Stripe, PayPal, or M-Pesa.  
Ensures seamless and safe financial transactions.

### 🔍 Advanced Search and Filtering
Enables users to search listings by location, price, and property type.  
Improves usability and helps users find ideal stays quickly.

### 📱 Responsive UI
Fully responsive interface for desktop and mobile devices.  
Built with React and Tailwind for speed and accessibility.

### ⚙️ Admin Dashboard (Optional)
Allows system administrators to manage users, monitor performance, and handle platform reports.

---

## 🗄️ Database Design

### 🧑‍💻 Users
- `user_id`, `full_name`, `email`, `password_hash`, `role`  
Each user can own properties, make bookings, and write reviews.

### 🏠 Properties
- `property_id`, `user_id`, `title`, `description`, `location`, `price_per_night`  
Each property belongs to one host and can have multiple bookings and reviews.

### 📅 Bookings
- `booking_id`, `user_id`, `property_id`, `check_in_date`, `check_out_date`, `total_price`, `status`  
Each booking belongs to one user and one property.

### 💬 Reviews
- `review_id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`  
Each review is tied to one user and one property.

### 💳 Payments
- `payment_id`, `booking_id`, `amount`, `payment_method`, `payment_status`, `transaction_date`  
Each payment corresponds to a specific booking.

**Entity Relationships Summary:**
- User ⇄ Property → One-to-Many  
- User ⇄ Booking → One-to-Many  
- Property ⇄ Booking → One-to-Many  
- Property ⇄ Review → One-to-Many  
- Booking ⇄ Payment → One-to-One

---

## 🔒 API Security

Security ensures safe interactions and data protection across the platform.

### 🔐 Authentication
JWT tokens secure endpoints and protect user sessions.  
**Why:** Prevents unauthorized access and identity theft.

### 🧩 Authorization
Role-based access control ensures users perform only allowed actions.  
**Why:** Preserves data integrity and prevents privilege abuse.

### 🚫 Rate Limiting
Prevents API abuse by limiting requests per IP.  
**Why:** Protects system performance and stability.

### 🔑 Data Encryption
Encrypts passwords and sensitive data using bcrypt & HTTPS/TLS.  
**Why:** Prevents data breaches and eavesdropping.

### 🧱 Input Validation
Sanitizes user input to prevent SQL Injection and XSS.  
**Why:** Protects system from malicious input.

### 💳 Payment Security
Implements token-based payment gateways (Stripe, PayPal, M-Pesa).  
**Why:** Ensures secure and PCI-compliant financial transactions.

### 🧠 Logging & Monitoring
Tracks API activity and user actions for auditing and debugging.  
**Why:** Enhances accountability and system reliability.

---

## ⚙️ CI/CD Pipeline

### 🔁 Continuous Integration (CI)
Automatically tests and validates code on every commit to maintain quality.  
**Benefit:** Detects issues early and ensures team collaboration efficiency.

### 🚀 Continuous Deployment (CD)
Automates deployment to staging or production environments.  
**Benefit:** Reduces downtime and accelerates release cycles.

### 🧰 Tools Used
- **GitHub Actions:** For build, test, and deploy workflows.  
- **Docker:** For containerization and environment consistency.  
- **AWS / Render / Vercel:** For deployment and hosting.  
- **Pytest / Jest / Postman:** For automated testing in CI pipelines.

---

## 👥 Team Roles

### 🧑‍💻 Backend Developer
Builds RESTful APIs, manages authentication, and ensures scalability and security.

### 🎨 Frontend Developer
Implements responsive UI and integrates with backend APIs.

### 🗄️ Database Administrator (DBA)
Designs and maintains the database, ensuring integrity and performance.

### 🧪 QA Engineer
Tests application features, identifies bugs, and verifies code quality.

### 🧠 Project Manager
Oversees planning, coordination, and delivery of milestones.

---

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/airbnb-clone.git
   cd airbnb-clone
