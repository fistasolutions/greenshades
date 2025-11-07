# Prompt Templates Collection

**Quick Reference Guide | One-Page Cheat Sheet**

**Last Updated:** 2025  
**Purpose:** Copy-paste ready prompts for common AI tasks

---

## Code Generation Prompts

### Generate Function
```
Generate a [language] function that [description]:
- Inputs: [list inputs with types]
- Output: [output type and description]
- Business Rules: [list rules]
- Error Handling: [error handling requirements]
- Examples: [provide examples]
```

### Generate Test Cases
```
Generate unit tests for this function:
[function code]

Cover:
- Happy path scenarios
- Edge cases
- Error cases
- Boundary conditions

Use [testing framework].
```

### Debug Code
```
This code is failing:
[code]

Error message: [error]
Expected behavior: [expected]
Actual behavior: [actual]

Analyze the issue and suggest a fix.
```

---

## Documentation Prompts

### Generate Documentation
```
Generate documentation for this code:
[code]

Include:
- Function/class description
- Parameters and return values
- Usage examples
- Error handling notes
```

### Summarize Code
```
Summarize this code in plain language:
[code]

Explain:
- What it does
- How it works
- Key components
- Dependencies
```

---

## Analysis Prompts

### Analyze Data
```
Analyze this [data type] data:
[data]

Provide:
- Summary statistics
- Key insights
- Anomalies or patterns
- Recommendations
```

### Analyze Payroll Data
```
Analyze this payroll batch for anomalies:
- Employee count: [number]
- Expected gross pay range: $[min]-$[max]
- Flag records with:
  * Gross pay > $[threshold] (outlier)
  * Hours > [threshold] per pay period
  * Negative deductions
  * Employee ID not in master file
Generate report with flagged records and confidence scores.
```

---

## Specification Prompts

### Write Specification
```
Create a specification for [feature/function]:
- Purpose: [what it does]
- Inputs: [inputs with types and constraints]
- Outputs: [outputs with types]
- Business Rules: [rules]
- Error Handling: [error scenarios]
- Examples: [example inputs/outputs]
```

### Extract Specification
```
Extract a specification from this code:
[code]

Include:
- Function signature
- Input/output types
- Business logic
- Error handling
```

---

## Refactoring Prompts

### Refactor Code
```
Refactor this code to improve:
[code]

Improvements needed:
- [improvement 1]
- [improvement 2]
- [improvement 3]

Maintain existing functionality.
```

### Improve Code Quality
```
Review and improve this code:
[code]

Focus on:
- Code clarity
- Performance
- Security
- Best practices
```

---

## Testing Prompts

### Generate Test Data
```
Generate test data for [scenario]:
- Data type: [type]
- Constraints: [constraints]
- Edge cases: [edge cases]
- Volume: [number] records
```

### Test Coverage Analysis
```
Analyze test coverage for this code:
[code]

Tests: [test code]

Identify:
- Missing test cases
- Edge cases not covered
- Error scenarios not tested
```

---

## Support Prompts

### Answer Customer Question
```
Customer asks: "[question]"

Context:
- Product: [product]
- Version: [version]
- Customer type: [type]

Provide a clear, helpful answer.
```

### Classify Support Ticket
```
Classify this support ticket:
[ticket content]

Categories: [list categories]
Priority levels: [list priorities]

Return: Category, Priority, Suggested resolution
```

---

## Business Analysis Prompts

### Generate Report
```
Generate a [report type] report:
- Period: [time period]
- Data source: [source]
- Include: [what to include]
- Format: [format]
- Delivery: [delivery method]
```

### Analyze ROI
```
Calculate ROI for this AI initiative:
- Time saved: [hours/week]
- Hourly rate: $[rate]
- Adoption rate: [percentage]
- Licensing cost: $[cost/year]
- Enablement cost: $[cost]

Provide ROI calculation and percentage.
```

---

## Quick Tips

- **Be Specific:** Include details, constraints, examples
- **Provide Context:** Include relevant background information
- **Use Examples:** Show what good output looks like
- **Iterate:** Refine prompts based on results
- **Review Outputs:** Always verify AI-generated content

---

**For More Prompts:** See lesson files in `01_ai_vs_ai_assisted_vs_ai_driven/` and `03_mcp_and_specdriven_development/`

**Last Updated:** 2025

