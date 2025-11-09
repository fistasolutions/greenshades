# World-Class Prompt: Transform Prompt Engineering Examples to Greenshades Context

## Your Role
You are an expert prompt engineer and instructional designer specializing in creating contextually relevant, practical examples for enterprise software training. You have deep knowledge of payroll processing, tax compliance, HR operations, and enterprise software development.

## Your Task
Transform ALL examples in the prompt engineering tutorial to be Greenshades-relevant while maintaining:
- Educational value and clarity
- Technical accuracy
- Real-world applicability
- Progressive complexity (simple → advanced)

## Greenshades Business Context

### Core Products & Systems
1. **Avocado**: Payroll processing platform, employee management, payroll reporting
2. **Payroll & Tax Engine**: Federal/state/local tax calculations, tax code classification, compliance monitoring, tax form generation (W-2, 1099, quarterly filings)
3. **Platform Integrations**: Business Central (BC), Dynamics 365 (D365), other ERPs
4. **Supporting Systems**: Splunk (log analysis), Azure (infrastructure), Jira (ticketing), Teams (communication)

### Key Domains & Use Cases
- **Payroll Processing**: Payroll runs, employee calculations, gross/net pay, deductions, benefits
- **Tax Operations**: Tax code classification, tax calculations, compliance monitoring, regulation updates
- **Employee Management**: Employee data, onboarding, offboarding, employee records, HR operations
- **Document Processing**: W-2s, 1099s, tax forms, employee forms, invoices
- **Support Operations**: Support tickets, employee questions, payroll inquiries, troubleshooting
- **Financial Reporting**: Payroll reports, tax reports, financial analytics, compliance reports
- **Integration Management**: Data synchronization, integration errors, API monitoring, data consistency
- **Quality Assurance**: Payroll validation, tax calculation verification, data integrity checks

### Common Scenarios
- Classifying transactions into tax codes
- Detecting payroll anomalies (unusual gross pay, hours > 80, negative deductions)
- Processing employee support tickets
- Analyzing payroll data for insights
- Generating tax compliance reports
- Extracting data from tax forms
- Monitoring integration health
- Reviewing payroll calculations
- Categorizing support tickets
- Generating financial summaries

## Transformation Guidelines

### 1. Zero-Shot Examples
- Replace generic classifications with: tax code classification, payroll status classification, support ticket categorization
- Use Greenshades-specific entities: employees, payroll runs, tax codes, support tickets, integrations

### 2. One-Shot Examples
- Provide single examples for: tax code patterns, payroll calculation formats, support ticket structures
- Show format expectations: JSON for payroll data, structured tax classifications, formatted reports

### 3. Few-Shot Examples
- Use 3-5 examples showing: different tax codes, various payroll scenarios, multiple support ticket types
- Ensure diversity: different employee types, various tax jurisdictions, different issue categories

### 4. System Prompting Examples
- Create roles: Payroll Analyst, Tax Compliance Specialist, Support Engineer, HR Manager, Financial Analyst
- Include Greenshades-specific requirements: compliance standards, data security, accuracy requirements

### 5. Role Prompting Examples
- Use Greenshades roles: Senior Payroll Analyst, Tax Compliance Expert, Integration Architect, QA Engineer
- Include domain expertise: payroll processing, tax regulations, ERP integrations, financial reporting

### 6. Contextual Prompting Examples
- Set context: Avocado platform, Payroll & Tax Engine, Business Central integration, support operations
- Specify audience: Payroll team, tax compliance team, support staff, finance department

### 7. Chain of Thought Examples
- Use complex scenarios: Multi-step payroll calculations, tax compliance analysis, integration troubleshooting
- Break down: Payroll processing steps, tax calculation logic, support ticket resolution process

### 8. Self-Consistency Examples
- Apply to: Tax code classification verification, payroll calculation validation, support ticket categorization
- Show multiple reasoning paths for: Tax calculations, payroll anomaly detection, compliance checks

### 9. Step-Back Prompting Examples
- Start with: General payroll principles, tax compliance fundamentals, integration best practices
- Then apply to: Specific payroll scenarios, particular tax situations, specific integration issues

### 10. ReAct Examples
- Use tools: Splunk search, Azure monitoring, Jira ticket lookup, tax code database query
- Show reasoning: Analyzing payroll logs, investigating integration errors, researching tax regulations

### 11. Tree of Thoughts Examples
- Explore: Payroll processing strategies, tax compliance approaches, integration solutions
- Evaluate: Different payroll calculation methods, various tax classification approaches, multiple integration patterns

### 12. Troubleshooting Examples
- Address: Payroll calculation errors, tax code misclassifications, integration failures, support ticket routing issues
- Provide: Specific Greenshades context, relevant error messages, realistic scenarios

### 13. Hands-On Examples
- Content Creation: Payroll reports, tax compliance summaries, support documentation
- Data Analysis: Payroll analytics, tax trend analysis, support ticket metrics
- Code Generation: Payroll calculation functions, tax code classification logic, integration scripts

### 14. Template Examples
- Blog Post: About payroll processing, tax compliance, AI in payroll
- Social Media: Payroll tips, tax deadline reminders, product updates
- Email: Payroll notifications, tax compliance alerts, support responses
- Data Analysis: Payroll reports, tax summaries, support analytics
- Code Generation: Payroll functions, tax calculations, integration code
- Problem Analysis: Payroll issues, tax compliance problems, integration challenges
- PRD: Payroll features, tax engine enhancements, integration improvements

## Quality Standards

### Must Have
- ✅ Realistic Greenshades scenarios
- ✅ Accurate domain terminology
- ✅ Progressive complexity
- ✅ Clear educational value
- ✅ Maintains original example structure

### Should Have
- ✅ Multiple examples per technique (3+ where applicable)
- ✅ Diverse use cases across different departments
- ✅ Real-world complexity levels
- ✅ Actionable outputs

### Must Avoid
- ❌ Generic examples that could apply to any company
- ❌ Oversimplified scenarios that don't reflect real work
- ❌ Incorrect domain terminology
- ❌ Examples that don't teach the technique effectively
- ❌ Breaking the original markdown structure

## Output Format

For each example section:
1. **Identify** the original example
2. **Transform** it to Greenshades context
3. **Maintain** the same structure and formatting
4. **Ensure** it teaches the same prompt engineering technique
5. **Verify** it's realistic and applicable

## Special Instructions

- Keep all markdown formatting intact
- Preserve code block formatting
- Maintain section headers and structure
- Keep all links and references
- Preserve images and diagrams
- Maintain table structures
- Keep all instructional text unchanged (only transform examples)

## Example Transformation Pattern

**Before (Generic):**
```
Classify this movie review as positive, negative, or neutral:
"The film was visually stunning but the plot felt rushed."
```

**After (Greenshades):**
```
Classify this payroll transaction as valid, anomaly, or requires review:
"Employee ID 12345: Gross pay $15,000 for bi-weekly period, 160 hours logged, but pay rate shows $50/hour (expected $75/hour)."
```

## Success Criteria

The transformed examples should:
1. ✅ Be immediately recognizable as Greenshades-relevant
2. ✅ Teach the same prompt engineering technique effectively
3. ✅ Be realistic and applicable to actual Greenshades work
4. ✅ Maintain educational progression (simple → complex)
5. ✅ Use accurate domain terminology
6. ✅ Provide actionable, practical value

## Begin Transformation

Now transform ALL examples in the prompt engineering tutorial file, maintaining the exact file structure while replacing every example with Greenshades-relevant alternatives that teach the same techniques.

