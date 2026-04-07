# 🏋️ Fitness Influencer Coaching Platform – DB Design

This project presents the database design for an online fitness coaching platform where trainers manage clients, sell plans, track progress, and conduct sessions.

---

##  Problem Statement

A fitness influencer started coaching via Instagram DMs and video calls. As the business scaled, a structured system was needed to:

- Manage trainers and clients
- Sell fitness plans
- Handle subscriptions and payments
- Schedule sessions/consultations
- Track client progress and check-ins

---

##  Key Features of the Design

-  User system with role-based extension (Trainer / Client)
-  Plan and subscription model (supports multiple enrollments)
-  Payment tracking for subscriptions
-  Session scheduling (consultation / live training)
-  Progress tracking (body metrics)
- Weekly check-ins system
-  Trainer notes for personalized feedback

---

##  Core Entities

- **users** – Common user data
- **trainer** – Trainer-specific details
- **client** – Client-specific details
- **plan** – Coaching programs
- **subscription** – Links clients with plans
- **payment** – Payment records
- **session** – Scheduled meetings
- **check_in** – Weekly reports
- **progress** – Body metrics tracking
- **trainer_note** – Trainer feedback

---

##  Relationships Overview

| Relationship | Type |
|-------------|------|
| User ↔ Trainer | 1 : 1 |
| User ↔ Client | 1 : 1 |
| Trainer → Plan | 1 : M |
| Client ↔ Plan | M : M (via Subscription) |
| Subscription → Payment | 1 : M |
| Trainer ↔ Client | M : M (via Session) |
| Client → Check-in | 1 : M |
| Client → Progress | 1 : M |
| Trainer ↔ Client | M : M (via Trainer Notes) |

---

##  ER Diagram
![ER Diagram](./fitness%20img.png)


---

## Design Decisions

- Used **separate tables for trainer and client** to maintain role clarity
- Implemented **subscription table** to resolve many-to-many between clients and plans
- Kept **sessions and check-ins separate** to avoid confusion
- Stored **progress data independently** for better normalization
- Added **trainer notes** for better coaching insights

---

##  Outcome

This schema is scalable and supports:

- Multiple trainers and clients
- Multiple plan subscriptions per client
- Real-time coaching workflows
- Structured progress tracking

---

##  Tech Used

- ER Modeling (Draw.io / Eraser)
- Relational Database Design Concepts

---

## Feedback

Open to feedback and suggestions to improve the design!
