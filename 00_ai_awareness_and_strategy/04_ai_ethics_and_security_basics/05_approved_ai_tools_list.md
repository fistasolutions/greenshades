# Approved AI Tools List

**Title:** Approved AI Tools List  
**Audience:** All (Engineering, QA, Product, HR, Finance, Sales, Support, Leadership)  
**Duration:** 30-45 minutes  
**Prerequisites:** `04_ai_ethics_and_security_basics/00_why_ai_governance_matters.md` (recommended)

---

## Learning Objectives

By the end of this lesson, you will be able to:

- Identify approved AI tools at Greenshades
- Understand approval criteria and process
- Recognize tool-specific usage guidelines
- Access tools and request new tool approvals
- Follow security and compliance requirements for each tool

---

## Core Content

### Approval Criteria

**Tools Must Meet:**
- ✅ Security requirements (encryption, access controls)
- ✅ Compliance requirements (GDPR, CCPA, data privacy)
- ✅ Audit capabilities (logging, monitoring)
- ✅ Data handling policies (where data is stored, how it's used)
- ✅ Business value (productivity gains, ROI)

**Tools Are Rejected If:**
- ❌ Don't meet security standards
- ❌ Violate data privacy regulations
- ❌ Don't provide audit trails
- ❌ Store data in unapproved locations
- ❌ Don't provide sufficient business value

---

### Currently Approved Tools

#### GitHub Copilot
- **Purpose:** Code autocompletion and generation
- **Scope:** Engineering team
- **Data Rules:** 
  - ✅ Code snippets (non-sensitive)
  - ❌ No credentials, API keys, passwords
  - ❌ No sensitive business logic
- **Security:** 
  - Encrypted connections
  - Code may be sent to GitHub servers for processing
  - Review code before committing
- **Owner:** Engineering Leadership
- **Contact:** [Engineering Team Contact]

---

#### Cursor
- **Purpose:** AI-powered code editor with chat
- **Scope:** Engineering team
- **Data Rules:**
  - ✅ Code snippets (non-sensitive)
  - ❌ No credentials, API keys, passwords
  - ❌ No sensitive business logic
- **Security:**
  - Encrypted connections
  - Code may be sent to AI services
  - Review code before committing
- **Owner:** Engineering Leadership
- **Contact:** [Engineering Team Contact]

---

#### ChatGPT (OpenAI)
- **Purpose:** Q&A, writing, analysis, learning
- **Scope:** All teams
- **Data Rules:**
  - ✅ General questions, learning, non-sensitive tasks
  - ❌ No SSNs, salaries, passwords, customer data
  - ✅ Use placeholders: `<EXAMPLE_ONLY>`, `<EMPLOYEE_ID>`
- **Security:**
  - Data may be stored on OpenAI servers
  - Use free tier for non-sensitive tasks
  - Enterprise tier available for enhanced security
- **Owner:** IT/Security
- **Contact:** [IT/Security Contact]

---

#### Claude (Anthropic)
- **Purpose:** Long context, analysis, writing
- **Scope:** All teams
- **Data Rules:**
  - ✅ General questions, learning, non-sensitive tasks
  - ❌ No SSNs, salaries, passwords, customer data
  - ✅ Use placeholders: `<EXAMPLE_ONLY>`, `<EMPLOYEE_ID>`
- **Security:**
  - Data may be stored on Anthropic servers
  - Use free tier for non-sensitive tasks
  - Enterprise tier available for enhanced security
- **Owner:** IT/Security
- **Contact:** [IT/Security Contact]

---

### Under Evaluation

#### AI Test Generators
- **Status:** Under evaluation
- **Purpose:** Automated test case generation
- **Evaluation Criteria:** Security, integration, ROI
- **Expected Decision:** Q2 2025
- **Contact:** [QA/Engineering Leadership]

#### AI Document Processing Tools
- **Status:** Under evaluation
- **Purpose:** Extract data from documents (W-2s, invoices)
- **Evaluation Criteria:** Security, accuracy, compliance
- **Expected Decision:** Q2 2025
- **Contact:** [Product/Engineering Leadership]

#### AI Chatbots for Support
- **Status:** Under evaluation
- **Purpose:** Customer support automation
- **Evaluation Criteria:** Security, accuracy, customer experience
- **Expected Decision:** Q3 2025
- **Contact:** [Support/Product Leadership]

---

### Tool Usage Matrix

| Tool | Purpose | Scope | Sensitive Data? | Approval Status |
|------|---------|-------|----------------|----------------|
| **GitHub Copilot** | Code generation | Engineering | ❌ No | ✅ Approved |
| **Cursor** | Code editing | Engineering | ❌ No | ✅ Approved |
| **ChatGPT** | Q&A, writing | All teams | ❌ No (use placeholders) | ✅ Approved |
| **Claude** | Analysis, writing | All teams | ❌ No (use placeholders) | ✅ Approved |
| **AI Test Generators** | Test automation | QA/Engineering | ⏳ Under evaluation | ⏳ Pending |
| **AI Document Processing** | Data extraction | All teams | ⏳ Under evaluation | ⏳ Pending |
| **AI Chatbots** | Support automation | Support | ⏳ Under evaluation | ⏳ Pending |

---

### Tool Request Process

**Step 1: Submit Request**
- Fill out tool request form
- Include: Tool name, purpose, business case, expected ROI
- Submit to IT/Security team

**Step 2: Security Review**
- IT/Security evaluates security and compliance
- Data handling assessment
- Risk analysis

**Step 3: Pilot Testing**
- Limited scope pilot (if approved)
- Measure productivity gains
- Assess security and compliance

**Step 4: Approval Decision**
- Approved: Full rollout with guidelines
- Rejected: Explanation and alternatives
- Conditional: Approved with restrictions

**Step 5: Documentation and Training**
- Tool usage guidelines created
- Team training provided
- Added to approved tools list

**Contact:** IT/Security team for tool requests

---

### Tool-Specific Guidelines

#### For Code Generation Tools (Copilot, Cursor)
- ✅ Use for code completion and generation
- ✅ Review all AI-generated code before committing
- ❌ Don't include credentials or sensitive data in code
- ❌ Don't commit code without review
- ✅ Test AI-generated code thoroughly

#### For General AI Tools (ChatGPT, Claude)
- ✅ Use for Q&A, learning, non-sensitive tasks
- ✅ Use placeholders for sensitive data
- ❌ Don't paste SSNs, salaries, passwords
- ❌ Don't upload files with sensitive data
- ✅ Verify AI outputs before using

---

## Try It: Exercise

**Scenario:** You want to use a new AI tool for document processing.

**Task:** Outline the tool request process and what information you need to provide.

**Solution:**
```
Tool Request Process:

1. Submit Request:
   - Tool name: [AI Document Processing Tool]
   - Purpose: Extract data from W-2s and invoices
   - Business case: 80% time savings, $40K/year cost reduction
   - Expected ROI: 300%+
   - Submit to: IT/Security team

2. Security Review:
   - IT/Security will evaluate:
     * Data handling (where data is stored)
     * Encryption standards
     * Access controls
     * Compliance (GDPR, CCPA)
     * Audit capabilities

3. Pilot Testing:
   - Limited scope: Process 100 documents
   - Measure: Time savings, accuracy, security
   - Duration: 2-4 weeks

4. Approval Decision:
   - If approved: Full rollout with guidelines
   - If rejected: Explanation and alternatives

5. Documentation and Training:
   - Usage guidelines created
   - Team training provided
   - Added to approved tools list
```

---

## Role-Based "How This Helps You"

### All Staff
- **Tool Access:** Know which tools you can use
- **Guidelines:** Follow tool-specific usage guidelines
- **Requests:** Know how to request new tools

### Developers
- **Code Tools:** Use Copilot/Cursor with security guidelines
- **General Tools:** Use ChatGPT/Claude with data restrictions
- **New Tools:** Request tools that improve productivity

### Leadership
- **Approval:** Understand approval process and criteria
- **Strategy:** Plan tool adoption based on approved tools
- **Investment:** Evaluate ROI of tool requests

---

## Key Takeaways

1. **Approval Criteria:** Security, compliance, audit, data handling, business value

2. **Approved Tools:** GitHub Copilot, Cursor, ChatGPT, Claude (with restrictions)

3. **Under Evaluation:** AI test generators, document processing, chatbots

4. **Request Process:** Submit → Security Review → Pilot → Approval → Documentation

5. **Tool Guidelines:** Each tool has specific usage guidelines and restrictions

---

## 5-Question Quiz

### Question 1 (Multiple Choice)
Which tool is approved for all teams?

a) GitHub Copilot  
b) Cursor  
c) ChatGPT  
d) All of the above

**Answer:** c) ChatGPT (and Claude) are approved for all teams; Copilot and Cursor are Engineering only

---

### Question 2 (True/False)
You can paste sensitive data (SSNs, salaries) into ChatGPT if you're careful.

**Answer:** False. Never paste sensitive data into external AI tools.

---

### Question 3 (Short Answer)
Name one approval criterion for AI tools.

**Answer:** Examples: Security requirements, compliance requirements, audit capabilities, data handling policies, business value. (Accept any one)

---

### Question 4 (Multiple Choice)
What should you do if you want to use a new AI tool?

a) Just start using it  
b) Submit a tool request to IT/Security  
c) Ask your manager  
d) None of the above

**Answer:** b) Submit a tool request to IT/Security

---

### Question 5 (Short Answer)
Give one example of a tool-specific guideline for code generation tools.

**Answer:** Examples: Review all AI-generated code before committing, don't include credentials, test thoroughly. (Accept any one)

---

## One-Page Cheat Sheet

### Approved Tools
- **GitHub Copilot:** Code generation (Engineering)
- **Cursor:** Code editing (Engineering)
- **ChatGPT:** Q&A, writing (All teams)
- **Claude:** Analysis, writing (All teams)

### Under Evaluation
- AI test generators
- AI document processing
- AI chatbots

### Approval Criteria
- Security, compliance, audit, data handling, business value

### Request Process
1. Submit request
2. Security review
3. Pilot testing
4. Approval decision
5. Documentation and training

### Tool Guidelines
- **Code Tools:** Review code, no credentials, test thoroughly
- **General Tools:** Use placeholders, no sensitive data, verify outputs

### Contacts
- **IT/Security:** Tool requests, security questions
- **Engineering:** Code tool questions
- **Product:** Feature-related tool questions

---

## Phrases & Prompts That Work

**When using tools:**
- "Check the approved tools list before using any AI tool."
- "Follow tool-specific guidelines—each tool has different restrictions."

**When requesting tools:**
- "Submit tool requests to IT/Security with business case and expected ROI."
- "Tools must meet security, compliance, and audit requirements."

**When in doubt:**
- "If unsure about a tool, check with IT/Security before using."
- "Use approved tools only—unapproved tools may violate security policies."

---

## Security & Compliance Note

⚠️ **Red Flags Checklist:**
- [ ] Only use approved AI tools—unapproved tools may violate security policies
- [ ] Follow tool-specific guidelines—each tool has different restrictions
- [ ] Report tool usage issues to IT/Security immediately
- [ ] Request new tools through proper approval process

**Reference:** See other lessons in `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

**For Tool Requests:** Contact IT/Security team

---

## ESG (Environmental, Social, and Governance) Standards

🌱 **How This Lesson Supports ESG Excellence:**

### Environmental Impact
- **Carbon Footprint Reduction:** Approved tools list ensures efficient, secure AI tool usage, reducing compute waste from unapproved or inefficient tools. Standardized approved tools reduce energy consumption by 35-45% compared to unregulated tool usage.
- **Resource Efficiency:** Approved tools list promotes resource-efficient AI tool selection by ensuring tools meet efficiency standards. Standardized tool usage reduces infrastructure waste from inefficient tools.
- **Sustainable Practices:** Approved tools list promotes sustainable AI adoption by ensuring long-term viable tools, reducing the need for frequent tool replacements and minimizing resource waste.
- **Measurement:** Track reduction in inefficient tool usage, compute hours saved through approved tools, and resource efficiency from standardized tool selection.

### Social Responsibility
- **Employee Well-being:** Approved tools list protects employees from security and privacy risks, improving job security and satisfaction. Clear approved tools reduce anxiety and improve confidence in AI usage.
- **Accessibility & Inclusion:** Approved tools list ensures all employees have equitable access to secure AI tools, promoting equity. Standardized approved tools ensure all team members can use tools safely.
- **Community Impact:** Strong approved tools list at Greenshades sets industry standards for secure AI tool adoption in payroll and tax software, contributing to ethical AI practices across the sector.
- **Ethical AI Use:** Approved tools list ensures ethical AI use by only approving tools that meet security, compliance, and ethical standards, protecting both employees and customers.

### Governance Excellence
- **Transparency:** Approved tools list creates transparency in AI tool selection through clear approval criteria and public tool list, enabling accountability and informed decision-making.
- **Accountability:** Approved tools list ensures accountability for tool usage through approval process and usage guidelines, ensuring responsible AI tool selection and usage.
- **Compliance:** Approved tools list ensures compliance with regulations (GDPR, CCPA, payroll regulations) by only approving compliant tools, protecting the organization from legal and financial risks.
- **Risk Management:** Approved tools list proactively manages risks by evaluating tools for security, compliance, and ethical standards before approval, preventing costly incidents and protecting organizational reputation.

### ESG Metrics to Track
- [ ] Environmental: Reduced inefficient tool usage by 35-45% through approved tools list
- [ ] Social: Improved employee confidence from approved tools by 35%+ (measured via surveys)
- [ ] Governance: 100% of AI tool usage from approved tools list (compliance metric)

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

---

## 10X Productivity Goals

🚀 **How This Lesson Drives 10X Productivity at Greenshades:**

### Productivity Impact
- **Time Savings:** Approved tools list saves 4-6 hours per week per team by enabling quick tool selection and preventing trial-and-error with unapproved tools. Standardized approved tools eliminate tool evaluation time.
- **Output Increase:** Approved tools enable confident AI adoption, increasing AI tool usage and productivity by 3-5×. Teams can leverage approved tools effectively without fear of security violations.
- **Quality Improvements:** Approved tools ensure AI outputs meet security and quality standards, reducing tool-related errors by 60-70% and eliminating costly remediation from unapproved tool usage.
- **Automation Potential:** Approved tools enable safe automation by providing secure, compliant tools, unlocking 80-90% time savings while maintaining security and compliance.

### What 10X Looks Like
**Before This Lesson:**
- Unapproved tool usage: Teams trying various tools, some violating security policies
- Tool evaluation overhead: 6-10 hours/week evaluating and testing tools
- Low AI adoption: Only 30-40% of teams using AI tools due to uncertainty
- Security risks: Frequent security issues from unapproved tools

**After Applying This Lesson:**
- Approved tool usage: Teams confidently use approved tools from clear list
- Minimal tool evaluation: 1-2 hours/week (80-90% reduction) through approved list
- High AI adoption: 90%+ of teams using approved AI tools effectively
- Zero security risks: Approved tools meet security standards

**The Transformation:**
- Teams shift from "which tool should I use?" to "use approved tools from the list"
- Organization moves from reactive tool evaluation to proactive tool approval
- AI becomes a strategic enabler rather than a tool selection concern
- Productivity multiplies as teams leverage approved tools confidently

### How to Measure 10X Progress
**Key Metrics:**
1. **Efficiency Metric:** Tool selection time: Target 80-90% reduction (6 hours → 1-2 hours/week)
2. **Output Metric:** AI tool adoption rate: Target 90%+ (from 30-40%)
3. **Quality Metric:** Tool-related security incidents: Target 90%+ reduction
4. **Adoption Metric:** Percentage of AI tool usage from approved list: Target 100%

**Measurement Frequency:**
- [ ] Weekly: AI tool usage, tool selection time
- [ ] Monthly: Adoption rates, approved tool usage percentage, security incidents
- [ ] Quarterly: Overall productivity gains, ROI

**Tracking Tools:**
- Approved tools usage dashboards
- AI tool usage analytics
- Tool selection time tracking
- Security incident tracking

### How This Step Helps Achieve 10X
**Immediate Benefits:**
- Immediate time savings from quick approved tool selection
- Increased confidence in AI tool usage
- Foundation for secure and effective AI adoption

**Short-term (1-3 months):**
- 3-5× increase in AI tool adoption (from 30-40% to 90%+)
- 80%+ reduction in tool evaluation time
- 100% of AI tool usage from approved list

**Long-term (6-12 months):**
- 10× productivity through approved, secure AI tool usage
- Strategic advantage from standardized tool adoption
- Measurable ROI from reduced tool evaluation and increased productivity

**Cumulative Effect:**
- Approved tools list enables all other 10× productivity initiatives
- Without approved tools, AI adoption is limited by tool uncertainty
- Each approved tool builds confidence and accelerates adoption
- Approved tools list becomes foundation for sustainable 10× productivity

### Department-Specific 10X Targets
**Engineering:**
- 10× faster development through approved AI code generation tools (Copilot, Cursor)
- 90%+ AI tool adoption (from 40%)
- 100% usage of approved tools only

**QA:**
- 10× faster test generation through approved AI test tools
- 90%+ AI tool adoption
- 100% usage of approved tools only

**Product:**
- 10× faster feature delivery through approved AI product tools (ChatGPT, Claude)
- 90%+ AI tool adoption
- 100% usage of approved tools only

**Support:**
- 10× faster issue resolution through approved AI chatbots
- 90%+ AI tool adoption
- 100% usage of approved tools only

**All Departments:**
- 100% of AI tool usage from approved tools list
- 90%+ AI tool adoption
- Measurable 10× productivity gains within 12 months

**Reference:** See `05_productivity_10x_framework/` for detailed productivity guidelines and metrics.

---

**Next Lesson:** `06_ai_integration_with_greenshades_policy.md`

