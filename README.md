Ticket Booking System
A multi-threaded ticket booking system with a Spring Boot backend and Angular front-end.

Requirements
Java 8 or later for Spring Boot
Google Gson library for JSON parsing and generation
Node.js and npm for Angular setup
Spring Boot application connected to a database
Backend Setup (Spring Boot)
Clone or Download the Repository.

Install Dependencies: Make sure you have Spring Boot set up and dependencies configured. You can use Maven or Gradle to manage dependencies.

If you're using Maven, run:

bash
Copy code
mvn install
Run the Spring Boot Application:

To run the backend Spring Boot application, use:

bash
Copy code
mvn spring-boot:run
The backend will be accessible at http://localhost:9090.

Database Configuration: Ensure that your database is properly set up and connected. The backend will use the configured database to store and manage ticket data.

Start or Stop: Once the application is running, you can interact with it via the Angular frontend or through REST API calls.

Frontend Setup (Angular)
1. Install Node.js and npm
To install Node.js (which includes npm), follow the instructions on the official website:

Download Node.js
After installation, verify it by running the following commands in your terminal:

bash
Copy code
node -v
npm -v
Both should display the installed version numbers.

2. Install Angular CLI
Once Node.js and npm are installed, install the Angular CLI globally by running:

bash
Copy code
npm install -g @angular/cli
3. Set Up the Angular Frontend
Navigate to the Angular project directory.

bash
Copy code
cd path/to/angular/project
Install required dependencies for the Angular project:

bash
Copy code
npm install
Start the Angular development server:

bash
Copy code
ng serve
This will run the Angular application at http://localhost:4200.

4. Backend and Frontend Integration
Ensure that the Spring Boot backend and Angular frontend are running:

The Spring Boot backend will run on localhost:9090.
The Angular frontend will run on localhost:4200.
You may need to set up CORS in your Spring Boot application to allow the frontend to communicate with the backend. If needed, add a CORS configuration in your backend code.

5. Accessing the System
Once both backend and frontend are running, open a web browser and go to http://localhost:4200 to access the ticket booking system. The Angular frontend will interact with the Spring Boot backend via the API at http://localhost:9090.

Example Output
Backend (Spring Boot):
sql
Copy code
Do you want to START or STOP the program? (Type START or STOP)
START
Vendor released 10 tickets. Available tickets: 10
Customer-1 bought 10 tickets. Available tickets: 0
Total tickets sold: 20
Ticket booking system has completed all operations.
Frontend (Angular):
The frontend will allow users to interact with the system, view available tickets, and simulate purchases. It will connect to the backend for ticket retrieval and display the status in real time.

Troubleshooting
1. Backend Not Starting
Solution: Check for missing dependencies or incorrect database settings. Ensure the database is running and the backend is configured for port 9090.
2. CORS Errors
Solution: Add CORS configuration in Spring Boot. Allow all origins, methods, and headers for cross-origin requests.
3. Database Connection Issues
Solution: Verify database credentials and ensure the database is running.
4. Angular Not Loading
Solution: Run npm install to install dependencies. Check browser console for errors.
5. Tickets Not Available
Solution: Ensure the vendor thread is releasing tickets correctly and the ticket pool logic is working.
6. Invalid Configuration Input
Solution: Enter valid numeric values when prompted. The system will prompt for re-entry if invalid input is detected.
Special Dependencies
The backend uses several important dependencies to enhance functionality:

Gson - For JSON parsing and generation.

xml
Copy code
<dependency>
    <groupId>com.google.code.gson</groupId>
    <artifactId>gson</artifactId>
    <version>2.10.1</version>
</dependency>
Spring Boot CORS Support - For handling cross-origin requests, allowing the frontend to communicate with the backend when they are on different ports.

xml
Copy code
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cors</artifactId>
</dependency>
Hibernate Validator - Provides bean validation support (e.g., @NotNull, @Size annotations).

xml
Copy code
<dependency>
    <groupId>org.hibernate</groupId>
    <artifactId>hibernate-validator</artifactId>
    <version>6.2.0.Final</version>
</dependency>
Spring Boot Security - For implementing authentication and authorization in the system.

xml
Copy code
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
Spring Boot Actuator - Adds production-ready features such as health checks and metrics.

xml
Copy code
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
Lombok - Reduces boilerplate code like getters, setters, and constructors.

xml
Copy code
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <version>1.18.24</version>
    <scope>provided</scope>
</dependency>
These dependencies are essential for making the application more efficient, secure, and easy to manage.
