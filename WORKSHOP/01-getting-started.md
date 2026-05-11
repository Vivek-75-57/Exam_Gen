# Module 1: Getting Started

## What You'll Learn
- How to clone the repository
- Installing dependencies
- Verifying your setup
- Understanding prerequisites

---

## Prerequisites

Before starting, ensure you have the following installed:

| Requirement | Version | Link |
|-------------|---------|------|
| Git | Latest | [Download Git](https://git-scm.com/download) |
| Node.js | v16+ | [Download Node.js](https://nodejs.org/) |
| npm | v7+ | Included with Node.js |
| Groq Account | - | [Create Account](https://console.groq.com) |

### Verify Installation
```bash
git --version
node --version
npm --version
```

---

## Clone the Repository

```bash
git clone https://github.com/Vivek-75-57/Exam_Gen.git
cd Exam_Gen
```

---

## Install Dependencies

### Backend Setup
```bash
cd backend
npm install
```

### Frontend Setup
```bash
cd ../frontend
npm install
```

### Verify Installation
```bash
cd ..
ls -la  # or 'dir' on Windows
# You should see: backend/, frontend/, README.md, etc.
```

---

## Next Steps

✅ Completed Getting Started? 

→ **Next:** [Project Structure](./02-project-structure.md)
