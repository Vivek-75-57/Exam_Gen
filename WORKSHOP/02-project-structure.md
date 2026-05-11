# Module 2: Project Structure

## Understanding the Codebase

ExamForge is organized into **Backend (Node.js/Express)** and **Frontend (React/Vite)** components.

---

## Backend Structure

```
backend/src/
├── app.js                     # Express app setup
├── index.js                   # Server entry point
│
├── config/
│   └── index.js               # Environment configuration
│
├── controllers/
│   ├── exam.js                # Exam request handlers
│   └── bookmark.js            # Bookmark handlers
│
├── routes/
│   ├── exam.js                # /api/exams endpoints
│   ├── bookmark.js            # /api/bookmarks endpoints
│   ├── health.js              # Health check
│   └── exportRoutes.js        # Route aggregator
│
└── services/
    ├── exam.js                # Exam business logic
    ├── bookmark.js            # Bookmark service
    ├── llm.js                 # Groq API integration
    ├── explanationService.js  # Generate explanations
    ├── reportService.js       # Generate reports
    ├── vectorStore.js         # Vector caching
    └── mockQuestions.js       # Test data
```

### Key Backend Concepts

| File | Purpose |
|------|---------|
| `app.js` | Express configuration, middleware setup |
| `index.js` | Server initialization, port binding |
| `controllers/` | Handle HTTP requests |
| `services/` | Business logic, API calls |
| `routes/` | Define API endpoints |

---

## Frontend Structure

```
frontend/src/
├── main.jsx                   # React entry point
├── App.jsx                    # Main component
│
├── components/
│   ├── exam/
│   │   ├── ConfigScreen.jsx       # Configuration page
│   │   ├── ExamScreen.jsx         # Exam taking interface
│   │   ├── ExplanationPanel.jsx   # Show explanations
│   │   └── GeneratingScreen.jsx   # Loading state
│   │
│   ├── results/
│   │   ├── ResultsScreen.jsx      # Display results
│   │   └── BookmarksScreen.jsx    # Saved questions
│   │
│   ├── layout/
│   │   └── Header.jsx             # Navigation
│   │
│   ├── animations/
│   │   └── Confetti.jsx           # Success animation
│   │
│   ├── notifications/
│   │   └── ToastContainer.jsx     # Toast messages
│   │
│   └── transitions/
│       └── PageTransition.jsx     # Page animations
│
├── hooks/
│   ├── useExam.js             # Exam state management
│   ├── useBookmarks.js        # Bookmark state
│   ├── useTheme.jsx           # Theme switching
│   └── useToast.js            # Toast notifications
│
├── services/
│   └── apiClient.js           # API communication
│
└── store/
    └── index.js               # Zustand store
```

### Key Frontend Concepts

| File | Purpose |
|------|---------|
| `components/` | React components |
| `hooks/` | Custom React hooks |
| `services/` | API calls and utilities |
| `store/` | Global state management |

---

## Data Flow

```
User Input → Frontend Component → API Call → Backend Route
    ↓
Backend Service → Groq API/Database → Response
    ↓
Frontend Component → UI Update → User Sees Result
```

---

## Next Steps

✅ Understand the structure?

→ **Next:** [Configuration](./03-configuration.md)
