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
- Use SpecKit commands (/speckit.constitution, /speckit.specify, /speckit.plan, /speckit.tasks, /speckit.implement, /speckit.clarify, /speckit.analyze, /speckit.checklist)
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
    A[/speckit.constitution/] --> B[/speckit.specify/]
    B --> C[/speckit.plan/]
    C --> D[/speckit.tasks/]
    D --> E[/speckit.implement/]
    E --> F[/speckit.clarify/]
    F --> G[/speckit.analyze/]
    G --> H[/speckit.checklist/]
    
    style A fill:#90EE90
    style C fill:#87CEEB
    style D fill:#FFD700
    style E fill:#DDA0DD
```

**Command Reference:**

1. **`/speckit.constitution`** - Establish or update the system constitution
2. **`/speckit.specify`** - Create or update a specification
3. **`/speckit.plan`** - Plan implementation steps from the specification
4. **`/speckit.tasks`** - Generate actionable task breakdowns
5. **`/speckit.implement`** - Generate code from specification
6. **`/speckit.clarify`** - Resolve ambiguities and request clarifications
7. **`/speckit.analyze`** - Trace outputs back to the specification
8. **`/speckit.checklist`** - Validate against policy and quality checklists

---

### Command 1: `/speckit.constitution` - Establish the Constitution

**Purpose:** Create or update the high-level constitution that defines mission, guardrails, and quality standards for the system or feature.

**Usage:**
```
/speckit.constitution initiative_name
```

**Example:**
```
/speckit.constitution payroll_compliance_suite

Constitution:
- Mission: Deliver compliant, auditable payroll calculations for mid-market employers.
- Quality Standards:
  - All monetary calculations must use decimal with 2-place precision.
  - Every automated decision requires traceable justification.
- Guardrails:
  - Never store personally identifiable information (PII) outside encrypted storage.
  - Flag and review any calculation that deviates more than 5% from historical norms.
- Collaboration Rules:
  - Document rationale for policy updates within 24 hours.
  - Surface unresolved clarifications before implementation.
```

**Output:** Constitution captured and ready to inform downstream specifications.

---

### Command 2: `/speckit.specify` - Create or Update a Specification

**Purpose:** Capture a precise, testable specification for a function, workflow, or capability.

**Usage:**
```
/speckit.specify function_name
```

**Example:**
```
/speckit.specify calculate_overtime_pay

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

**Use Case:** Define a new capability or revise an existing behavior before implementation.

---

### Command 3: `/speckit.plan` - Build the Implementation Plan

**Purpose:** Translate the specification into a sequenced plan that outlines architecture, dependencies, and checkpoints.

**Usage:**
```
/speckit.plan function_name
```

**Example:**
```
/speckit.plan calculate_overtime_pay

Plan:
1. Validate inputs (type and range checks) before computations.
2. Separate regular hours calculation from overtime logic.
3. Use Decimal for monetary math to avoid floating-point drift.
4. Create helper function for overtime multiplier to support future policy updates.
5. Document edge cases (0 hours, maximum allowable hours, invalid inputs).
6. Identify integration points for audit logging.
```

**Output:** A clear plan that developers can follow before breaking work into tasks.

---

### Command 4: `/speckit.tasks` - Generate Actionable Tasks

**Purpose:** Produce an actionable task list derived from the plan that can be tracked in project tooling.

**Usage:**
```
/speckit.tasks function_name
```

**Example:**
```
/speckit.tasks calculate_overtime_pay

Task Breakdown:
- [ ] Create validation helper ensuring hours_worked is between 0-168.
- [ ] Implement Decimal-based payroll calculation module.
- [ ] Add overtime helper covering rate multipliers.
- [ ] Write docstring describing algorithm and edge cases.
- [ ] Emit audit log when overtime is applied.
- [ ] Add monitoring hook for anomaly detection.
```

**Output:** Ready-to-track tasks that align directly with the specification and plan.

---

### Command 5: `/speckit.implement` - Generate Code from Specification

**Purpose:** Produce implementation code that satisfies the approved specification.

**Usage:**
```
/speckit.implement function_name
```

**Example:**
```
/speckit.implement calculate_overtime_pay

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

**Output:** Production-ready code aligned with the plan, tasks, and specification.

---

### Command 6: `/speckit.clarify` - Resolve Ambiguities

**Purpose:** Surface questions, assumptions, or missing details that must be clarified with stakeholders.

**Usage:**
```
/speckit.clarify function_name
```

**Example:**
```
/speckit.clarify calculate_overtime_pay

Clarification Requests:
1. Should holiday pay follow the same overtime multiplier?
2. Do salaried employees follow a different overtime rule set?
3. What logging destination should receive overtime events?
4. Are fractional hours (e.g., 37.5) supported?
5. Should we cap overtime at a maximum number of hours per week?
```

**Output:** Structured questions to resolve before or during implementation.

---

### Command 7: `/speckit.analyze` - Analyze Traceability

**Purpose:** Examine code, tests, or outputs and map them back to the originating specification statements.

**Usage:**
```
/speckit.analyze function_name
```

**Example:**
```
/speckit.analyze calculate_overtime_pay

Traceability Map:
- Code line 21 implements rule: "If hours_worked <= 40"
- Code line 27 implements rule: "Overtime multiplier 1.5x"
- Tests test_calculate_overtime_pay_with_overtime maps to example: hours_worked=50
- Logging hook maps to constitution guardrail: "Flag deviations > 5%"
```

**Use Case:** Maintain end-to-end traceability for audits, compliance, and debugging.

---

### Command 8: `/speckit.checklist` - Run Policy and Quality Checklists

**Purpose:** Validate deliverables against organizational policies, security requirements, and quality standards.

**Usage:**
```
/speckit.checklist function_name
```

**Example:**
```
/speckit.checklist calculate_overtime_pay

Checklist Results:
✅ No hardcoded credentials
✅ Input validation present
✅ Error handling implemented
⚠️ Consider: Add rate limiting for high-volume calls
⚠️ Consider: Add audit logging for financial calculations
```

**Output:** Policy and quality compliance report with recommendations.

---

## Mini-Lab: Spec-Driven Development Workflow

**Scenario:** Build a payroll tax calculation function using Spec-Driven Development.

**Step 1: Establish the Constitution**
```
/speckit.constitution state_tax_platform

Constitution:
- Mission: Deliver compliant, auditable state tax calculations.
- Guardrails: No hardcoded rates; source tables must be versioned.
- Quality: Decimal math only, full traceability for rate changes.
```

**Step 2: Capture the Specification**
```
/speckit.specify calculate_state_tax

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

**Step 3: Build the Plan**
```
/speckit.plan calculate_state_tax
```
*(AI derives architectural steps, dependencies, and checkpoints)*

**Step 4: Generate Tasks**
```
/speckit.tasks calculate_state_tax
```
*(AI produces an actionable task list aligned to the plan)*

**Step 5: Generate Implementation**
```
/speckit.implement calculate_state_tax
```
*(AI generates code from the specification)*

**Step 6: Clarify Ambiguities**
```
/speckit.clarify calculate_state_tax
```
*(AI surfaces open questions or assumptions)*

**Step 7: Analyze Traceability**
```
/speckit.analyze calculate_state_tax
```
*(AI maps code, tests, and logs back to the specification and constitution)*

**Step 8: Run the Checklist**
```
/speckit.checklist calculate_state_tax
```
*(AI verifies compliance with policy, security, and quality requirements)*

---

## Try It: Exercise

**Scenario:** You need to build a function that validates payroll data.

**Task:** Write a specification using `/speckit.specify` format, then describe what `/speckit.plan` and `/speckit.implement` would generate.

**Function Requirements:**
- Validates employee ID exists in database
- Checks hours worked are between 0 and 80
- Ensures gross pay is positive
- Validates tax deductions don't exceed gross pay

**Solution:**
```
/speckit.specify validate_payroll_data

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

**What `/speckit.plan` would generate:**
- Identify validation helper modules needed.
- Sequence steps: fetch employee, validate numeric ranges, compare deductions.
- Highlight dependency on employee database adapter.
- Note requirement for structured error payloads.
- Flag need for logging invalid attempts.

**What `/speckit.implement` would generate:**
- Function with database query for employee_id.
- Validation logic for each rule.
- Structured error message generation.
- Tuple return containing validity flag and error collection.

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

1. **Spec-Driven Development:** Define a constitution and specs, then let AI plan, implement, and validate.

2. **SpecKit Commands:** `/speckit.constitution`, `/speckit.specify`, `/speckit.plan`, `/speckit.tasks`, `/speckit.implement`, `/speckit.clarify`, `/speckit.analyze`, `/speckit.checklist`

3. **Workflow:** Constitution → Specify → Plan → Tasks → Implement → Clarify → Analyze → Checklist

4. **Benefits:** 50-70% faster development, better quality, automated testing, better documentation

5. **Best Practices:** Write clear, detailed specs; review AI-generated code; iterate based on feedback

---

## 5-Question Quiz

### Question 1 (Multiple Choice)
What is the first step in the SpecKit workflow?

a) Generate tasks  
b) Implement code  
c) Establish the constitution  
d) Run the checklist

**Answer:** c) Establish the constitution

---

### Question 2 (True/False)
SpecKit's `/speckit.tasks` command generates actionable work items from the approved plan.

**Answer:** True

---

### Question 3 (Short Answer)
Name one SpecKit command and its purpose.

**Answer:** Examples: `/speckit.constitution` (define guardrails), `/speckit.specify` (create specification), `/speckit.plan` (derive implementation plan), `/speckit.tasks` (break work into tasks), `/speckit.implement` (generate code), `/speckit.clarify` (surface questions), `/speckit.analyze` (map outputs back to specs), `/speckit.checklist` (run policy checks). (Accept any one)

---

### Question 4 (Multiple Choice)
Which command checks code against security and policy rules?

a) `/speckit.implement`  
b) `/speckit.checklist`  
c) `/speckit.analyze`  
d) `/speckit.clarify`

**Answer:** b) `/speckit.checklist`

---

### Question 5 (Short Answer)
Give one benefit of Spec-Driven Development.

**Answer:** Examples: Faster development (50-70% time savings), better quality, automated test generation, better documentation, alignment between requirements and implementation. (Accept any one)

---

## One-Page Cheat Sheet

### Spec-Driven Development
- **Definition:** Establish a constitution, capture specifications, and let AI plan, implement, and validate.
- **Workflow:** Constitution → Specify → Plan → Tasks → Implement → Clarify → Analyze → Checklist

### SpecKit Commands
- **`/speckit.constitution`:** Define mission, guardrails, and success criteria
- **`/speckit.specify`:** Create or update specifications
- **`/speckit.plan`:** Derive implementation strategy and dependencies
- **`/speckit.tasks`:** Break work into actionable tasks
- **`/speckit.implement`:** Generate code that satisfies the specification
- **`/speckit.clarify`:** Surface open questions and assumptions
- **`/speckit.analyze`:** Map code, tests, and logs back to the specification
- **`/speckit.checklist`:** Validate against policy and quality checklists

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
- "`/speckit.constitution initiative` to set mission and guardrails"
- "`/speckit.specify function_name` to capture the specification"
- "`/speckit.plan function_name` to derive the implementation strategy"
- "`/speckit.tasks function_name` to break work into deliverable tasks"
- "`/speckit.implement function_name` to generate code from the specification"
- "`/speckit.checklist function_name` to verify policy and quality compliance"

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
- [ ] Use `/speckit.checklist` to check security and compliance
- [ ] Verify business logic matches requirements (AI may misunderstand domain rules)
- [ ] Test AI-generated code thoroughly before production deployment
- [ ] Maintain audit trail of specifications and generated code

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed security guidelines.

---

## ESG (Environmental, Social, and Governance) Standards

🌱 **How This Lesson Supports ESG Excellence:**

### Environmental Impact
- **Carbon Footprint Reduction:** Spec-driven development reduces compute cycles by generating correct code on the first attempt, eliminating wasteful trial-and-error iterations. This reduces server energy consumption by 40-50% compared to traditional development cycles with multiple failed builds and tests.
- **Resource Efficiency:** Automated code generation from specifications eliminates redundant code writing, reducing CPU and memory usage. Spec-driven testing reduces the need for manual test execution, saving compute resources.
- **Sustainable Practices:** Specifications serve as reusable documentation, reducing the need for separate documentation files and minimizing storage requirements. This promotes long-term code maintainability and reduces technical debt.
- **Measurement:** Track reduction in build/test cycles, compute hours saved per feature, and code reuse percentage.

### Social Responsibility
- **Employee Well-being:** Spec-driven development reduces cognitive load by separating "what" (specs) from "how" (implementation), making development less stressful. Developers focus on problem-solving rather than boilerplate code, improving job satisfaction.
- **Accessibility & Inclusion:** Clear specifications make code accessible to all team members, including non-developers (QA, Product). This promotes collaboration and ensures everyone understands requirements, reducing communication barriers.
- **Community Impact:** Spec-driven development practices contribute to industry best practices, helping the broader software development community adopt more efficient and sustainable development methods.
- **Ethical AI Use:** Specifications ensure AI-generated code aligns with business requirements and ethical standards, preventing unintended consequences from AI code generation.

### Governance Excellence
- **Transparency:** Specifications provide clear, auditable documentation of what code should do, enabling better code reviews and compliance checks.
- **Accountability:** Spec-driven development creates clear traceability from requirements to implementation, ensuring developers can explain and justify code decisions.
- **Compliance:** Specifications can include compliance requirements (security, data privacy, payroll regulations), ensuring AI-generated code meets regulatory standards.
- **Risk Management:** Early specification review catches issues before implementation, reducing the risk of security vulnerabilities and compliance violations.

### ESG Metrics to Track
- [ ] Environmental: Reduced build/test cycles by 40-50% through first-attempt code generation
- [ ] Social: Improved developer satisfaction scores by 30%+ (measured via surveys)
- [ ] Governance: 100% of AI-generated code traceable to specifications (audit compliance)

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

---

## 10X Productivity Goals

🚀 **How This Lesson Drives 10X Productivity at Greenshades:**

### Productivity Impact
- **Time Savings:** Spec-driven development saves 50-70% of development time by eliminating manual code writing and enabling AI code generation. A feature that takes 8 hours traditionally can be completed in 2-4 hours.
- **Output Increase:** With spec-driven development, developers can deliver 3-5× more features in the same time period. Specs enable parallel development where multiple developers work from the same specification.
- **Quality Improvements:** Specifications catch requirements issues early, reducing bugs by 40-60% and eliminating costly rework. Automated test generation ensures comprehensive test coverage.
- **Automation Potential:** Spec-driven development automates 70-80% of code writing, 90% of test generation, and 60% of documentation, unlocking massive productivity gains.

### What 10X Looks Like
**Before This Lesson:**
- Manual code writing: 8 hours for a payroll calculation feature
- Manual test writing: 4 hours for test cases
- Requirements drift: 20% of features need rework
- Total: 12+ hours per feature with high error rate

**After Applying This Lesson:**
- Spec writing: 1 hour (clear requirements)
- AI code generation: 30 minutes (from spec)
- AI test generation: 15 minutes (from spec)
- Review and refinement: 1 hour
- Total: 3 hours per feature (4× faster, 10× with parallelization)

**The Transformation:**
- Development shifts from "write code, then test" to "define spec, generate everything"
- Teams move from sequential development to parallel spec-based development
- Quality improves as specs catch issues before implementation
- Documentation is automatically generated from specs

### How to Measure 10X Progress
**Key Metrics:**
1. **Efficiency Metric:** Development time per feature: Target 70% reduction (8 hours → 2.4 hours)
2. **Output Metric:** Features delivered per sprint: Target 5× increase
3. **Quality Metric:** Bug rate per feature: Target 60% reduction
4. **Adoption Metric:** Percentage of features using spec-driven development: Target 90%+

**Measurement Frequency:**
- [ ] Weekly: Development velocity, time per feature
- [ ] Monthly: Feature output, bug rates, spec adoption
- [ ] Quarterly: Overall productivity gains, ROI

**Tracking Tools:**
- Development tracking tools (Jira, GitHub Issues)
- Code generation metrics from AI tools
- Test coverage and bug tracking systems
- Spec repository and traceability tools

### How This Step Helps Achieve 10X
**Immediate Benefits:**
- 50-70% time savings on first spec-driven feature
- Immediate quality improvement through early requirement validation
- Foundation for automated code and test generation

**Short-term (1-3 months):**
- 3-5× increase in feature delivery rate
- 60% reduction in bugs and rework
- 90%+ spec adoption across development teams

**Long-term (6-12 months):**
- 10× productivity through cumulative spec reuse and refinement
- Strategic advantage from faster time-to-market
- Measurable ROI from reduced development costs and increased quality

**Cumulative Effect:**
- Specs become reusable assets, compounding productivity gains
- Each spec-driven feature builds a library of patterns and templates
- Teams become more efficient as they refine their spec-writing skills
- Spec-driven development enables other 10× practices (automated testing, documentation)

### Department-Specific 10X Targets
**Engineering:**
- 10× faster feature development through spec-driven code generation
- 5× increase in features delivered per sprint
- 60% reduction in bugs through early spec validation

**QA:**
- 10× faster test case generation from specifications
- 5× increase in test coverage with automated test generation
- 80% reduction in manual test writing time

**Product:**
- 10× faster feature specification and documentation
- 3× increase in features defined per sprint
- 50% reduction in requirements drift through clear specs

**All Departments:**
- 90%+ adoption of spec-driven development practices
- Measurable 10× productivity gains within 6 months

**Reference:** See `05_productivity_10x_framework/` for detailed productivity guidelines and metrics.

---

**Next Lesson:** `03_ai_agents_orchestration_flow.md`

