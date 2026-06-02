# 🔧 Backend — Flask Learning Management System API

> A Flask-based REST API for a Learning Management System (LMS) with user authentication, course management, assignment submissions, and grading — intentionally built with security vulnerabilities for educational/research purposes.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

---

## 📌 Overview

This is the backend service for a Learning Management System, built with **Flask** and **SQLAlchemy**. It supports role-based access for students and teachers, course enrollment, assignment submission, and grading workflows.

> ⚠️ **Security Notice**: This application is intentionally built with security vulnerabilities (SQL injection, plaintext passwords, IDOR, XSS) for **educational and research purposes only**. Do NOT deploy in production.

---

## ✨ Features

- 👤 User registration and login (student & teacher roles)
- 📚 Course creation and enrollment
- 📝 Assignment submission with file upload
- 🏆 Grading system with feedback
- 🔐 JWT-based authentication
- 🐳 Dockerized for easy deployment

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Health check |
| POST | `/api/register` | Register a new user |
| POST | `/api/login` | Login and get JWT token |
| GET/POST | `/api/courses` | Get all / create courses |
| POST | `/api/enroll` | Enroll in a course |
| POST | `/api/submit-assignment` | Submit an assignment |
| POST | `/api/grade/student` | Grade a student |
| GET | `/api/courses/:id/students` | Get students in a course |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Docker (optional)

### Run Locally
```bash
pip install -r requirements.txt
python app.py
```
App runs at `http://localhost:4000`

### Run with Docker
```bash
docker build -t lms-backend .
docker run -p 4000:4000 lms-backend
```

### Default Teacher Account

Username: john.smith
Password: teacher123

---

## 🔐 Known Vulnerabilities (Intentional)

| Vulnerability | Location |
|---|---|
| SQL Injection | `/api/login` |
| Plaintext Passwords | User model |
| IDOR | `/api/student-submissions` |
| Stored XSS | Course description field |
| Command Injection | `/api/export-grades` |
| Path Traversal | `/api/download` |

---

## 📁 Project Structure

📦 Backend-
┣ 📄 app.py          # Main Flask application
┣ 📄 test_app.py     # Unit tests
┣ 📄 requirements.txt
┣ 📄 Dockerfile
┗ 📄 .gitignore

---

<p align="center">Made with 🐍 by <a href="https://github.com/Sumanjali23">Grace Sumanjali Pagolu</a></p>
