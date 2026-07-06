# 💊 DoseDone

AI-powered medication adherence platform built with FastAPI, PostgreSQL, JWT authentication, and intelligent reminder workflows.

## 📌 Overview

DoseDone helps users manage medicines, track medication intake, and improve adherence through reminders and analytics.

The goal is to simplify daily medication routines by allowing users to:

- Register and securely log in
- Add and manage medicines
- Track medicine schedules
- Monitor adherence history
- Receive low-stock alerts
- Get medication insights and reminders

---

## 🚀 Current Features (V1 Progress)

### User Authentication
- User registration
- Password hashing using bcrypt
- JWT-based authentication
- Protected routes
- Current logged-in user endpoint

### Medicine Management
- Add medicines
- Fetch medicines for logged-in users
- User-specific medicine ownership

### Database Integration
- PostgreSQL database
- SQLAlchemy ORM
- Pydantic schema validation
- Environment-based configuration

---

## 🛠️ Tech Stack

**Backend**
- FastAPI
- Python
- SQLAlchemy
- PostgreSQL

**Authentication**
- JWT
- Passlib (bcrypt)

**Validation**
- Pydantic

**Server**
- Uvicorn

---

## 📂 Project Structure

```bash
DoseDone/
│
├── app/
│   │
│   ├── routers/
│   │   ├── auth.py
│   │   ├── users.py
│   │   ├── medicines.py
│   │
│   ├── services/
│   │   ├── notification_service.py
│   │   ├── scheduler_service.py
│   │   └── stock_service.py
│   │
│   ├── auth.py
│   ├── crud.py
│   ├── database.py
│   ├── dependencies.py
│   ├── main.py
│   ├── models.py
│   └── schemas.py
│
├── tests/
├── uploads/
├── .env
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

Clone repository:

```bash
git clone https://github.com/sreejaguntu/DoseDone.git
```

Move into project:

```bash
cd DoseDone
```

Create virtual environment:

```bash
python -m venv venv
```

Activate environment:

Windows:

```bash
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file:

```env
DATABASE_URL=postgresql://postgres:yourpassword@localhost:5432/dosedone

SECRET_KEY=your_secret_key

ALGORITHM=HS256

ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

## ▶️ Run Project

Start FastAPI server:

```bash
uvicorn app.main:app --reload
```

API Docs:

```bash
http://127.0.0.1:8000/docs
```

---

## API Endpoints

### Authentication

| Method | Endpoint | Description |
|----------|----------|-------------|
| POST | /users/register | Register new user |
| POST | /auth/login | Login and get JWT |

### Users

| Method | Endpoint | Description |
|----------|----------|-------------|
| GET | /users/me | Get current logged-in user |

### Medicines

| Method | Endpoint | Description |
|----------|----------|-------------|
| POST | /medicines | Add medicine |
| GET | /medicines | Get user medicines |

---

## 🔒 Authentication Flow

```text
Register User
      ↓
Password Hashing
      ↓
Login
      ↓
JWT Token Generated
      ↓
Protected Routes
      ↓
Fetch User-specific Data
```

---

## 🎯 Upcoming Features

- DoseLog APIs
- Medicine schedules
- Daily reminder workflows
- Low-stock notifications
- Adherence dashboard
- AI-powered medication insights
- Mobile app integration

---

## 📜 License

MIT License

---

## 👩‍💻 Author

**Sreeja Guntu**

GitHub: https://github.com/sreejaguntu
