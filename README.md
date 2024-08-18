# AviaSphere Airline Management System

## Introduction

AviaSphere is a comprehensive Airline Management System designed to streamline and optimize airline operations. This system features functionalities for flight management, passenger handling and booking services. It provides a user-friendly interface for administrators and passengers to manage tasks such as booking and flight tracking efficiently.
   
### Features

- User Registration: Secure user registration.
- Flight Management: Manage flight details and availability.
- Passenger Handling: Record and manage passenger information.
- Add-ons: Customize travel experience with meal preferences and seating options.

## Setup Instructions

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MySQL](https://www.mysql.com/) (v8 or higher)

### Installation 

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Ananya-55/Airline-Management-System.git
   cd Airline-Management-System
   
2. **Installing the dependencies:**
   ```bash
   npm install
   
3. **Setup MySQL Database:**
   
   Create the following tables in your MySQL database:

-  **register**
   ```sql
   CREATE TABLE register (
     email VARCHAR(50) PRIMARY KEY,
     name VARCHAR(20),
     password VARCHAR(15)
   );
- **passenger**
   ```sql
  CREATE TABLE passenger (
  passenger_id INT AUTO_INCREMENT PRIMARY KEY,
  flight_id INT,
  passenger_name VARCHAR(45),
  age VARCHAR(45),
  email VARCHAR(45),
  contact VARCHAR(45),
  address VARCHAR(100)
   );
- **flights**
   ```sql
   CREATE TABLE flights (
  flight_id INT PRIMARY KEY,
  from_location VARCHAR(45),
  to_location VARCHAR(45),
  departure_date DATE,
  arrival_date DATE,
  departure_time VARCHAR(45),
  arrival_time VARCHAR(45),
  total_seats VARCHAR(45)
   );
- **airport**
   ```sql
   CREATE TABLE airport (
  airport_id INT PRIMARY KEY,
  country VARCHAR(45),
  airport_name VARCHAR(45),
  city VARCHAR(45)
  );
- **admin**
   ```sql
   CREATE TABLE admin (
  admin_id INT PRIMARY KEY,
  username VARCHAR(45),
  password VARCHAR(45)
  );
- **addons**
   ```sql
   CREATE TABLE addons (
  seat_preference VARCHAR(45),
  meal_preference VARCHAR(45),
  xl_seatbelt VARCHAR(45),
  child_seatbelt VARCHAR(45)
  );
   
5. **Run the Server:**
   ```bash
   node server.js
   
6. **Access the Application:**
     Open your browser and navigate to http://localhost:3000 to access the AviaSphere Airline Management System.




