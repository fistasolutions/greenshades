# AI Data Security Policy

**Title:** AI Data Security Policy  
**Audience:** All (Engineering, QA, Product, HR, Finance, Sales, Support, Leadership)  
**Duration:** 45-60 minutes  
**Prerequisites:** `04_ai_ethics_and_security_basics/00_why_ai_governance_matters.md` (recommended)

---

## Learning Objectives

By the end of this lesson, you will be able to:

- Understand AI data security requirements at Greenshades
- Identify sensitive data that must be protected
- Apply data security rules when using AI tools
- Recognize data security risks and how to mitigate them
- Follow data security policies in daily work

---

## Core Content

### Data Classification

**Sensitive Data (Never Use in AI Tools):**
- **PII (Personally Identifiable Information):** SSNs, employee IDs, names with addresses
- **Financial Data:** Salaries, bank account numbers, tax information
- **Credentials:** Passwords, API keys, access tokens
- **Proprietary Information:** Business secrets, customer data, competitive intelligence

**Example Sensitive Data:**
```
❌ Employee SSN: 123-45-6789
❌ Salary: $75,000
❌ Password: MySecurePass123!
❌ API Key: sk_live_abc123xyz
❌ Customer Name: John Doe (with address)
```

**Safe to Use (With Placeholders):**
```
✅ Employee ID: <EMPLOYEE_ID>
✅ Salary Range: $50,000-$100,000 (range, not exact)
✅ Example SSN: <EXAMPLE_ONLY>
✅ Test Data: <TEST_DATA>
```

---

### Data Security Rules

#### Rule 1: No Sensitive Data in External AI Tools

**Prohibited:**
- Pasting SSNs, salaries, passwords into ChatGPT, Claude, or other external tools
- Uploading files containing sensitive data to AI tools
- Using AI tools that store data on external servers without encryption

**Why:**
- External AI tools may store data on their servers
- Data could be accessed by unauthorized parties
- Violates GDPR, CCPA, and other data privacy regulations

**Example Violation:**
```
❌ "Calculate tax for employee with SSN 123-45-6789, salary $75,000"
```

**Correct Approach:**
```
✅ "Calculate tax for employee with SSN <EMPLOYEE_ID>, salary <SALARY_AMOUNT>"
✅ Use internal AI tools with proper encryption and access controls
```

---

#### Rule 2: Use Placeholders for Sensitive Data

**When:** Testing, examples, documentation

**Format:**
- `<EXAMPLE_ONLY>` - Generic placeholder
- `<EMPLOYEE_ID>` - Employee identifier
- `<SALARY_AMOUNT>` - Salary data
- `<CUSTOMER_NAME>` - Customer information
- `<SSN>` - Social Security Number
- `<API_KEY>` - API credentials

**Example:**
```
❌ "Employee John Doe (SSN: 123-45-6789) earns $75,000"

✅ "Employee <EMPLOYEE_NAME> (SSN: <SSN>) earns <SALARY_AMOUNT>"
```

---

#### Rule 3: Encrypt Data in Transit and at Rest

**Requirements:**
- All data transmitted to AI tools must be encrypted (HTTPS/TLS)
- All data stored by AI tools must be encrypted at rest
- Use approved encryption standards (AES-256, TLS 1.3+)

**Verification:**
- Check AI tool documentation for encryption standards
- Verify HTTPS is used for all connections
- Confirm data storage encryption policies

---

#### Rule 4: Control Access to AI Tools

**Requirements:**
- Only authorized personnel can access AI tools
- Use authentication (SSO, MFA) for AI tool access
- Implement role-based access control (RBAC)
- Regular access reviews and revocation

**Example:**
```
✅ GitHub Copilot: Engineering team only, SSO authentication
✅ ChatGPT: All teams, but with data restrictions
✅ Internal AI tools: Role-based access, audit logging
```

---

#### Rule 5: Audit All AI Data Usage

**Requirements:**
- Log all AI tool usage (who, what, when)
- Monitor for sensitive data exposure
- Regular audits of AI tool access and usage
- Report security incidents immediately

**Audit Trail Should Include:**
- User identity
- Tool used
- Data accessed/processed
- Timestamp
- Purpose/justification

---

### Data Security by AI Tool Type

#### External AI Tools (ChatGPT, Claude)
- **Restriction:** No sensitive data
- **Use Case:** General Q&A, learning, non-sensitive tasks
- **Data Handling:** Data may be stored on external servers
- **Security:** Use placeholders, verify data handling policies

#### Internal AI Tools (On-Premises)
- **Restriction:** Encrypted, access-controlled
- **Use Case:** Payroll, tax, sensitive business data
- **Data Handling:** Data stays on-premises
- **Security:** Full encryption, access controls, audit trails

#### AI Development Tools (Copilot, Cursor)
- **Restriction:** No sensitive data in code
- **Use Case:** Code generation, debugging
- **Data Handling:** Code may be sent to AI services
- **Security:** Review code before committing, no credentials in code

---

### Data Security Risks and Mitigation

#### Risk 1: Accidental Data Exposure

**Scenario:** Developer pastes payroll data into ChatGPT

**Mitigation:**
- Training on data security policies
- Data loss prevention (DLP) tools
- Code review to catch sensitive data
- Automated scanning for sensitive data patterns

---

#### Risk 2: Unauthorized Access

**Scenario:** AI tool account compromised, sensitive data accessed

**Mitigation:**
- Strong authentication (MFA)
- Regular access reviews
- Monitor for unusual access patterns
- Immediate revocation on suspicion

---

#### Risk 3: Data Storage on External Servers

**Scenario:** External AI tool stores data on unencrypted servers

**Mitigation:**
- Use internal AI tools for sensitive data
- Verify external tool encryption policies
- Use placeholders in external tools
- Regular security assessments

---

### Compliance Requirements

#### GDPR (General Data Protection Regulation)
- **Requirement:** Protect EU citizen data
- **AI Impact:** No EU employee/customer data in external AI tools
- **Action:** Use internal tools or placeholders

#### CCPA (California Consumer Privacy Act)
- **Requirement:** Protect California resident data
- **AI Impact:** No CA employee/customer data in external AI tools
- **Action:** Use internal tools or placeholders

#### Payroll Regulations
- **Requirement:** Protect employee payroll data
- **AI Impact:** Encrypted storage, access controls, audit trails
- **Action:** Use internal AI tools with proper security

---

## Try It: Exercise

**Scenario:** You need to test an AI tool with payroll data.

**Task:** Identify what data you can and cannot use, and how to handle it safely.

**Solution:**
```
Cannot Use (Sensitive Data):
- Real employee SSNs
- Real salaries
- Real employee names with addresses
- Real bank account numbers

Can Use (With Placeholders):
- <EMPLOYEE_ID> instead of real SSN
- <SALARY_AMOUNT> instead of real salary
- <EMPLOYEE_NAME> instead of real name
- Test data that doesn't match real employees

Safe Approach:
1. Use placeholders for all sensitive data
2. Use internal AI tools if real data needed (with encryption)
3. Verify AI tool data handling policies
4. Review outputs for any sensitive data exposure
5. Delete test data after use
```

---

## Role-Based "How This Helps You"

### Developers
- **Code Security:** Never hardcode credentials or sensitive data
- **AI Tools:** Use placeholders when testing with AI
- **Code Review:** Check for sensitive data in code

### QA Engineers
- **Test Data:** Use placeholders or synthetic test data
- **Security Testing:** Test AI tools for data security
- **Compliance:** Verify AI tools meet security requirements

### Product Managers
- **Feature Planning:** Consider data security in AI feature design
- **Compliance:** Ensure features meet data privacy regulations
- **Risk Management:** Identify and mitigate data security risks

### All Staff
- **Daily Usage:** Follow data security rules when using AI tools
- **Reporting:** Report data security incidents immediately
- **Training:** Stay updated on data security policies

---

## Key Takeaways

1. **Data Classification:** Sensitive data (SSNs, salaries, passwords) must be protected

2. **Security Rules:** No sensitive data in external AI tools, use placeholders, encrypt data, control access, audit usage

3. **Tool Types:** External tools (no sensitive data), Internal tools (encrypted, controlled), Development tools (no credentials)

4. **Risks:** Accidental exposure, unauthorized access, external storage—mitigate with training, controls, monitoring

5. **Compliance:** GDPR, CCPA, payroll regulations require data protection

---

## 5-Question Quiz

### Question 1 (Multiple Choice)
Which data should NEVER be used in external AI tools?

a) Placeholders  
b) Sensitive data (SSNs, salaries, passwords)  
c) Test data  
d) All of the above

**Answer:** b) Sensitive data (SSNs, salaries, passwords)

---

### Question 2 (True/False)
Using placeholders like `<EMPLOYEE_ID>` is acceptable when testing AI tools with sensitive data scenarios.

**Answer:** True

---

### Question 3 (Short Answer)
Name one data security rule for AI tools.

**Answer:** Examples: No sensitive data in external tools, use placeholders, encrypt data, control access, audit usage. (Accept any one)

---

### Question 4 (Multiple Choice)
What should you do if you accidentally paste sensitive data into an AI tool?

a) Ignore it  
b) Report it immediately to IT/Security  
c) Delete it yourself  
d) None of the above

**Answer:** b) Report it immediately to IT/Security

---

### Question 5 (Short Answer)
Give one example of a placeholder you should use instead of real sensitive data.

**Answer:** Examples: `<EMPLOYEE_ID>`, `<SALARY_AMOUNT>`, `<SSN>`, `<API_KEY>`, `<EXAMPLE_ONLY>`. (Accept any one)

---

## One-Page Cheat Sheet

### Sensitive Data (Never Use)
- SSNs, employee IDs, names with addresses
- Salaries, bank account numbers, tax information
- Passwords, API keys, access tokens
- Business secrets, customer data

### Data Security Rules
1. No sensitive data in external AI tools
2. Use placeholders for sensitive data
3. Encrypt data in transit and at rest
4. Control access to AI tools
5. Audit all AI data usage

### Placeholders
- `<EXAMPLE_ONLY>` - Generic
- `<EMPLOYEE_ID>` - Employee identifier
- `<SALARY_AMOUNT>` - Salary data
- `<SSN>` - Social Security Number
- `<API_KEY>` - API credentials

### Tool Types
- **External Tools:** No sensitive data, use placeholders
- **Internal Tools:** Encrypted, access-controlled
- **Development Tools:** No credentials in code

### Compliance
- GDPR: Protect EU citizen data
- CCPA: Protect CA resident data
- Payroll Regulations: Encrypted storage, access controls

### Incident Response
- Report data security incidents immediately
- Contact IT/Security team
- Follow incident response procedures

---

## Phrases & Prompts That Work

**When using AI tools:**
- "Never paste sensitive data—use placeholders like `<EMPLOYEE_ID>`."
- "External AI tools may store data—use internal tools for sensitive data."

**When testing:**
- "Use placeholders or synthetic test data—never real sensitive data."
- "Verify AI tool data handling policies before using."

**When reporting:**
- "Report data security incidents immediately to IT/Security."
- "If in doubt, don't use sensitive data in AI tools."

---

## Security & Compliance Note

⚠️ **Red Flags Checklist:**
- [ ] Never paste sensitive data (SSNs, salaries, passwords) into AI tools
- [ ] Always use placeholders for sensitive data in examples and tests
- [ ] Verify AI tool data handling policies before using
- [ ] Report data security incidents immediately
- [ ] Use internal AI tools for sensitive data (with proper encryption)

**Reference:** See other lessons in `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

---

## ESG (Environmental, Social, and Governance) Standards

🌱 **How This Lesson Supports ESG Excellence:**

### Environmental Impact
- **Carbon Footprint Reduction:** AI data security policies prevent data breaches and security incidents that require remediation, reducing compute cycles and infrastructure needs. Secure AI practices reduce energy consumption by 30-40% compared to unsecured AI usage.
- **Resource Efficiency:** Security policies promote efficient AI tool usage by preventing wasteful security remediation work. Encrypted, access-controlled data reduces infrastructure waste from security incidents.
- **Sustainable Practices:** Data security policies promote sustainable AI practices by ensuring long-term secure operations, reducing the need for frequent security fixes and minimizing resource waste.
- **Measurement:** Track reduction in security incidents, compute hours saved through secure practices, and resource efficiency from encrypted, access-controlled data.

### Social Responsibility
- **Employee Well-being:** Data security policies protect employees from data breaches and security incidents, improving job security and satisfaction. Clear security policies reduce anxiety and improve confidence in AI usage.
- **Accessibility & Inclusion:** Security policies ensure all employees have secure access to AI tools, promoting equity. Placeholder usage and secure practices make AI accessible while protecting sensitive data.
- **Community Impact:** Strong data security policies at Greenshades set industry standards for secure AI adoption in payroll and tax software, contributing to ethical AI practices across the sector.
- **Ethical AI Use:** Data security policies ensure ethical AI use by protecting sensitive data (SSNs, salaries, passwords), preventing privacy violations and ensuring responsible AI adoption.

### Governance Excellence
- **Transparency:** Data security policies create transparency in AI data handling through clear policies and audit trails, enabling accountability and compliance verification.
- **Accountability:** Security policies ensure accountability for data handling through access controls, audit logging, and incident reporting, ensuring responsible AI data usage.
- **Compliance:** Data security policies ensure compliance with regulations (GDPR, CCPA, payroll regulations), protecting the organization from legal and financial risks.
- **Risk Management:** Security policies proactively identify and mitigate data security risks (breaches, unauthorized access, data exposure), preventing costly incidents and protecting organizational reputation.

### ESG Metrics to Track
- [ ] Environmental: Reduced security incidents by 30-40% through data security policies
- [ ] Social: Improved employee confidence from secure AI practices by 35%+ (measured via surveys)
- [ ] Governance: 100% compliance with data security policies (mandatory compliance metric)

**Reference:** See `04_ai_ethics_and_security_basics/` for detailed ESG guidelines.

---

## 10X Productivity Goals

🚀 **How This Lesson Drives 10X Productivity at Greenshades:**

### Productivity Impact
- **Time Savings:** Data security policies save 5-10 hours per week per team by preventing security incidents and data breaches that require remediation. Secure practices eliminate costly security fixes.
- **Output Increase:** Secure AI practices enable confident AI adoption, increasing AI tool usage and productivity by 3-5×. Teams can leverage AI tools effectively without fear of security violations.
- **Quality Improvements:** Security policies ensure AI outputs meet security standards, reducing security-related errors by 70-80% and eliminating costly remediation from security incidents.
- **Automation Potential:** Secure AI practices enable safe automation of high-risk processes (payroll, tax), unlocking 80-90% time savings while maintaining security and compliance.

### What 10X Looks Like
**Before This Lesson:**
- Unsecured AI usage: Teams afraid to use AI tools effectively due to security concerns
- Frequent security incidents: Data breaches, unauthorized access requiring remediation
- Low AI adoption: Only 30-40% of teams using AI tools due to security fears
- Security overhead: 10-15 hours/week on security remediation

**After Applying This Lesson:**
- Secured AI usage: Teams confidently leverage AI tools within clear security policies
- Zero security incidents: Policies prevent data breaches and unauthorized access
- High AI adoption: 90%+ of teams using AI tools effectively and safely
- Minimal security overhead: 1-2 hours/week on security compliance (80-90% reduction)

**The Transformation:**
- Teams shift from "fear of security violations" to "confident secure AI adoption"
- Organization moves from reactive security incident response to proactive security policies
- AI becomes a strategic enabler rather than a security risk concern
- Productivity multiplies as teams leverage AI tools safely and effectively

### How to Measure 10X Progress
**Key Metrics:**
1. **Efficiency Metric:** Time saved from prevented security incidents: Target 5-10 hours/week per team
2. **Output Metric:** AI tool adoption rate: Target 90%+ (from 30-40%)
3. **Quality Metric:** Security incidents: Target 90%+ reduction
4. **Adoption Metric:** Security policy compliance: Target 100%

**Measurement Frequency:**
- [ ] Weekly: AI tool usage, security incident tracking
- [ ] Monthly: Adoption rates, compliance metrics, security scores
- [ ] Quarterly: Overall productivity gains, ROI, risk reduction

**Tracking Tools:**
- Security compliance dashboards
- AI tool usage analytics
- Security incident tracking systems
- Compliance audit tools

### How This Step Helps Achieve 10X
**Immediate Benefits:**
- Immediate risk reduction and security incident prevention
- Increased confidence in AI tool usage
- Foundation for safe and effective AI adoption

**Short-term (1-3 months):**
- 3-5× increase in AI tool adoption (from 30-40% to 90%+)
- 80%+ reduction in security incidents
- 100% security policy compliance

**Long-term (6-12 months):**
- 10× productivity through safe, confident AI adoption
- Strategic advantage from risk-free AI innovation
- Measurable ROI from prevented security incidents and increased productivity

**Cumulative Effect:**
- Security policies enable all other 10× productivity initiatives
- Without security, AI adoption is limited by fear and risk
- Each secure AI initiative builds confidence and accelerates adoption
- Security becomes the foundation for sustainable 10× productivity

### Department-Specific 10X Targets
**Engineering:**
- 10× faster development through secure AI code generation
- 90%+ AI tool adoption (from 40%)
- Zero security incidents from AI usage

**QA:**
- 10× faster test generation through secure AI tools
- 90%+ AI tool adoption
- Zero data security violations

**Product:**
- 10× faster feature delivery through secure AI assistance
- 90%+ AI tool adoption
- Zero security issues from AI outputs

**Support:**
- 10× faster issue resolution through secure AI chatbots
- 90%+ AI tool adoption
- Zero customer data privacy incidents

**All Departments:**
- 100% security policy compliance
- 90%+ AI tool adoption
- Measurable 10× productivity gains within 12 months

**Reference:** See `05_productivity_10x_framework/` for detailed productivity guidelines and metrics.

---

**Next Lesson:** `02_model_bias_and_fairness.md`

