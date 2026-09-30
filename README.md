# Student Course Management – Relational Schema

## Project Description
This project demonstrates a basic relational database schema for a Student Course Management System. The system stores information about students, courses, and student course registrations.

## Relations
The database contains three relations:
1. STUDENT
2. COURSE
3. ENROLLMENT

## 1. STUDENT Relation
### Attributes
- Student_ID
- Student_Name
- Email
- Department

### Primary Key
Student_ID

### Sample Tuples
| Student_ID | Student_Name | Email | Department |
|---|---|---|---|
| S001 | Ananya | ananya@gmail.com | CSE |
| S002 | Rahul | rahul@gmail.com | ECE |
| S003 | Priya | priya@gmail.com | CSE |
| S004 | Kiran | kiran@gmail.com | EEE |
| S005 | Sneha | sneha@gmail.com | IT |

## 2. COURSE Relation
### Attributes
- Course_ID
- Course_Name
- Trainer_Name
- Duration

### Primary Key
Course_ID

### Sample Tuples
| Course_ID | Course_Name | Trainer_Name | Duration |
|---|---|---|---|
| C001 | Java Programming | Ravi Kumar | 3 Months |
| C002 | Python Programming | Priya Sharma | 4 Months |
| C003 | Web Development | Arun Kumar | 3 Months |

## 3. ENROLLMENT Relation
### Attributes
- Enrollment_ID
- Student_ID
- Course_ID
- Enrollment_Date

### Primary Key
Enrollment_ID

### Foreign Keys
- Student_ID references STUDENT(Student_ID)
- Course_ID references COURSE(Course_ID)

### Sample Tuples
| Enrollment_ID | Student_ID | Course_ID | Enrollment_Date |
|---|---|---|---|
| E001 | S001 | C001 | 2026-01-10 |
| E002 | S002 | C002 | 2026-01-12 |
| E003 | S003 | C001 | 2026-01-15 |
| E004 | S004 | C003 | 2026-01-18 |
| E005 | S005 | C002 | 2026-01-20 |

## Relationship Between Student and Course
STUDENT and COURSE are connected through ENROLLMENT.

- ENROLLMENT.Student_ID refers to STUDENT.Student_ID.
- ENROLLMENT.Course_ID refers to COURSE.Course_ID.

A student can enroll in courses, and a course can have multiple students.

## Basic Definitions

### What is a Relation?
A relation is a table in a relational database consisting of rows and columns.

### What is an Attribute?
An attribute is a column of a relation representing a particular property.

### What is a Tuple?
A tuple is a single row or record in a relation.

### What is a Relational Schema?
A relational schema defines the structure of a relation, including its name, attributes, and keys.

## Primary Keys
- STUDENT: Student_ID
- COURSE: Course_ID
- ENROLLMENT: Enrollment_ID

## Note
This project focuses only on basic relational schema concepts as required by the task. No normalization or advanced SQL queries are included.
