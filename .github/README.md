# ExamForge GitHub Configuration

Professional GitHub Copilot customization and workflow setup.

---

## 📁 Structure

```
.github/
├── copilot-instructions.md    (Global rules & standards)
├── prompts/                    (Reusable task templates)
│   ├── create-api.prompt.md    (API endpoint creation)
│   ├── fix-bug.prompt.md       (Bug fixing guide)
│   └── refactor.prompt.md      (Code refactoring guide)
└── agents/                     (Advanced agent configs)
```

---

## 📖 Usage

### Global Instructions
The `copilot-instructions.md` file defines:
- Code quality standards
- Backend conventions (Node.js/Express)
- Frontend conventions (React)
- Git commit standards
- Security practices

### Prompts
Use these prompts when asking Copilot to help with specific tasks:

- **`create-api.prompt.md`** - When building new API endpoints
- **`fix-bug.prompt.md`** - When debugging issues
- **`refactor.prompt.md`** - When improving existing code

---

## 🎯 How to Use

### When Creating an API Endpoint
1. Reference: `create-api.prompt.md`
2. Ask Copilot to create endpoint following the template
3. Use the checklist to verify completeness

### When Fixing a Bug
1. Reference: `fix-bug.prompt.md`
2. Follow the debugging process
3. Use the fix checklist

### When Refactoring
1. Reference: `refactor.prompt.md`
2. Ensure tests pass before & after
3. Use the refactor checklist

---

## ✅ Standards

### Code Quality
- ESLint/Prettier compliant
- JSDoc comments for functions
- Meaningful variable names
- Small, focused functions

### Backend
- async/await (no callbacks)
- Error handling with try-catch
- Input validation
- RESTful conventions

### Frontend
- Functional components with hooks
- No prop drilling
- Memoization for expensive ops
- Under 300 lines per component

### Git
- Format: `type: description`
- Types: feat, fix, docs, style, refactor, test
- Atomic, focused commits

---

## 🔒 Security

- Never hardcode secrets
- Validate all inputs
- Sanitize outputs
- Keep dependencies updated
- Use environment variables for config

---

## 📚 References

- [GitHub Copilot Docs](https://docs.github.com/en/copilot)
- [ExamForge README](../README.md)
- [API Documentation](../API_CALLS_EXPLAINED.md)

---

**Follow these standards for consistent, professional code! 🚀**
