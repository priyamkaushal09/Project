# AI Resume Analyzer & ATS Checker

A modern full-stack AI-powered Resume Analyzer web application where users can upload resumes, paste job descriptions, and receive an ATS compatibility score, matched skills, missing skills, AI suggestions, and interview preparation tips.

## 🎯 Features

### Core Features
- ✅ User Authentication (Sign up, Login, JWT)
- ✅ Resume Upload & PDF Parsing
- ✅ ATS Score Calculation
- ✅ Skill Matching & Gap Analysis
- ✅ AI-Powered Suggestions
- ✅ User Dashboard with History
- ✅ Analytics & Charts

### Advanced Features
- 🤖 AI Interview Question Generator
- 📊 Resume Strength Meter
- 📥 Download Reports as PDF
- 🌙 Dark/Light Theme
- 📱 Fully Responsive Design

## 🛠️ Tech Stack

### Frontend
- React.js + Vite
- Tailwind CSS
- Axios
- React Router DOM
- Framer Motion
- Recharts

### Backend
- Python Flask
- Flask-CORS
- JWT Authentication
- PyPDF2 & pdfplumber
- scikit-learn, nltk, spaCy

### Database
- MongoDB Atlas

### Deployment
- Frontend: Vercel
- Backend: Render
- Database: MongoDB Atlas

## 📁 Project Structure

```
ai-resume-analyzer/
├── frontend/                 # React application
│   ├── src/
│   ├── public/
│   ├── vite.config.js
│   ├── tailwind.config.js
│   ├── package.json
│   └── .env.example
│
├── backend/                  # Flask API server
│   ├── app.py
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── services/
│   ├── utils/
│   ├── middleware/
│   ├── config/
│   ├── requirements.txt
│   └── .env.example
│
├── .gitignore
├── README.md
└── DEPLOYMENT.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js 16+ & npm
- Python 3.8+
- MongoDB Atlas account
- Git

### Frontend Setup

```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```

### Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
python app.py
```

## 📋 Development Phases

**Phase 1:** Authentication & Setup
**Phase 2:** Resume Upload & ATS Analysis
**Phase 3:** Dashboard & Analytics
**Phase 4:** AI Features & Advanced Analysis
**Phase 5:** Deployment & Optimization

## 🔑 Environment Variables

Frontend `.env.local`:
```
VITE_API_URL=http://localhost:5000
```

Backend `.env`:
```
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
FLASK_ENV=development
```

## 📦 API Endpoints

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/resume/upload` - Upload resume
- `POST /api/analysis/analyze` - Analyze resume vs JD
- `GET /api/history` - Get user history
- `GET /api/profile` - Get user profile

## 🤝 Contributing

1. Create a feature branch: `git checkout -b feature/feature-name`
2. Commit changes: `git commit -m "Add feature"`
3. Push to branch: `git push origin feature/feature-name`
4. Open a Pull Request

## 📝 License

MIT License - feel free to use this project!

## 👨‍💻 Author

**Priyam Kaushal** - Full Stack Developer

---

**Status:** 🚀 In Development

Last Updated: May 2026
