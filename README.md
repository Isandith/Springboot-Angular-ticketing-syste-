# Ticket Booking System

A multi-threaded ticket booking application built with Spring Boot backend and Angular frontend. This system allows vendors to release tickets and customers to purchase them in real-time.

## System Requirements

### Backend Requirements
- Java 8 or later
- Maven or Gradle
- MySQL/PostgreSQL (or your preferred database)
- Spring Boot
- Google Gson library (included)

### Frontend Requirements
- Node.js (Latest LTS version)
- npm (comes with Node.js)
- Angular CLI
- Modern web browser

## Installation Guide

### Backend Setup (Spring Boot)

1. **Clone the Repository**
   ```bash
   git clone [repository-url]
   cd ticket-booking-system/backend
   ```

2. **Configure Database**
   - Open `src/main/resources/application.properties`
   - Update database credentials:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/ticket_db
     spring.datasource.username=your_username
     spring.datasource.password=your_password
     ```

3. **Install Dependencies**
   ```bash
   mvn install
   ```

4. **Run Backend**
   ```bash
   mvn spring-boot:run
   ```
   Backend will start on `http://localhost:9090`

