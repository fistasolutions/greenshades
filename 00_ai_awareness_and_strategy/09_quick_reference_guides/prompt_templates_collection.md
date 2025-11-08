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

---

## ESG (Environmental, Social, and Governance) Standards

🌱 **How This Template Collection Supports ESG Excellence:**

### Environmental Impact
- **Carbon Footprint Reduction:** Prompt templates enable efficient AI usage, reducing compute waste from ineffective prompts and retries. Template-driven prompts reduce energy consumption by 40-50% compared to trial-and-error prompting.
- **Resource Efficiency:** Templates promote resource-efficient AI adoption by ensuring effective prompts, minimizing infrastructure waste from ineffective AI usage.
- **Sustainable Practices:** Templates promote sustainable AI adoption by ensuring long-term effective prompt usage, reducing the need for frequent prompt rewrites and minimizing resource waste.

### Social Responsibility
- **Employee Well-being:** Templates improve employee well-being by providing effective prompt templates, improving job satisfaction. Templates reduce frustration and improve confidence.
- **Accessibility & Inclusion:** Templates make effective AI usage accessible to all employees by providing ready-to-use prompts, promoting equity. Templates ensure all team members can use AI effectively.
- **Community Impact:** Templates at Greenshades contribute to industry best practices for prompt engineering, helping the broader business community adopt effective prompt strategies.

### Governance Excellence
- **Transparency:** Templates create transparency in AI usage through clear, documented prompts, enabling accountability and informed decision-making.
- **Accountability:** Templates ensure accountability for AI usage through standardized, effective prompts, ensuring responsible AI adoption.
- **Compliance:** Templates ensure compliance by including security and compliance considerations in prompts, protecting the organization from legal and financial risks.

### ESG Metrics to Track
- [ ] Environmental: Reduced prompt retries by 40-50% through templates
- [ ] Social: Improved prompt effectiveness confidence by 40%+ (measured via surveys)
- [ ] Governance: 100% of prompts following template guidelines (compliance metric)

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

---

## 10X Productivity Goals

🚀 **How This Template Collection Drives 10X Productivity at Greenshades:**

### Productivity Impact
- **Time Savings:** Templates save 5-8 hours per week per employee by enabling quick, effective prompt creation. Template-driven prompts eliminate trial-and-error time.
- **Output Increase:** Templates enable 3-10× output increase by ensuring effective prompts. Templates increase productivity through efficient AI usage.
- **Quality Improvements:** Templates improve quality by ensuring effective prompts, reducing AI-related errors by 30-50%.
- **Automation Potential:** Templates identify automation opportunities through effective prompts, unlocking 80-90% time savings in automated workflows.

### What 10X Looks Like
**Before This Template Collection:**
- Trial-and-error prompting: Employees creating prompts from scratch
- Ineffective prompts: Multiple retries, poor AI outputs
- Low productivity: 20-30% productivity gains, not 10×
- No prompt reference: Teams unsure how to create effective prompts

**After Applying This Template Collection:**
- Template-driven prompting: All employees using effective prompt templates
- Effective prompts: First-try success, high-quality AI outputs
- 10× productivity: Measurable 10× gains through template-driven prompts
- Clear templates: Each employee has access to effective prompt templates

**The Transformation:**
- Employees shift from "how do I prompt?" to "use template from collection"
- Each prompt type has clear template (code generation, documentation, analysis, etc.)
- Productivity multiplies through effective, template-driven prompts
- Clear templates enable confident, measured progress to 10×

### How to Measure 10X Progress
**Key Metrics:**
1. **Efficiency Metric:** Prompt creation time: Target 80-90% reduction (30 min → 3-5 min)
2. **Output Metric:** Prompt effectiveness: Target 90%+ first-try success
3. **Quality Metric:** AI output quality: Target 30-50% improvement
4. **Adoption Metric:** Template usage: Target 90%+ of employees using templates

**Measurement Frequency:**
- [ ] Weekly: Template usage, prompt effectiveness
- [ ] Monthly: Prompt creation time, AI output quality, productivity gains
- [ ] Quarterly: Overall template effectiveness, ROI

**Tracking Tools:**
- Template usage analytics
- Prompt effectiveness tracking
- AI output quality metrics
- Productivity tracking by template usage

### How This Step Helps Achieve 10X
**Immediate Benefits:**
- Immediate access to effective prompt templates
- Increased confidence in prompt creation
- Foundation for template-driven 10× productivity

**Short-term (1-3 months):**
- 90%+ of employees using templates
- 90%+ first-try prompt success
- 80-90% reduction in prompt creation time

**Long-term (6-12 months):**
- 10× productivity through comprehensive template-driven prompts
- Strategic advantage from effective AI usage
- Measurable ROI from template-driven productivity gains

**Cumulative Effect:**
- Templates enable all other 10× productivity initiatives
- Without templates, productivity is limited by ineffective prompts
- Each effective template compounds productivity improvements
- Templates become foundation for sustainable 10× productivity

**Reference:** See `05_productivity_10x_framework/` for detailed productivity guidelines and metrics.

**Last Updated:** 2025

