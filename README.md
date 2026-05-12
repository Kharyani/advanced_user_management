Advanced SQLite-Based User Management System
Project Overview

The Advanced SQLite-Based User Management System is a Python CLI application designed to simulate a secure real-world backend authentication and user management system. The project allows users to register, log in, manage profiles, and perform CRUD operations using an SQLite database.

The system also includes an Admin Panel with role-based access control (RBAC) for managing users efficiently.

This project demonstrates backend development concepts including authentication, database integration, password security, CRUD operations, and role-based authorization.

Features
User Features
User Registration
Secure Login Authentication
Password Hashing using SHA-256
View Profile
Update Profile
Delete Account
Session-like Logged-in User Tracking
Admin Features
View All Users
Search Users by Username or Email
Delete Any User
Role-Based Access Control (RBAC)
Security Features
SQLite Parameterized Queries
Password Hashing
Exception Handling
SQL Injection Prevention
Technologies Used
Python 3
SQLite3
hashlib
csv
datetime
colorama (optional)
tabulate (optional)
Project Structure
advanced_user_management/
│
├── main.py
├── database.py
├── auth.py
├── admin.py
├── utils.py
├── users.db
├── README.md
├── requirements.txt
└── exports/
    └── users.csv
Database Schema
Users Table
Field Name	Data Type
id	INTEGER PRIMARY KEY AUTOINCREMENT
username	TEXT UNIQUE
email	TEXT UNIQUE
password	TEXT
phone	TEXT
role	TEXT
created_at	TIMESTAMP
Installation Guide
Step 1: Clone Repository
git clone https://github.com/your-username/advanced-sqlite-user-management-system.git
Step 2: Open Project Folder
cd advanced-sqlite-user-management-system
Step 3: Install Required Libraries
pip install colorama tabulate
How to Run

Run the application using:

python main.py
Main Menu
1. Register
2. Login
3. Exit
User Dashboard
1. View Profile
2. Update Profile
3. Delete Account
4. Logout
Admin Panel
1. View All Users
2. Search User
3. Delete User
4. Back
Password Security

Passwords are securely stored using SHA-256 hashing.

Example:

import hashlib

def hash_password(password):
    return hashlib.sha256(password.encode()).hexdigest()
SQL Injection Prevention

The system uses parameterized queries to prevent SQL injection attacks.

Example:

cursor.execute(
    "SELECT * FROM users WHERE email=?",
    (email,)
)
CRUD Operations

The project supports complete CRUD operations:

Create User
Read User Profile
Update User Information
Delete User Account
Role-Based Access Control (RBAC)

Users are assigned roles:

User
Admin

Only Admin users can access the Admin Panel.

Future Improvements
Forgot Password System
Login Attempt Limit
GUI Version using Tkinter
Email Verification
Activity Logs
CSV Export Feature
Advanced Password Validation
Learning Outcomes

This project helped in understanding:

Python Database Connectivity
Authentication Systems
SQLite Database Management
Password Security
CRUD Operations
Role-Based Authorization
Backend Application Development

Author
Kashish Haryani

License

This project is created for educational and internship purposes.
