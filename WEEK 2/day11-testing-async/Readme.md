# Day 11 - Testing and Asynchronous Processing

# Why Testing Matters

Testing helps developers find problems before users face them in the real system.

Benefits of testing:

- Prevents invalid data from entering the system.
- Ensures business rules work correctly.
- Improves reliability and stability.
- Reduces system failures.
- Helps maintain data accuracy.
- Improves user experience.

Without proper testing, enterprise applications can produce incorrect results, lose data, or crash unexpectedly.

# What is Asynchronous Processing?

Asynchronous processing means a task runs in the background instead of making the user wait for it to finish.

Advantages:

- Faster user experience.
- Better performance.
- Handles large volumes of data.
- Reduces waiting time.
- Improves scalability.

Salesforce examples include:

- Future Methods
- Batch Apex
- Queueable Apex
- Scheduled Apex

# Important Test Cases

## 1. Invalid Email Address

**Test:** Enter an invalid email format.

**Prevents:** Storing incorrect contact information and email delivery failures.

## 2. Duplicate Student Registration

**Test:** Register the same student twice.

**Prevents:** Duplicate records and reporting issues.

## 3. Course Seats Exceeding Limit

**Test:** Register students after all seats are filled.

**Prevents:** Overbooking of courses.

## 4. Missing Mandatory Fields

**Test:** Submit registration without required fields.

**Prevents:** Incomplete student records.

## 5. Invalid Attendance Value

**Test:** Enter attendance greater than 100% or less than 0%.

**Prevents:** Incorrect attendance calculations.

## 6. Low Attendance Warning

**Test:** Attendance falls below minimum threshold.

**Prevents:** Missing academic warning notifications.

## 7. Formula Field Verification

**Test:** Check remaining seats calculation.

**Prevents:** Incorrect seat availability display.

## 8. Email Notification Failure

**Test:** Simulate email delivery failure.

**Prevents:** Missing confirmation notifications.

## 9. Unauthorized Access

**Test:** Student attempts to access admin functionality.

**Prevents:** Security and permission issues.

## 10. Bulk Student Registration

**Test:** Register many students at the same time.

**Prevents:** Performance issues and data inconsistencies.

# Async Use Cases

## 1. Bulk Email Sending

Sending hundreds or thousands of emails should happen in the background.

**Reason:** Users should not wait for all emails to be delivered.

## 2. Report Generation

Large reports can take time to generate.

**Reason:** Reports should be prepared in the background while users continue working.

## 3. Large Data Import

Importing thousands of records can take several minutes.

**Reason:** Background processing prevents system slowdown.

## 4. Notifications

Sending alerts to students and faculty.

**Reason:** Notifications do not need immediate user interaction.

## 5. External System Synchronization

Sharing data with external applications.

**Reason:** External systems may respond slowly and should not block users.

# Reliability Discussion

## Student Registration Crash

Possible Problems:

- Student record may not be saved.
- Course allocation may fail.
- Confirmation email may not be sent.

Testing Helps By:

- Verifying successful record creation.
- Checking rollback behavior during failures.
- Ensuring validations work correctly.

## Payment Update Crash

Possible Problems:

- Payment status may remain incorrect.
- Duplicate payment records may occur.
- Financial reports may become inaccurate.

Testing Helps By:

- Verifying payment updates.
- Preventing duplicate transactions.
- Ensuring accurate financial data.

## Attendance Update Crash

Possible Problems:

- Attendance records may be incomplete.
- Warning notifications may not trigger.
- Reports may show incorrect values.

Testing Helps By:

- Validating attendance calculations.
- Verifying notification triggers.
- Ensuring data consistency.

# Architecture Thinking

Enterprise systems need multiple layers working together.

## Frontend

Provides screens and dashboards for users.

Example:

- Student Dashboard
- Faculty Dashboard

## Backend

Processes business logic and validations.

Example:

- Registration eligibility checks
- Attendance calculations

## Database

Stores all application data.

Example:

- Students
- Courses
- Faculty
- Departments

## Automation

Reduces manual work.

Example:

- Auto confirmation emails
- Attendance warnings

## Events

Allow systems to react automatically.

Example:

- Notify faculty when a course becomes full.
- Alert students when attendance is low.

# Reflection

After learning Salesforce, I realized that enterprise applications are much more complex than simple programs.

A system must:

- Handle thousands of users.
- Protect important data.
- Process large amounts of information.
- Continue working even when failures occur.
- Provide accurate results.
- Scale as the organization grows.

Testing ensures correctness.

Scalability ensures performance when many users access the system.

Asynchronous processing improves efficiency by moving heavy tasks to the background.

Together, these concepts help build reliable enterprise software that can support real-world business operations.
