# Day 14 - Flow Governance

# What is Flow Governance?

Flow Governance is the practice of controlling how business processes are executed through approvals, validations, permissions, and automated workflows.

Benefits:

- Improves security
- Prevents unauthorized actions
- Ensures accountability
- Reduces human errors
- Maintains data integrity
- Supports business compliance

---

# Core Tasks

## Task-1: Multi-Level Approval Design

### 1. Course Creation Approval Workflow

#### Scenario
A faculty member wants to create a new course.

### Approval Order

1. Faculty Member submits course proposal
2. Head of Department (HOD) reviews the course
3. Academic Committee validates curriculum
4. Principal/Dean gives final approval

### After Approval

- Course is added to the course catalog
- Students can enroll
- Course becomes visible in the system

### After Rejection

- Course status becomes Rejected
- Feedback is sent to the faculty member
- Faculty can modify and resubmit

---

### 2. Faculty Leave Request Workflow

#### Scenario
A faculty member requests leave.

### Approval Order

1. Faculty submits leave request
2. HOD reviews request
3. HR Department verifies leave balance
4. Principal approves if required

### After Approval

- Leave status becomes Approved
- Attendance records are updated
- Faculty receives confirmation

### After Rejection

- Leave request status becomes Rejected
- Faculty receives rejection reason

---

### 3. Student Scholarship Request Workflow

#### Scenario
A student applies for a scholarship.

### Approval Order

1. Student submits application
2. Scholarship Committee reviews documents
3. Finance Department verifies eligibility
4. Principal approves final request

### After Approval

- Scholarship amount is sanctioned
- Student record is updated
- Notification is sent

### After Rejection

- Application status becomes Rejected
- Student receives explanation

---

### 4. Budget Approval Workflow

#### Scenario
Department requests funds for new equipment.

### Approval Order

1. Department submits budget request
2. HOD approves department need
3. Finance Department verifies availability
4. Principal/Management grants final approval

### After Approval

- Budget is allocated
- Procurement process begins
- Request status becomes Approved

### After Rejection

- Budget request becomes Rejected
- Department receives comments for correction

---

## Task-2: Branching Flow Logic

### Attendance Monitoring Flow

### Decision Point 1

**Is Attendance < 75%?**

If YES:

- Send warning email to student

If NO:

- No action required

---

### Decision Point 2

**Is Attendance < 60%?**

If YES:

- Send notification to parents
- Generate counseling request

If NO:

- Continue monitoring

---

### Decision Point 3

**Is Attendance < 50%?**

If YES:

- Escalate case to administration
- Schedule disciplinary review
- Flag student as high-risk

If NO:

- Continue regular tracking

---

### Flow Diagram

```text
Attendance Check
        |
        V
Attendance < 75% ?
        |
       YES
        |
Send Warning Email
        |
        V
Attendance < 60% ?
        |
       YES
        |
Notify Parents
        |
        V
Attendance < 50% ?
        |
       YES
        |
Admin Escalation
