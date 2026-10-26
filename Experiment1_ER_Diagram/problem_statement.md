# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1145" height="696" alt="image" src="https://github.com/user-attachments/assets/4ca1f27c-062a-40ce-b5b7-ad80f8233721" />


### Entities and Attributes

<img width="838" height="502" alt="image" src="https://github.com/user-attachments/assets/25de606f-eb0d-4b1f-8a36-db80ade6c8f2" />


### Relationships and Constraints

<img width="842" height="531" alt="image" src="https://github.com/user-attachments/assets/d2ee585c-5242-4d2f-ad54-f8768f7592bc" />




# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="1310" height="702" alt="WhatsApp Image 2026-10-26 at 10 41 07 AM" src="https://github.com/user-attachments/assets/ca599e79-51ff-4754-b2fd-5fb5ff97e2be" />

### Entities and Attributes
<img width="846" height="367" alt="image" src="https://github.com/user-attachments/assets/cd09f975-9966-43b5-943b-fd984494555d" />

### Relationships and Constraints
<img width="835" height="343" alt="image" src="https://github.com/user-attachments/assets/ffdec2f2-22fc-413a-8e95-760fa5c8d419" />




# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="1032" height="687" alt="image" src="https://github.com/user-attachments/assets/fa96a790-6e75-4382-9e39-fa8d7ed43e79" />


### Relationships and Constraints
<img width="840" height="351" alt="image" src="https://github.com/user-attachments/assets/9a9d294d-6086-4237-bfb7-8dd6ae83435e" />


### ER DIAGRAM
<img width="1032" height="687" alt="image" src="https://github.com/user-attachments/assets/b10c6e71-b7da-4369-a97f-e18868f61e59" />

### Assumptions
Only registered members can borrow books. Members may register for multiple events. Every event has at least one speaker. A book can be borrowed many times at different periods.

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
