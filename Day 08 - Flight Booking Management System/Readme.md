# 🛫 Day 8: Flight Booking Management System
## 💡 Task Overview:
In this project, you will build a Flight Booking Management System with the following features:

## Admin Features:
Add new flights ✈️
View passenger details 👤
## Passenger Features:
Book a flight 🛬
Check available flights 📅
This system makes use of OOP in Python to model flights, passengers, and admin roles.

## 🛠️ Steps and Instructions:
### 📂 Import Required Modules:

You will need modules like datetime and os to manage flight schedules and file operations.
### 🔑 Admin Class:

The Admin class manages administrative functions:
Add a Flight: Admin can add new flights by providing details like flight number, source, destination, date, and available seats.
View Passengers: Admin can view a list of passengers who have booked flights, along with their details.
No authentication is added at this stage, but it can be extended with a login system if needed.
### ✈️ Passenger Class:

The Passenger class handles passenger functions:
Book a Flight: Passengers can select from available flights and book seats by providing their name, contact number, and number of seats required.
View Available Flights: Passengers can check which flights are available along with seat availability, date, and time.
### 🗂️ Flight Class:

The Flight class holds all details related to a flight:
Flight Number
Source and Destination
Flight Date and Time
Available Seats
### 🔄 Main Menu:

Upon running the program, the user is presented with the Main Menu:
Admin Mode: Accessible to admins for adding flights and checking passenger information.
Passenger Mode: Accessible to passengers for booking flights and checking flight availability.
Exit: Exit the system.
### 💾 File Management:

Use file handling to store flight and passenger information persistently, so that data is available between sessions.
### ✅ Task Checklist:
 Implement the Admin class with options to add flights and view passengers 🔧.
 Implement the Passenger class to book flights and view available flights 👥.
 Store flight and passenger information using file handling 💾.
 Handle input validation and exceptions where necessary 🚨.
### 📤 Submission:
Ensure that the program is fully functional with no errors.
Submit your completed notebook, ensuring that each class and function is well-documented with comments.
Test the system by running through all the functionalities (Admin and Passenger).
