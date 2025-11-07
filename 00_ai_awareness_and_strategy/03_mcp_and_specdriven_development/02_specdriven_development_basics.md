# Spec-Driven Development Basics

**Title:** Spec-Driven Development Basics  
**Audience:** Engineering, QA, Product  
**Duration:** 60-90 minutes  
**Prerequisites:** `01_ai_vs_ai_assisted_vs_ai_driven/01_ai_driven_development.md` (recommended)

---

## Learning Objectives

By the end of this lesson, you will be able to:

- Define Spec-Driven Development and understand its principles
- Write effective specifications for AI code generation
- Use SpecKit commands (/specify, /extract, /implement, /autofix, /review, /testgen, /trace, /policyguard)
- Apply Spec-Driven Development to real Greenshades use cases
- Understand the workflow from specification to implementation
- Evaluate when to use Spec-Driven Development

---

## Core Content

### What is Spec-Driven Development?

**Spec-Driven Development** is a development paradigm where developers write specifications (what the code should do) and AI generates the implementation (how to do it). The specification serves as the single source of truth for requirements, implementation, and tests.

**Key Principles:**
1. **Specification First:** Write specs before implementation
2. **AI Generation:** AI generates code from specs
3. **Spec as Truth:** Spec defines requirements, implementation, and tests
4. **Iterative Refinement:** Refine specs based on AI output
5. **Automated Testing:** Tests generated from specs

**Benefits:**
- ✅ Faster development (50-70% time savings)
- ✅ Better alignment between requirements and implementation
- ✅ Automated test generation
- ✅ Reduced bugs (specs catch issues early)
- ✅ Better documentation (specs are documentation)

---

### SpecKit Commands Overview

**SpecKit** is a tool that implements Spec-Driven Development. It provides commands for the full development lifecycle:

```mermaid
graph LR
    A[/specify] --> B[/extract]
    B --> C[/implement]
    C --> D[/testgen]
    D --> E[/review]
    E --> F[/autofix]
    F --> G[/trace]
    G --> H[/policyguard]
    
    style A fill:#90EE90
    style C fill:#87CEEB
    style D fill:#FFD700
    style E fill:#DDA0DD
```

**Command Reference:**

1. **`/specify`** - Create or update a specification
2. **`/extract`** - Extract specification from existing code
3. **`/implement`** - Generate code from specification
4. **`/autofix`** - Automatically fix issues in generated code
5. **`/review`** - Review code against specification
6. **`/testgen`** - Generate tests from specification
7. **`/trace`** - Trace code back to specification
8. **`/policyguard`** - Check code against security and policy rules

---

### Command 1: `/specify` - Create Specification

**Purpose:** Create or update a specification for a feature or function.

**Usage:**
```
/specify function_name
```

**Example:**
```
/specify calculate_overtime_pay

Specification:
- Function: calculate_overtime_pay
- Inputs:
  - hours_worked: number (0-168)
  - hourly_rate: number (> 0)
- Output: number (gross pay including overtime)
- Rules:
  - If hours_worked <= 40: return hours_worked * hourly_rate
  - If hours_worked > 40:
    - regular_pay = 40 * hourly_rate
    - overtime_pay = (hours_worked - 40) * hourly_rate * 1.5
    - return regular_pay + overtime_pay
- Error Handling:
  - Validate hours_worked is number and 0-168
  - Validate hourly_rate is number and > 0
  - Raise ValueError for invalid inputs
- Examples:
  - calculate_overtime_pay(40, 20) = 800
  - calculate_overtime_pay(50, 20) = 1100
  - calculate_overtime_pay(-5, 20) = ValueError
```

**Output:** Specification saved and ready for implementation.

---

### Command 2: `/extract` - Extract Specification from Code

**Purpose:** Extract a specification from existing code (reverse engineering).

**Usage:**
```
/extract function_name
```

**Example:**
```
/extract calculate_overtime_pay

Existing Code:
def calculate_overtime_pay(hours_worked, hourly_rate):
    if hours_worked > 40:
        regular = 40 * hourly_rate
        overtime = (hours_worked - 40) * hourly_rate * 1.5
        return regular + overtime
    return hours_worked * hourly_rate

Extracted Specification:
- Function: calculate_overtime_pay
- Inputs: hours_worked (number), hourly_rate (number)
- Output: number
- Rules: [extracted from code]
```

**Use Case:** Document legacy code, understand existing implementations.

---

### Command 3: `/implement` - Generate Code from Specification

**Purpose:** Generate implementation code from a specification.

**Usage:**
```
/implement function_name
```

**Example:**
```
/implement calculate_overtime_pay

Generated Code:
def calculate_overtime_pay(hours_worked: float, hourly_rate: float) -> float:
    """
    Calculate gross pay including overtime.
    
    Args:
        hours_worked: Hours worked (0-168)
        hourly_rate: Hourly rate (> 0)
    
    Returns:
        Gross pay including overtime
    
    Raises:
        ValueError: If inputs are invalid
    """
    if not isinstance(hours_worked, (int, float)) or hours_worked < 0 or hours_worked > 168:
        raise ValueError(f"hours_worked must be a number between 0 and 168, got {hours_worked}")
    
    if not isinstance(hourly_rate, (int, float)) or hourly_rate <= 0:
        raise ValueError(f"hourly_rate must be a positive number, got {hourly_rate}")
    
    if hours_worked <= 40:
        return hours_worked * hourly_rate
    else:
        regular_pay = 40 * hourly_rate
        overtime_pay = (hours_worked - 40) * hourly_rate * 1.5
        return regular_pay + overtime_pay
```

**Output:** Generated code ready for review and testing.

---

### Command 4: `/testgen` - Generate Tests

**Purpose:** Generate test cases from specification.

**Usage:**
```
/testgen function_name
```

**Example:**
```
/testgen calculate_overtime_pay

Generated Tests:
def test_calculate_overtime_pay_normal_hours():
    assert calculate_overtime_pay(40, 20) == 800

def test_calculate_overtime_pay_with_overtime():
    assert calculate_overtime_pay(50, 20) == 1100

def test_calculate_overtime_pay_invalid_hours():
    with pytest.raises(ValueError):
        calculate_overtime_pay(-5, 20)

def test_calculate_overtime_pay_invalid_rate():
    with pytest.raises(ValueError):
        calculate_overtime_pay(40, 0)
```

**Output:** Comprehensive test suite covering happy path, edge cases, and error handling.

---

### Command 5: `/review` - Review Code Against Specification

**Purpose:** Review generated code to ensure it matches the specification.

**Usage:**
```
/review function_name
```

**Example:**
```
/review calculate_overtime_pay

Review Results:
✅ Implements all specification rules
✅ Error handling matches specification
✅ Type hints match specification
⚠️ Missing: Edge case for hours_worked = 0
⚠️ Suggestion: Add logging for overtime calculations
```

**Output:** Review report with compliance status and suggestions.

---

### Command 6: `/autofix` - Automatically Fix Issues

**Purpose:** Automatically fix issues found in code review.

**Usage:**
```
/autofix function_name
```

**Example:**
```
/autofix calculate_overtime_pay

Fixed Issues:
- Added edge case handling for hours_worked = 0
- Added logging for overtime calculations
- Improved error messages
```

**Output:** Updated code with fixes applied.

---

### Command 7: `/trace` - Trace Code to Specification

**Purpose:** Trace code back to the specification that generated it.

**Usage:**
```
/trace function_name
```

**Example:**
```
/trace calculate_overtime_pay

Trace Results:
- Code line 15: Implements "if hours_worked <= 40" rule
- Code line 18: Implements "overtime_pay = (hours_worked - 40) * hourly_rate * 1.5" rule
- Code line 12: Implements "validate hours_worked" error handling
```

**Use Case:** Understand how code relates to specs, maintain traceability.

---

### Command 8: `/policyguard` - Check Against Policies

**Purpose:** Check code against security and policy rules.

**Usage:**
```
/policyguard function_name
```

**Example:**
```
/policyguard calculate_overtime_pay

Policy Check Results:
✅ No hardcoded credentials
✅ Input validation present
✅ Error handling implemented
⚠️ Consider: Add rate limiting for high-volume calls
⚠️ Consider: Add audit logging for financial calculations
```

**Output:** Policy compliance report with recommendations.

---

## Mini-Lab: Spec-Driven Development Workflow

**Scenario:** Build a payroll tax calculation function using Spec-Driven Development.

**Step 1: Write Specification**
```
/specify calculate_state_tax

Specification:
- Function: calculate_state_tax
- Inputs:
  - income: number (>= 0)
  - state: string (2-letter state code: "CA", "NY", "TX")
- Output: number (state tax amount)
- Rules:
  - California (CA):
    - If income < 10000: tax = income * 0.01
    - If income < 50000: tax = 100 + (income - 10000) * 0.05
    - If income >= 50000: tax = 2100 + (income - 50000) * 0.10
  - New York (NY):
    - If income < 8000: tax = income * 0.04
    - If income < 11000: tax = 320 + (income - 8000) * 0.045
    - If income >= 11000: tax = 455 + (income - 11000) * 0.0525
  - Texas (TX): tax = 0 (no state income tax)
- Error Handling:
  - Validate income >= 0
  - Validate state is valid 2-letter code
  - Raise ValueError for invalid inputs
```

**Step 2: Generate Implementation**
```
/implement calculate_state_tax
```
*(AI generates code from specification)*

**Step 3: Generate Tests**
```
/testgen calculate_state_tax
```
*(AI generates comprehensive test suite)*

**Step 4: Review Code**
```
/review calculate_state_tax
```
*(Check compliance with specification)*

**Step 5: Fix Issues**
```
/autofix calculate_state_tax
```
*(Auto-fix any issues found)*

**Step 6: Check Policies**
```
/policyguard calculate_state_tax
```
*(Verify security and compliance)*

**Step 7: Trace to Specification**
```
/trace calculate_state_tax
```
*(Maintain traceability)*

---

## Try It: Exercise

**Scenario:** You need to build a function that validates payroll data.

**Task:** Write a specification using `/specify` format, then describe what `/implement` and `/testgen` would generate.

**Function Requirements:**
- Validates employee ID exists in database
- Checks hours worked are between 0 and 80
- Ensures gross pay is positive
- Validates tax deductions don't exceed gross pay

**Solution:**
```
/specify validate_payroll_data

Specification:
- Function: validate_payroll_data
- Inputs:
  - employee_id: string
  - hours_worked: number
  - gross_pay: number
  - tax_deductions: number
  - employee_db: database connection
- Output: tuple (is_valid: bool, errors: list)
- Rules:
  - Check employee_id exists in employee_db
  - Validate hours_worked is number and 0 <= hours_worked <= 80
  - Validate gross_pay is number and > 0
  - Validate tax_deductions is number and 0 <= tax_deductions <= gross_pay
  - Return (True, []) if all validations pass
  - Return (False, [error_messages]) if any validation fails
- Error Handling:
  - Handle database connection errors
  - Return clear error messages for each validation failure
```

**What `/implement` would generate:**
- Function with database query for employee_id
- Validation logic for each rule
- Error message generation
- Return tuple with validation results

**What `/testgen` would generate:**
- Tests for valid payroll data
- Tests for invalid employee_id
- Tests for hours_worked out of range
- Tests for negative gross_pay
- Tests for deductions exceeding gross_pay
- Tests for database connection errors

---

## Role-Based "How This Helps You"

### Developers
- **Faster Development:** Generate code from specs in minutes vs. hours
- **Better Quality:** Specs catch issues early, tests generated automatically
- **Documentation:** Specs serve as living documentation
- **Maintainability:** Trace code back to specs for updates

### QA Engineers
- **Test Generation:** AI generates comprehensive test suites from specs
- **Coverage:** Specs ensure all requirements are tested
- **Traceability:** Tests trace back to specifications
- **Quality:** Automated test generation improves coverage

### Product Managers
- **Clear Requirements:** Specs force clarity on what needs to be built
- **Faster Delivery:** 50-70% faster development cycles
- **Alignment:** Specs ensure implementation matches requirements
- **Documentation:** Specs serve as product documentation

---

## Key Takeaways

1. **Spec-Driven Development:** Write specs, AI generates implementation and tests

2. **SpecKit Commands:** `/specify`, `/extract`, `/implement`, `/autofix`, `/review`, `/testgen`, `/trace`, `/policyguard`

3. **Workflow:** Specify → Implement → Test → Review → Fix → Policy Check → Trace

4. **Benefits:** 50-70% faster development, better quality, automated testing, better documentation

5. **Best Practices:** Write clear, detailed specs; review AI-generated code; iterate based on feedback

---

## 5-Question Quiz

### Question 1 (Multiple Choice)
What is the first step in Spec-Driven Development?

a) Generate code  
b) Write tests  
c) Write specification  
d) Review code

**Answer:** c) Write specification

---

### Question 2 (True/False)
SpecKit's `/testgen` command generates tests from the specification, not from the code.

**Answer:** True

---

### Question 3 (Short Answer)
Name one SpecKit command and its purpose.

**Answer:** Examples: `/specify` (create specification), `/implement` (generate code), `/testgen` (generate tests), `/review` (review code), `/autofix` (fix issues), `/trace` (trace to spec), `/policyguard` (check policies). (Accept any one)

---

### Question 4 (Multiple Choice)
Which command checks code against security and policy rules?

a) `/review`  
b) `/policyguard`  
c) `/trace`  
d) `/autofix`

**Answer:** b) `/policyguard`

---

### Question 5 (Short Answer)
Give one benefit of Spec-Driven Development.

**Answer:** Examples: Faster development (50-70% time savings), better quality, automated test generation, better documentation, alignment between requirements and implementation. (Accept any one)

---

## One-Page Cheat Sheet

### Spec-Driven Development
- **Definition:** Write specs, AI generates implementation and tests
- **Workflow:** Specify → Implement → Test → Review → Fix → Policy Check → Trace

### SpecKit Commands
- **`/specify`:** Create or update specification
- **`/extract`:** Extract spec from existing code
- **`/implement`:** Generate code from specification
- **`/autofix`:** Automatically fix issues
- **`/review`:** Review code against specification
- **`/testgen`:** Generate tests from specification
- **`/trace`:** Trace code back to specification
- **`/policyguard`:** Check against security and policy rules

### Benefits
- 50-70% faster development
- Better quality (specs catch issues early)
- Automated test generation
- Better documentation (specs are documentation)
- Alignment between requirements and implementation

### Best Practices
- Write clear, detailed specifications
- Include examples and edge cases
- Review AI-generated code thoroughly
- Iterate based on feedback
- Maintain traceability (specs → code → tests)

### Specification Format
- Function name, inputs, outputs, rules, error handling, examples

---

## Phrases & Prompts That Work

**When using SpecKit:**
- "`/specify function_name` to create a specification"
- "`/implement function_name` to generate code from spec"
- "`/testgen function_name` to generate tests"

**When writing specifications:**
- "Be specific: include inputs, outputs, rules, error handling, examples"
- "Specs should be clear enough for AI to generate correct code"

**When reviewing AI-generated code:**
- "Does the code match the specification? Check all rules are implemented."
- "Are edge cases handled? Test with boundary values."

---

## Security & Compliance Note

⚠️ **Red Flags Checklist:**
- [ ] Always review AI-generated code, especially for financial calculations (payroll, tax)
- [ ] Use `/policyguard` to check security and compliance
- [ ] Verify business logic matches requirements (AI may misunderstand domain rules)
- [ ] Test AI-generated code thoroughly before production deployment
- [ ] Maintain audit trail of specifications and generated code

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed security guidelines.

---

**Next Lesson:** `03_ai_agents_orchestration_flow.md`

