# Top AI Commands Cheat Sheet

**Quick Reference Guide | One-Page Cheat Sheet**

---

## SpecKit Commands

### `/specify function_name`
Create or update a specification
```
/specify calculate_overtime_pay
```

### `/extract function_name`
Extract specification from existing code
```
/extract calculate_overtime_pay
```

### `/implement function_name`
Generate code from specification
```
/implement calculate_overtime_pay
```

### `/testgen function_name`
Generate tests from specification
```
/testgen calculate_overtime_pay
```

### `/review function_name`
Review code against specification
```
/review calculate_overtime_pay
```

### `/autofix function_name`
Automatically fix issues in code
```
/autofix calculate_overtime_pay
```

### `/trace function_name`
Trace code back to specification
```
/trace calculate_overtime_pay
```

### `/policyguard function_name`
Check code against security and policy rules
```
/policyguard calculate_overtime_pay
```

---

## Common AI Prompts

### Code Generation
```
Generate a function that [requirement] with error handling
Write unit tests for this function covering edge cases
Explain why this code is failing and suggest a fix
```

### Documentation
```
Summarize this code and generate documentation
Create a README for this project
Generate API documentation from this code
```

### Debugging
```
Why is this code failing? [paste code]
Suggest improvements for this function
Identify potential security vulnerabilities in this code
```

### Analysis
```
Analyze this payroll data for anomalies
Classify these transactions into tax codes
Predict processing time for this payroll run
```

---

## GitHub Copilot / Cursor Shortcuts

### Code Completion
- Type function signature → Copilot suggests implementation
- Type comment describing code → Copilot generates code
- Type `// TODO:` → Copilot suggests implementation

### Chat Commands (Cursor)
- `@code` - Reference code in chat
- `@docs` - Reference documentation
- `@web` - Search web for information

---

## Quick Tips

- **Be Specific:** Clear prompts = better AI outputs
- **Provide Context:** Include function names, variable types, business rules
- **Iterate:** AI suggestions are starting points, refine as needed
- **Review Always:** Verify AI-generated code before using
- **Test Thoroughly:** AI can generate incorrect code

---

**Last Updated:** 2025  
**Version:** 1.0

