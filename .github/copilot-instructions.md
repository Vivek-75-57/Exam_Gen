# GitHub Copilot Instructions

Global instructions for GitHub Copilot when working on ExamForge project.

---

## Core Principles

### Code Quality
- Write clean, readable code
- Follow ESLint/Prettier standards
- Add meaningful comments for complex logic
- Keep functions small and focused

### Backend (Node.js/Express)
- Use async/await (no callbacks)
- Error handling with try-catch
- Validate all inputs
- Use environment variables for config
- Follow RESTful API conventions

### Frontend (React)
- Use functional components with hooks
- Avoid prop drilling (use context/zustand)
- Memoize expensive computations
- Keep components under 300 lines
- Use meaningful component names

### Database & Storage
- Validate data before saving
- Use consistent naming conventions
- Document schema changes
- Handle errors gracefully

---

## Project Structure Rules

```
Backend:  backend/src/{controllers,routes,services}
Frontend: frontend/src/{components,hooks,services,store}
Config:   Use .env files for secrets
Docs:     Keep README files updated
```

---

## Git Commit Standards

- Format: `type: brief description`
- Types: feat, fix, docs, style, refactor, test
- Example: `feat: add bookmark functionality`
- Keep commits atomic and focused

---

## Testing & Documentation

- Add JSDoc comments for functions
- Update README with API changes
- Test before committing
- Update CHANGELOG for major changes

---

## Security

- Never hardcode secrets
- Validate user inputs
- Sanitize outputs
- Use HTTPS in production
- Keep dependencies updated

---

## Performance

- Optimize queries
- Use caching when appropriate
- Minimize re-renders in React
- Monitor API response times
- Profile before optimizing

---

## AI/LLM Best Practices

- Cache LLM responses when possible
- Handle rate limits gracefully
- Provide context in prompts
- Validate generated content
- Log all LLM API calls
