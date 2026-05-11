# GitHub Instructions - ExamForge

## Getting Started with ExamForge from GitHub

This guide will help you clone, set up, and run the ExamForge project on your local machine.

---

## 📋 Prerequisites

Before starting, ensure you have the following installed:
- **Git** - [Download Git](https://git-scm.com/download)
- **Node.js** (v16+) - [Download Node.js](https://nodejs.org/)
- **npm** (comes with Node.js)

---

## 🚀 Quick Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Vivek-75-57/Exam_Gen.git
cd Exam_Gen
```

### 2. Set Up Environment Variables

#### Backend Setup:
```bash
cd backend
cp .env.example .env
```

Edit the `.env` file and add your **Groq API Key**:
```
GROQ_API_KEY=your-key-here
```

**How to get Groq API Key:**
1. Go to [Groq Console](https://console.groq.com)
2. Sign up or log in
3. Navigate to "API keys"
4. Create a new API key
5. Copy and paste it into your `.env` file

### 3. Install Dependencies

#### Backend:
```bash
cd backend
npm install
```

#### Frontend (new terminal):
```bash
cd frontend
npm install
```

---

## 🏃 Running the Project

### Start Backend Server

```bash
cd backend
npm run dev
```

✅ Backend will run at: `http://localhost:3001`

### Start Frontend Dev Server (new terminal)

```bash
cd frontend
npm run dev
```

✅ Frontend will run at: `http://localhost:5173`

### Open in Browser

Visit `http://localhost:5173` in your browser and start creating exams! 🎉

---

## 📁 Project Structure

```
Exam_Gen/
├── backend/
│   ├── src/
│   │   ├── controllers/    # Request handlers
│   │   ├── routes/         # API endpoints
│   │   ├── services/       # Business logic
│   │   ├── config/         # Configuration
│   │   ├── app.js          # Express app setup
│   │   └── index.js        # Server entry point
│   ├── package.json
│   └── .env.example
│
├── frontend/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── hooks/          # Custom hooks
│   │   ├── services/       # API client
│   │   ├── store/          # State management
│   │   ├── App.jsx         # Main app component
│   │   └── main.jsx        # Entry point
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

## 🛠️ Available Commands

### Backend
```bash
npm run dev        # Start development server
npm start          # Start production server
npm test           # Run tests (if available)
```

### Frontend
```bash
npm run dev        # Start Vite dev server
npm run build      # Build for production
npm run preview    # Preview production build
npm run lint       # Check for linting errors (if configured)
```

---

## 🔧 Technologies Used

| Component | Stack |
|-----------|-------|
| **Backend** | Node.js, Express.js |
| **Frontend** | React 18, Vite, Tailwind CSS |
| **Database** | JSON files (local) |
| **AI/LLM** | Groq API (llama-3.1-8b-instant) |
| **State** | Zustand |

---

## 🐛 Troubleshooting

### Issue: "GROQ_API_KEY is not defined"
**Solution:** Make sure you've created a `.env` file in the `backend` folder with your Groq API key.

### Issue: Port 3001 or 5173 already in use
**Solution:** Change the port in the respective `.env` or config file.

### Issue: npm install fails
**Solution:** Try clearing npm cache:
```bash
npm cache clean --force
npm install
```

### Issue: Module not found errors
**Solution:** Delete `node_modules` and reinstall:
```bash
rm -r node_modules package-lock.json  # or use 'del' on Windows
npm install
```

---

## 📝 Making Changes & Contributing

1. **Create a new branch** for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** and commit:
   ```bash
   git add .
   git commit -m "Add your descriptive commit message"
   ```

3. **Push to GitHub**:
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Create a Pull Request** on GitHub

---

## 📚 API Documentation

See [API_CALLS_EXPLAINED.md](./API_CALLS_EXPLAINED.md) for detailed API endpoint documentation.

---

## 📄 License

This project is licensed under the MIT License - see [LICENSE](./LICENSE) file for details.

---

## 🤝 Support

For issues, questions, or suggestions, please [open an issue](https://github.com/Vivek-75-57/Exam_Gen/issues) on GitHub.

---

**Happy coding! 🚀**
