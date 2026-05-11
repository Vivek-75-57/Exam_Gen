# Prompt: Create API Endpoint

When creating new API endpoints for ExamForge, follow this pattern.

---

## Requirements

When I ask to create an API endpoint, ensure:

1. **REST Conventions**
   - POST for create
   - GET for read
   - PUT/PATCH for update
   - DELETE for remove

2. **Error Handling**
   ```javascript
   try {
     // logic
   } catch (error) {
     res.status(500).json({ error: error.message });
   }
   ```

3. **Input Validation**
   - Check required fields
   - Validate data types
   - Return 400 for invalid input

4. **Response Format**
   ```javascript
   {
     success: true,
     data: { /* result */ },
     message: "Operation successful"
   }
   ```

5. **Documentation**
   - Add JSDoc comment
   - Document parameters
   - Document response structure
   - Add example usage

---

## Template

```javascript
/**
 * @route   [METHOD] /api/path
 * @param   {type} paramName - Description
 * @returns {object} { success, data, message }
 * @example
 * POST /api/endpoint
 * { "field": "value" }
 */
router.[method]('/path', async (req, res) => {
  try {
    // Validate input
    const { field } = req.body;
    if (!field) {
      return res.status(400).json({ error: 'Field required' });
    }

    // Process
    const result = await service.process(field);

    // Respond
    res.json({ success: true, data: result });
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});
```

---

## Checklist

- [ ] Follows REST conventions
- [ ] Has error handling
- [ ] Validates inputs
- [ ] Returns proper status codes
- [ ] Has JSDoc comments
- [ ] Tested with curl/Postman
- [ ] Added to routes/exportRoutes.js
