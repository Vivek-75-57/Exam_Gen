# Prompt: Fix Bug

When fixing bugs in ExamForge, follow this systematic approach.

---

## Debugging Process

1. **Identify the Issue**
   - Get error message/stack trace
   - Reproduce the bug
   - Understand expected behavior

2. **Find Root Cause**
   - Check logs
   - Add console statements
   - Trace through code flow

3. **Fix Implementation**
   - Make minimal change
   - Don't refactor during fix
   - Keep fix focused

4. **Test the Fix**
   - Verify bug is gone
   - Check for side effects
   - Test edge cases

5. **Document the Fix**
   - Comment why fix was needed
   - Add test case if applicable
   - Update CHANGELOG

---

## Common Bug Patterns in ExamForge

### Frontend Bugs
- **React State:** Check if state updates are batched
- **API Calls:** Verify response handling
- **Components:** Check prop types and defaults

### Backend Bugs
- **Async/Await:** Ensure promises are awaited
- **Error Handling:** Verify all errors are caught
- **Database:** Check query parameters

---

## Fix Checklist

- [ ] Bug is reproducible
- [ ] Root cause identified
- [ ] Fix is minimal
- [ ] No side effects
- [ ] Tests pass
- [ ] Code commented
- [ ] Git commit message clear

---

## Commit Format for Fixes

```bash
git commit -m "fix: [brief description]"
```

Example:
```bash
git commit -m "fix: handle null response from Groq API"
```
