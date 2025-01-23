# Electricity Billing System

A **Java Swing**-based GUI application designed to manage and automate electricity billing tasks. This project provides users with an intuitive interface to perform various operations, such as adding customers, calculating bills, and generating detailed invoices.

---

## Key Features:

1. **User Authentication**:
   - Secure login system to ensure data privacy.
   - Each user can create their personal account for access.

2. **Customer Management**:
   - Add and store customer details including address, phone number, and meter information.
   - View and update customer information.

3. **Electricity Bill Calculation**:
   - Automatically calculate bills based on units consumed.
   - Includes additional charges like GST, meter rent, and service rent.

4. **Bill Payment**:
   - Users can record bill payments seamlessly within the system.

5. **Bill Generation**:
   - Generate detailed and professional electricity bills.
   - Includes customer and billing details for reference.

---

## About the Project:

This project is a **desktop-based application** built using **Java Swing** for the GUI and **MySQL** for the database. The application is designed with multiple modules to handle specific functionalities, ensuring a clean and maintainable codebase.

### Tools and Technologies Used:
- **Java**: Core logic and GUI development.
- **Java Swing**: For creating the graphical user interface.
- **JDBC**: For database connectivity between the application and MySQL.
- **MySQL**: Database to store and manage user, customer, and billing data.
- **IntelliJ IDEA**: IDE used for development.

### Modular Design:
The project consists of **9 interdependent classes** that provide modularity and improve the user experience:
1. **Splash Screen Class**: Displays the application loading animation.
2. **Login Screen Class**: Secure login system with user authentication.
3. **Main System Class**: Central dashboard for accessing all system functionalities.
4. **Add Customer Class**: Allows users to register new customers in the database.
5. **Pay Bill Class**: Handles bill payment operations.
6. **Generate Bill Class**: Generates detailed electricity bills for customers.
7. **Show Details Class**: Displays customer and billing information.
8. **Last Bill Class**: Retrieves and displays the last generated bill for a customer.
9. **Connection Setup Class**: Manages the connection between the application and MySQL database using JDBC.

---

## Database Design (MySQL):

The MySQL database for this application is well-structured and consists of 4 tables:

1. **Login Table**:
   - Stores user login credentials.
   - Columns: `UserName`, `Password`.

2. **Bill Table**:
   - Keeps track of customer bills.
   - Columns: `MeterNumber`, `Units`, `Month`, `Amount`.

3. **Emp Table**:
   - Stores customer details.
   - Columns: `Name`, `MeterNumber`, `Address`, `State`, `City`, `Email`, `Phone`.

4. **Tax Table**:
   - Stores additional charges and tax information.
   - Columns: `MeterLocation`, `MeterType`, `PhaseCode`, `BillType`, `Days`, `MeterRent`, `MCB_Rent`, `ServiceRent`, `GST`.

### Database Communication:
The project utilizes **JDBC (Java Database Connectivity)** to interact with the MySQL database. JDBC enables secure and efficient handling of data between the application and the database.

---

## Screenshots:

Here are some screenshots to give you a glimpse of the application:

### 1. Login Screen:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/Login.JPG" width="400" height="300">

---

### 2. Main Page:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/Main.JPG" width="600" height="500">

---

### 3. Add Customer:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/AddC.JPG" width="500" height="500">

---

### 4. Calculate Bill:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/CalculateBill.JPG" width="500" height="500">

---

### 5. Customer Details:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/Details.JPG" width="800" height="300">

---

### 6. Generate Bill:
<img src="https://github.com/DJay2012/Electricity_Bill_System/ScreenShots/GenerateBill.JPG" width="400" height="700">

---

## How to Set Up and Run the Project:

### Prerequisites:
1. Install **Java JDK 8 or higher**.
2. Install a local MySQL server (e.g., MySQL Workbench or XAMPP).
3. Add a JDBC library (e.g., `mysql-connector-java-x.x.x.jar`) to the project's build path.

### Steps to Run:
1. **Clone the Repository**:
   Download or clone this repository to your local machine.

2. **Setup the Database**:
   - Open your MySQL management tool.
   - Create the required tables (`Login`, `Bill`, `Emp`, `Tax`) as described in the database section.
   - Import any provided SQL dump file (if available).

3. **Configure JDBC**:
   - Update the database connection details in the **Connection Setup Class**:
     ```java
     String url = "jdbc:mysql://localhost:3306/YourDatabaseName";
     String username = "YourUsername";
     String password = "YourPassword";
     ```

4. **Compile and Run**:
   - Open the project in **IntelliJ IDEA** or your preferred Java IDE.
   - Add the required `mysql-connector-java` JAR file to the classpath.
   - Compile and run the project.

5. **Login and Use**:
   - Use the default credentials or create new ones for logging in.
   - Explore the features like adding customers, calculating bills, and generating invoices.

---

## Future Enhancements:
1. **Mobile Application**:
   - Build a mobile-friendly version of the billing system for better accessibility.
   
2. **Online Bill Payment**:
   - Integrate payment gateways to enable online bill payments.

3. **Improved UI/UX**:
   - Upgrade the UI to a more modern design using JavaFX or external libraries.

4. **Data Visualization**:
   - Add charts and graphs to analyze bill data and usage trends.

5. **Multi-User Roles**:
   - Add role-based access for Admins, Managers, and Staff.

---

## License:

This project is released under the **MIT License**. You are free to use, modify, and distribute it as per the license terms.

---

## Acknowledgments:

- **JDBC Library** for database connectivity.
- **MySQL** for database management.
- **IntelliJ IDEA** for providing a great development environment.
- Special thanks to everyone who contributed to the testing and development of this application.
