# Health-and-Fitness-Club-Management-System
An SQL database system for a health and fitness club, used to manage members, emails, weight goals, and track progess. 

Ahmad Kanaan


## Overview
This project implements a Health & Fitness Club Management System using **Python**, **PostgreSQL**, and **SQLAlchemy ORM**.  
It supports three roles:
- **Members** – track metrics, set goals, register for classes, schedule PT sessions  
- **Trainers** – set availability, view schedules, search members  
- **Admins** – manage rooms, classes, equipment, maintenance tickets  

Includes: ERD, ORM schema, CLI app, and required SQL View, Trigger, and Index.

---

## Setup Instructions

### 1. Create virtual environment
```bash
python -m venv venv
venv/Scripts/activate
```

### 2. Install dependencies
```bash
pip install sqlalchemy psycopg2-binary
```

### 3. Create PostgreSQL database
Name it:
```
fitness_club
```

### 4. Set database credentials  
In `models.py`, update:
```python
DATABASE_URL = "postgresql+psycopg2://USER:PASSWORD@localhost:5432/fitness_club"
```

### 5. Create tables
```bash
python init_db.py
```

### 6. Seed demo trainer + room
```bash
python seed_demo_data.py
```

### 7. Run the application
```bash
python main.py
```

---

## Features

### Member
- Register / Login  
- Add health metrics  
- Set fitness goals  
- View dashboard & history  
- Register for group classes  
- Schedule personal training sessions (conflict-checked)

### Trainer
- Login  
- Set availability (no overlapping windows)  
- View upcoming schedule  
- Search members (case-insensitive)

### Admin
- Create rooms  
- Create group classes  
- Log equipment issues  
- Update maintenance tickets  


---

## Demo Video:

https://youtu.be/5ws1sVM3t7Y
