# Module 4: Running the Application

## Starting Both Servers

ExamForge requires both **Backend** and **Frontend** servers running simultaneously.

---

## Backend Server

### Start Development Server

```bash
cd backend
npm run dev
```

### Expected Output

```
Server running on http://localhost:3001
Groq API initialized
✓ Connected to Groq
✓ Database connected
Ready to accept requests
```

### Available Backend Commands

| Command | Purpose |
|---------|---------|
| `npm run dev` | Development (with auto-reload) |
| `npm start` | Production mode |
| `npm test` | Run tests |

### Backend API Endpoints

- **Health Check:** `GET http://localhost:3001/api/health`
- **Create Exam:** `POST http://localhost:3001/api/exams`
- **Get Bookmarks:** `GET http://localhost:3001/api/bookmarks`

---

## Frontend Server

### Open New Terminal and Start Dev Server

```bash
cd frontend
npm run dev
```

### Expected Output

```
  VITE v4.x.x  ready in 234 ms

  ➜  Local:   http://localhost:5173/
  ➜  press h to show help
```

### Available Frontend Commands

| Command | Purpose |
|---------|---------|
| `npm run dev` | Development server |
| `npm run build` | Production build |
| `npm run preview` | Preview build |

---

## Accessing the Application

### Open in Browser

Navigate to: **http://localhost:5173**

You should see the ExamForge home screen.

---

## Complete Startup Checklist

- [ ] Backend `.env` file configured
- [ ] Backend running on `http://localhost:3001`
- [ ] Frontend running on `http://localhost:5173`
- [ ] Browser shows ExamForge interface
- [ ] No errors in browser console
- [ ] No errors in terminal

---

## Verifying Everything Works

### Test Backend
```bash
# In a new terminal
curl http://localhost:3001/api/health

# Expected response:
# {"status":"ok"}
```

### Test Frontend
- Open DevTools (F12)
- Go to Network tab
- Create an exam and verify API calls

---

## Stopping the Servers

To stop either server, press **Ctrl + C** in the terminal.

---

## Next Steps

✅ Servers running smoothly?

→ **Next:** [Creating Exams](./05-creating-exams.md)
