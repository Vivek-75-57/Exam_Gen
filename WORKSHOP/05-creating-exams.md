# Module 5: Creating Exams

## How to Generate AI-Powered Exams

Learn how to create, take, and submit exams using ExamForge.

---

## Step-by-Step Process

### Step 1: Configuration Screen

When you first load ExamForge, you'll see the **Configuration Screen**.

#### Configure Your Exam

| Setting | Options | Default |
|---------|---------|---------|
| **Subject** | Any topic (e.g., JavaScript, React) | Required |
| **Number of Questions** | 5, 10, 15, 20 | 10 |
| **Difficulty Level** | Easy, Medium, Hard | Medium |
| **Question Type** | Multiple Choice, True/False | Multiple Choice |

#### Example Configuration
```
Subject: JavaScript Fundamentals
Questions: 10
Difficulty: Medium
Type: Multiple Choice
```

---

### Step 2: Generate Exam

1. Fill in all configuration fields
2. Click **"Generate Exam"** button
3. Wait for AI to generate questions (10-30 seconds)

#### Behind the Scenes

```
Your Config → Backend Receives → Groq API → Generate Questions
    ↓
Format Questions → Send to Frontend → Display Exam
```

### Step 3: Taking the Exam

#### For Each Question

1. **Read the Question** carefully
2. **Review All Options** 
3. **Select Your Answer**
4. **Click Next** to proceed

#### Features During Exam

| Feature | Purpose |
|---------|---------|
| Progress Bar | Shows question progress |
| Question Counter | "Question 3 of 10" |
| Timer | Tracks time spent |
| Bookmark Icon | Save for later |
| Navigation | Previous/Next buttons |

---

### Step 4: Submitting Exam

1. Complete all questions
2. Review your answers (optional)
3. Click **"Submit Exam"** button
4. Confirm submission

---

## After Submission

### Results Screen

Your results include:

```
╔════════════════════════════════╗
║   EXAM RESULTS                 ║
║─────────────────────────────────║
║  Score: 8/10 (80%)             ║
║  Time: 12:34                   ║
║  Difficulty: Medium            ║
║  Accuracy: 80%                 ║
╚════════════════════════════════╝
```

### Review Answers

For each question, you can:
- ✅ View if you answered correctly
- 📖 Read detailed explanation
- 🔗 See related topics
- 📌 Save for bookmarks

---

## Example Workflow

```
START
  ↓
Configure Exam (Select subject, difficulty, etc)
  ↓
Generate (AI creates questions)
  ↓
Take Exam (Answer all questions)
  ↓
Submit Answers
  ↓
View Results & Score
  ↓
Review Explanations
  ↓
Save Bookmarks (Optional)
  ↓
Export Report (Optional)
  ↓
FINISH
```

---

## Tips for Best Results

### While Configuring
- Choose a specific topic for better questions
- Medium difficulty is recommended for learning
- Start with 10 questions

### While Taking Exam
- Read questions carefully
- Use the bookmark feature for uncertain answers
- Don't rush through

### After Submission
- Review explanations for wrong answers
- Bookmark important questions
- Take another exam on different topics

---

## Bookmarking Questions

### Why Bookmark?
- Save important questions for review
- Build a study list
- Track difficult topics

### How to Bookmark
1. During exam, click **bookmark icon** (📌)
2. After results, click **bookmark** on specific questions
3. View all bookmarks in **Bookmarks section**

---

## Next Steps

✅ Created and submitted an exam?

→ **Next:** [Advanced Features](./06-advanced-features.md)
