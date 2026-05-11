# Module 3: Configuration

## Setting Up Environment Variables

All sensitive configuration is managed through environment variables.

---

## Backend Configuration

### Step 1: Copy Example File
```bash
cd backend
cp .env.example .env
```

### Step 2: Edit `.env` File

```env
# Server Settings
NODE_ENV=development
PORT=3001

# Groq API Configuration
GROQ_API_KEY=your-api-key-here
GROQ_MODEL=mixtral-8x7b-32768
GROQ_MAX_TOKENS=4096

# Frontend Access
CORS_ORIGIN=http://localhost:5173

# Features
ENABLE_FAISS_CACHING=true
```

---

## Getting Your Groq API Key

### Step-by-Step Guide

1. **Visit Groq Console**
   - Go to [Groq Console](https://console.groq.com)

2. **Sign Up or Login**
   - Create an account or use existing credentials

3. **Navigate to API Keys**
   - Click on "API keys" in the left sidebar

4. **Create New Key**
   - Click "Create New API Key"
   - Give it a name (e.g., "ExamForge Dev")

5. **Copy the Key**
   - Copy the generated key

6. **Paste into `.env`**
   ```env
   GROQ_API_KEY=gsk_xxxxxxxxxxxxxxxxxxxxxxxxxx
   ```

7. **Save and Verify**
   - Your backend should now authenticate with Groq

---

## Configuration Options Reference

### Server Configuration

| Variable | Default | Purpose |
|----------|---------|---------|
| `NODE_ENV` | development | Environment mode |
| `PORT` | 3001 | Server port |

### Groq API Configuration

| Variable | Default | Purpose |
|----------|---------|---------|
| `GROQ_API_KEY` | - | API authentication key |
| `GROQ_MODEL` | mixtral-8x7b-32768 | AI model to use |
| `GROQ_MAX_TOKENS` | 4096 | Max response length |

### Application Configuration

| Variable | Default | Purpose |
|----------|---------|---------|
| `CORS_ORIGIN` | http://localhost:5173 | Frontend origin |
| `ENABLE_FAISS_CACHING` | true | Enable vector caching |

---

## Verifying Configuration

```bash
# Test if server starts with config
npm run dev

# Expected output:
# Server running on http://localhost:3001
# Groq API initialized
```

---

## Troubleshooting Configuration

### Issue: "GROQ_API_KEY is not defined"
**Solution:** 
- Check if `.env` file exists
- Verify the API key is correctly set
- Restart the server after changing `.env`

### Issue: "CORS error"
**Solution:**
- Verify CORS_ORIGIN matches your frontend URL
- For local dev, use: `http://localhost:5173`

### Issue: "Unable to connect to Groq"
**Solution:**
- Check if your API key is valid
- Verify you have API quota remaining
- Check internet connection

---

## Next Steps

✅ Configuration complete?

→ **Next:** [Running the Application](./04-running-application.md)
