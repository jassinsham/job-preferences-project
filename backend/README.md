# 🚀 Job Analytics Platform & Resume Matcher

An AI-powered job analytics platform that matches resumes with real-world job market data using NLP and provides a premium, interactive dashboard.

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

## ✨ Features
- **AI Resume Analysis**: Extract skills, experience, and education using spaCy and regex.
- **Market Matching**: Weighted compatibility scoring against 1000+ real job listings.
- **Dynamic Dashboards**: Glassmorphism UI with Chart.js visualizations (Radar, Bar, Line).
- **Secure Auth**: JWT-based authentication with PBKDF2-SHA256 hashing.
- **Salary Insights**: Real-time aggregation of market compensation trends.
- **Job Persistence**: Save interesting roles and track them in your personal dashboard.

## 🛠️ Tech Stack
- **Backend**: FastAPI (Python)
- **Database**: SQLAlchemy (SQLite for dev, easily switchable to PostgreSQL)
- **NLP**: spaCy, PyMuPDF, docx2txt
- **Frontend**: Jinja2 Templates, Vanilla CSS (Glassmorphism), Chart.js
- **Server**: Gunicorn / Uvicorn

## 🚀 Deployment Guide

### Why not GitHub Pages?
**Important**: This project contains a Python backend and a database. GitHub Pages only supports **static** files (HTML/CSS). To run the full application, you must use a Web Service provider.

### Option 1: One-Click Deploy (Recommended)
1. Push this code to your GitHub repository.
2. Click the **Deploy to Render** button above.
3. Render will automatically detect the `Dockerfile` and `Procfile` and start your service!

### Option 2: Manual Deployment (Render/Railway/Heroku)
- **Build Command**: `pip install -r requirements.txt`
- **Start Command**: `gunicorn -w 4 -k uvicorn.workers.UvicornWorker main:app`
- **Environment Variables**: Set `PORT=8000`.

## 💻 Local Development
1. Clone the repo.
2. Install dependencies: `pip install -r requirements.txt`.
3. Run the dev server: `python -m uvicorn main:app --reload`.
4. Access at `http://localhost:8000`.

---
*Built with ❤️ for Job Seekers.*
