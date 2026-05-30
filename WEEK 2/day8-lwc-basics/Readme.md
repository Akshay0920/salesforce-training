# Day 8 - LWC Basics

## What is LWC?

Lightning Web Components (LWC) is a modern UI framework developed by Salesforce. It is used to build fast, reusable, and interactive user interfaces on the Salesforce platform. LWC uses standard web technologies such as HTML, JavaScript, and CSS, making development easier and more efficient.

## Why Salesforce Uses LWC

Salesforce uses LWC because it provides better performance, faster loading times, and a modern development experience. LWC follows web standards and allows developers to create reusable components that are easy to maintain and scale. It also improves user experience by creating responsive and interactive applications.

# UI Thinking Exercise

For the College Management System, the following UI screens/components are required:

### 1. Student Registration Form
Used for adding new students to the system. It collects information such as name, email, phone number, department, and address.

### 2. Student Dashboard
Displays student details, attendance percentage, enrolled courses, and notifications.

### 3. Course Management Dashboard
Allows administrators to add, update, and manage courses offered by the college.

### 4. Attendance Management Screen
Used by faculty to mark and view student attendance records.

### 5. Faculty Panel
Allows faculty members to manage student records, attendance, assignments, and course information.

# Component Thinking

## Selected Screen: Student Dashboard

The Student Dashboard can be divided into the following reusable components:

### Header Component
Displays the application title, navigation menu, and user profile information.

### Student Information Component
Shows student details such as name, roll number, department, and contact information.

### Attendance Component
Displays attendance percentage and attendance history.

### Course Component
Shows enrolled courses and course-related information.

### Notification Component
Displays important announcements, alerts, and updates.

### Why Reusable Components Are Useful

Reusable components help reduce duplicate code and improve maintainability. A component can be used in multiple screens without rewriting the same code. This saves development time, improves consistency, and makes future updates easier.

# Frontend vs Backend Thinking

| Functionality | Frontend (UI) | Backend (Apex) |
|--------------|--------------|---------------|
| Button Click | Handles user interaction and sends request | Processes requested operation |
| Data Validation | Basic validation such as required fields | Advanced validation and security checks |
| Fee Calculation | Displays calculated fee information | Performs actual fee calculation and business logic |
| Notification Display | Shows notifications to users | Retrieves and manages notification data |
| Form Submission | Collects and sends user input | Stores data in the database |

## Frontend Responsibilities

- Display data to users
- Handle button clicks
- Show notifications and messages
- Perform basic input validation
- Manage page navigation

## Backend Responsibilities

- Process business logic
- Validate and store data
- Calculate fees and attendance statistics
- Handle database operations
- Maintain security and access control

# Reflection

## Why do modern enterprise systems use component-based UI architecture?

Modern enterprise systems use component-based UI architecture because it improves code reusability, maintainability, and scalability. Developers can build small independent components and combine them to create complex applications. This approach reduces development effort, makes testing easier, and allows teams to work on different components independently. It also provides a consistent user experience across the application.

