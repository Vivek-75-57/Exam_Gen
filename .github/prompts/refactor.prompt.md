# Prompt: Refactor Code

When refactoring ExamForge code, improve quality without changing functionality.

---

## Refactoring Guidelines

1. **Before Refactoring**
   - Ensure tests pass
   - Understand current code flow
   - Have clear goals
   - Commit current state

2. **During Refactoring**
   - Change one thing at a time
   - Keep tests passing
   - Maintain same functionality
   - Comment complex sections

3. **After Refactoring**
   - Run all tests
   - Performance testing
   - Code review
   - Document changes

---

## Common Refactorings

### Extract Function
```javascript
// Before
const result = data.filter(x => x > 10).map(x => x * 2);

// After
const filterData = (data) => data.filter(x => x > 10);
const doubleValues = (data) => data.map(x => x * 2);
const result = doubleValues(filterData(data));
```

### Extract Service
```javascript
// Move business logic to service layer
// Before: In controller
// After: In services/ folder
```

### Consolidate Imports
```javascript
// Before
import { useState } from 'react';
import { useCallback } from 'react';

// After
import { useState, useCallback } from 'react';
```

### Remove Duplication
- DRY principle
- Extract common patterns
- Create reusable utilities

---

## What NOT to Do

❌ Don't refactor without tests
❌ Don't change functionality
❌ Don't refactor everything at once
❌ Don't skip documentation
❌ Don't ignore performance

---

## Refactor Checklist

- [ ] Tests pass before & after
- [ ] Same functionality
- [ ] Improved readability
- [ ] Better performance (or neutral)
- [ ] Code commented
- [ ] No console warnings
- [ ] Commit message clear

---

## Commit Format

```bash
git commit -m "refactor: [what was improved]"
```

Example:
```bash
git commit -m "refactor: extract question generation logic to service"
```
