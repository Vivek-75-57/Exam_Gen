# ExamForge Workshop - Complete Guide

Welcome to the **ExamForge Workshop** — a self-paced guide to understanding and using ExamForge's AI-powered exam generation capabilities.

This workshop covers the full spectrum of features, from basic setup to advanced customization, helping you create and manage technical exams with AI assistance.

---

## 📚 Workshop Modules

| Step | Module | Description |
|------|--------|-------------|
| 1 | [Getting Started](#1-getting-started) | Setup and installation guide |
| 2 | [Project Structure](#2-project-structure) | Understanding the codebase |
| 3 | [Configuration](#3-configuration) | Setting up environment and API keys |
| 4 | [Running the Application](#4-running-the-application) | Starting backend and frontend |
| 5 | [Creating Exams](#5-creating-exams) | How to generate AI-powered exams |
| 6 | [Advanced Features](#6-advanced-features) | Bookmarks, explanations, and reports |

---

## 1️⃣ Getting Started

### What You'll Learn
- How to clone the repository
- Installing dependencies
- Verifying your setup

### Prerequisites
- Git installed
- Node.js v16 or higher
- npm package manager
- Groq API account

### Quick Start
```bash
# Clone the repository
git clone https://github.com/Vivek-75-57/Exam_Gen.git
cd Exam_Gen

# Install dependencies
cd backend && npm install
cd ../frontend && npm install
```

---

## 2️⃣ Project Structure

### Understanding the Codebase

#### Backend Structure
```
backend/
├── src/
│   ├── app.js                 # Express app configuration
│   ├── index.js               # Server entry point
│   ├── config/
│   │   └── index.js           # Environment & API config
│   ├── controllers/
│   │   ├── exam.js            # Exam request handlers
│   │   └── bookmark.js        # Bookmark request handlers
│   ├── routes/
│   │   ├── exam.js            # Exam API routes
│   │   ├── bookmark.js        # Bookmark API routes
│   │   ├── health.js          # Health check route
│   │   └── exportRoutes.js    # Route exports
│   └── services/
│       ├── exam.js            # Exam business logic
│       ├── bookmark.js        # Bookmark management
│       ├── llm.js             # Groq API integration
│       ├── explanationService.js  # Generate explanations
│       ├── reportService.js   # Generate reports
│       ├── vectorStore.js     # Vector storage
│       └── mockQuestions.js   # Mock question data
├── .env.example               # Environment variables template
└── package.json               # Dependencies
```

#### Frontend Structure
```
frontend/
├── src/
│   ├── main.jsx               # React entry point
│   ├── App.jsx                # Main app component
│   ├── index.css              # Global styles
│   ├── components/
│   │   ├── exam/
│   │   │   ├── ConfigScreen.jsx       # Exam configuration
│   │   │   ├── ExamScreen.jsx         # Exam interface
│   │   │   ├── ExplanationPanel.jsx   # Show explanations
│   │   │   └── GeneratingScreen.jsx   # Loading state
│   │   ├── results/
│   │   │   ├── ResultsScreen.jsx      # Show results
│   │   │   └── BookmarksScreen.jsx    # View bookmarks
│   │   ├── layout/
│   │   │   └── Header.jsx             # Navigation
│   │   ├── animations/
│   │   │   └── Confetti.jsx           # Celebration animation
│   │   ├── notifications/
│   │   │   └── ToastContainer.jsx     # Toast messages
│   │   └── transitions/
│   │       └── PageTransition.jsx     # Page animations
│   ├── hooks/
│   │   ├── useExam.js         # Exam state management
│   │   ├── useBookmarks.js    # Bookmark management
│   │   ├── useTheme.jsx       # Theme switching
│   │   └── useToast.js        # Toast notifications
│   ├── services/
│   │   └── apiClient.js       # API communication
│   └── store/
│       └── index.js           # Zustand state store
├── vite.config.js             # Vite configuration
├── tailwind.config.js         # Tailwind CSS config
└── package.json               # Dependencies
```

---

## 3️⃣ Configuration

### Setting Up Environment Variables

#### Backend Configuration
```bash
cd backend
cp .env.example .env
```

Edit `.env` with your values:
```env
NODE_ENV=development
PORT=3001
GROQ_API_KEY=your-groq-api-key-here
CORS_ORIGIN=http://localhost:5173
GROQ_MODEL=mixtral-8x7b-32768
GROQ_MAX_TOKENS=4096
ENABLE_FAISS_CACHING=true
```

### Getting Your Groq API Key
1. Visit [Groq Console](https://console.groq.com)
2. Sign up or login
3. Navigate to "API keys"
4. Click "Create New API Key"
5. Copy the key and paste into `.env`

### Important Config Options

| Variable | Value | Purpose |
|----------|-------|---------|
| `GROQ_API_KEY` | Your API key | Authenticate with Groq LLM |
| `GROQ_MODEL` | mixtral-8x7b-32768 | LLM model to use |
| `GROQ_MAX_TOKENS` | 4096 | Maximum response length |
| `CORS_ORIGIN` | http://localhost:5173 | Frontend origin for CORS |
| `ENABLE_FAISS_CACHING` | true | Enable vector caching |

---

## 4️⃣ Running the Application

### Starting the Backend Server
```bash
cd backend
npm run dev
```

Expected output:
```
Server running on http://localhost:3001
Connected to Groq API
```

### Starting the Frontend Dev Server
```bash
# New terminal
cd frontend
npm run dev
```

Expected output:
```
  VITE v4.x.x  ready in xxx ms

  ➜  Local:   http://localhost:5173/
  ➜  press h to show help
```

### Opening in Browser
Navigate to: **http://localhost:5173**

---

## 5️⃣ Creating Exams

### Step-by-Step Guide

#### 1. Configuration Screen
- **Subject**: Enter the topic (e.g., "JavaScript", "Database Design")
- **Number of Questions**: Choose 5, 10, 15, or 20
- **Difficulty Level**: Select Easy, Medium, or Hard
- **Question Type**: Multiple Choice or True/False

#### 2. Generating Exam
- Click "Generate Exam"
- AI uses Groq API to create questions
- Wait for generation (typically 10-30 seconds)

#### 3. Taking the Exam
- Read each question carefully
- Select your answer
- View immediate feedback
- Track your progress

#### 4. Viewing Results
- See your score
- Review correct/incorrect answers
- Access detailed explanations

### Example Workflow
```
Start → Configure → Generate → Take Exam → Submit → View Results → Export
```

---

## 6️⃣ Advanced Features

### 📌 Bookmarks
Save important questions or answers for later review.

```javascript
// Save a bookmark
POST /api/bookmarks
{
  "questionId": "q1",
  "questionText": "...",
  "savedAnswer": "..."
}

// Retrieve bookmarks
GET /api/bookmarks
```

### 📖 Explanations
AI-generated explanations for each question.

**Features:**
- Detailed answer breakdown
- Concept explanation
- Related topics
- Learning resources

### 📊 Reports
Generate comprehensive exam reports.

**Includes:**
- Score breakdown
- Time taken
- Difficulty analysis
- Performance metrics

### 🔄 Vector Store
Efficient question caching using FAISS.

**Benefits:**
- Faster retrieval
- Semantic search
- Question similarity matching

---

## 🔧 Available Commands

### Backend
```bash
npm run dev      # Development mode (with hot reload)
npm start        # Production mode
npm test         # Run tests
npm run lint     # Check code quality
```

### Frontend
```bash
npm run dev      # Development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Lint code (if configured)
```

---

## 📖 API Reference

### Exam Endpoints
```
POST   /api/exams                # Generate new exam
GET    /api/exams/:id            # Get exam details
POST   /api/exams/:id/submit     # Submit answers
GET    /api/exams/:id/results    # Get results
```

### Bookmark Endpoints
```
GET    /api/bookmarks            # List all bookmarks
POST   /api/bookmarks            # Create bookmark
DELETE /api/bookmarks/:id        # Delete bookmark
```

### Health Check
```
GET    /api/health               # Server health status
```

---

## 🐛 Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| GROQ_API_KEY error | Verify `.env` file has valid key |
| Port 3001 in use | Change PORT in `.env` |
| Dependencies error | Run `npm cache clean --force` |
| CORS error | Check CORS_ORIGIN in `.env` |
| Slow generation | Check Groq API quota |

---

## 📈 Performance Tips

1. **Enable Caching**: Set `ENABLE_FAISS_CACHING=true`
2. **Use Appropriate Models**: Smaller models are faster
3. **Batch Questions**: Generate multiple questions together
4. **Clean Bookmarks**: Regularly remove old bookmarks

---

## 🔐 Security Best Practices

- Never commit `.env` files with real API keys
- Use environment variables for sensitive data
- Validate all user inputs
- Keep dependencies updated
- Use HTTPS in production

---

## 📚 Additional Resources

- [Groq API Documentation](https://console.groq.com/docs)
- [Express.js Guide](https://expressjs.com/)
- [React Documentation](https://react.dev)
- [Vite Documentation](https://vitejs.dev)
- [Tailwind CSS](https://tailwindcss.com)

---

## 🤝 Need Help?

- Check [GITHUB_INSTRUCTIONS.md](./GITHUB_INSTRUCTIONS.md)
- Review [API_CALLS_EXPLAINED.md](./API_CALLS_EXPLAINED.md)
- Open an issue on [GitHub](https://github.com/Vivek-75-57/Exam_Gen/issues)

---

## ✅ Workshop Completion Checklist

- [ ] Cloned the repository
- [ ] Installed dependencies
- [ ] Set up environment variables
- [ ] Started backend server
- [ ] Started frontend server
- [ ] Created first exam
- [ ] Reviewed explanations
- [ ] Bookmarked a question
- [ ] Viewed exam results
- [ ] Explored advanced features

**Congratulations! You've completed the ExamForge Workshop! 🎉**

---

**Happy Learning! 🚀**
