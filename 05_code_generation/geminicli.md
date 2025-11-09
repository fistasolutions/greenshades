# Gemini CLI: Complete Tutorial and Mastery Guide

*Master Google's Gemini Command-Line Interface from Beginner to Expert*

**Official Documentation:** https://developers.google.com/gemini-code-assist/docs/gemini-cli  
**GitHub Repository:** https://github.com/google/gemini-cli

---

## Table of Contents

1. [Introduction to Gemini CLI](#introduction-to-gemini-cli)
2. [Installation and Setup](#installation-and-setup)
3. [Getting Started](#getting-started)
4. [Basic Commands](#basic-commands)
5. [Core Features](#core-features)
6. [Advanced Features](#advanced-features)
7. [File Operations](#file-operations)
8. [Code Generation and Development](#code-generation-and-development)
9. [Integration and Automation](#integration-and-automation)
10. [Advanced Techniques](#advanced-techniques)
11. [Troubleshooting and Optimization](#troubleshooting-and-optimization)
12. [Real-World Projects](#real-world-projects)
13. [Resources and Next Steps](#resources-and-next-steps)

---

## Introduction to Gemini CLI

### What is Gemini CLI?

Gemini CLI is Google's official command-line interface for interacting with Google's Gemini AI models. It provides a powerful, scriptable way to leverage Gemini's capabilities directly from your terminal, enabling automation, batch processing, and integration into development workflows.

### Why Gemini CLI?

**Key Advantages:**
- **Terminal-Native:** Work directly from command line
- **Scriptable:** Integrate into automation workflows
- **Fast:** No GUI overhead, direct API access
- **Flexible:** Supports various input/output formats
- **Powerful:** Access to all Gemini model capabilities
- **Free Tier:** Generous free usage limits
- **Multi-Model:** Support for different Gemini models

### Gemini CLI vs. Other Tools

| Aspect | Gemini CLI | ChatGPT Web | Claude CLI | Gemini Web |
|--------|------------|-------------|------------|------------|
| **Interface** | ⭐⭐⭐⭐⭐ CLI | ⭐⭐⭐ Web | ⭐⭐⭐⭐⭐ CLI | ⭐⭐⭐ Web |
| **Automation** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Limited | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Limited |
| **Scripting** | ⭐⭐⭐⭐⭐ Native | ⭐⭐ None | ⭐⭐⭐⭐⭐ Native | ⭐⭐ None |
| **Batch Processing** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Manual | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Manual |
| **Integration** | ⭐⭐⭐⭐⭐ Easy | ⭐⭐ Difficult | ⭐⭐⭐⭐⭐ Easy | ⭐⭐ Difficult |
| **Cost** | ⭐⭐⭐⭐ Free tier | ⭐⭐⭐ Paid | ⭐⭐⭐⭐ Free tier | ⭐⭐⭐⭐ Free tier |
| **Speed** | ⭐⭐⭐⭐⭐ Fast | ⭐⭐⭐ Medium | ⭐⭐⭐⭐⭐ Fast | ⭐⭐⭐ Medium |

### Use Cases

**Perfect For:**
- ✅ Code generation and review
- ✅ Batch file processing
- ✅ Automation scripts
- ✅ CI/CD integration
- ✅ Documentation generation
- ✅ Data analysis
- ✅ Text processing
- ✅ Report generation

---

## Installation and Setup

### System Requirements

**Minimum Requirements:**
- **Node.js:** Version 18.0.0 or higher
- **npm:** Version 9.0.0 or higher (comes with Node.js)
- **Operating System:** macOS, Linux, or Windows
- **RAM:** 4GB minimum
- **Internet:** Required for API access

**Recommended:**
- Node.js 20+ (LTS version)
- 8GB+ RAM
- Stable internet connection
- Terminal with color support

### Installation Methods

#### Method 1: npm (Recommended)

**Global Installation:**
```bash
npm install -g @google/gemini-cli
```

**Verify Installation:**
```bash
gemini --version
```

**Expected Output:**
```
@google/gemini-cli/1.0.0
```

#### Method 2: Yarn

**Global Installation:**
```bash
yarn global add @google/gemini-cli
```

**Verify Installation:**
```bash
gemini --version
```

#### Method 3: npx (No Installation)

**Run Without Installing:**
```bash
npx @google/gemini-cli ask "Hello, Gemini!"
```

**Note:** First run will download the package, subsequent runs use cache.

#### Method 4: From Source

**Clone and Build:**
```bash
git clone https://github.com/google/gemini-cli.git
cd gemini-cli
npm install
npm link  # Makes 'gemini' command available globally
```

### Platform-Specific Installation

#### macOS

**Using Homebrew (if available):**
```bash
brew install node
npm install -g @google/gemini-cli
```

**Manual Installation:**
1. Install Node.js from https://nodejs.org
2. Open Terminal
3. Run: `npm install -g @google/gemini-cli`

#### Windows

**Using Chocolatey:**
```bash
choco install nodejs
npm install -g @google/gemini-cli
```

**Manual Installation:**
1. Download Node.js installer from https://nodejs.org
2. Run installer
3. Open Command Prompt or PowerShell
4. Run: `npm install -g @google/gemini-cli`

#### Linux

**Ubuntu/Debian:**
```bash
# Install Node.js
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt-get install -y nodejs

# Install Gemini CLI
sudo npm install -g @google/gemini-cli
```

**Fedora/RHEL:**
```bash
# Install Node.js
sudo dnf install nodejs npm

# Install Gemini CLI
sudo npm install -g @google/gemini-cli
```

### Authentication Setup

#### Method 1: Google Account Login (Recommended)

**Interactive Login:**
```bash
gemini auth login
```

**What Happens:**
1. Opens browser window
2. Prompts Google account sign-in
3. Requests permissions
4. Stores credentials locally

**Verify Login:**
```bash
gemini auth status
```

#### Method 2: API Key (For Automation)

**Get API Key:**
1. Visit https://makersuite.google.com/app/apikey
2. Sign in with Google account
3. Create new API key
4. Copy the key

**Set API Key:**

**macOS/Linux:**
```bash
export GEMINI_API_KEY="your-api-key-here"
```

**Windows (PowerShell):**
```powershell
$env:GEMINI_API_KEY="your-api-key-here"
```

**Windows (Command Prompt):**
```cmd
set GEMINI_API_KEY=your-api-key-here
```

**Make Permanent:**

**macOS/Linux (.bashrc or .zshrc):**
```bash
echo 'export GEMINI_API_KEY="your-api-key-here"' >> ~/.bashrc
source ~/.bashrc
```

**Windows (Environment Variables):**
1. System Properties → Environment Variables
2. Add `GEMINI_API_KEY` with your key
3. Restart terminal

**Verify API Key:**
```bash
gemini auth status
```

### Configuration

#### Configuration File Location

**macOS/Linux:**
```
~/.config/gemini-cli/config.json
```

**Windows:**
```
%APPDATA%\gemini-cli\config.json
```

#### Create Configuration File

**Manual Creation:**
```bash
mkdir -p ~/.config/gemini-cli
cat > ~/.config/gemini-cli/config.json << EOF
{
  "apiKey": "your-api-key-here",
  "model": "gemini-pro",
  "temperature": 0.7,
  "maxTokens": 2048
}
EOF
```

**Using CLI:**
```bash
gemini config set model gemini-pro
gemini config set temperature 0.7
gemini config set maxTokens 2048
```

#### Configuration Options

**Available Settings:**
- `apiKey`: Your Gemini API key
- `model`: Model to use (gemini-pro, gemini-pro-vision, etc.)
- `temperature`: Creativity (0.0-1.0)
- `maxTokens`: Maximum response length
- `topP`: Nucleus sampling parameter
- `topK`: Top-K sampling parameter

**View Configuration:**
```bash
gemini config list
```

**Reset Configuration:**
```bash
gemini config reset
```

### Verification

**Test Installation:**
```bash
gemini ask "Hello, what is 2+2?"
```

**Expected Output:**
```
Hello! 2 + 2 equals 4.
```

**If you see an error, check:**
- Node.js version: `node --version` (should be 18+)
- Installation: `gemini --version`
- Authentication: `gemini auth status`
- API Key: `echo $GEMINI_API_KEY` (macOS/Linux) or `echo %GEMINI_API_KEY%` (Windows)

---

## Getting Started

### Your First Command

**Simple Query:**
```bash
gemini ask "What is artificial intelligence?"
```

**Output:**
```
Artificial intelligence (AI) is the simulation of human intelligence 
in machines that are programmed to think and learn like humans...
```

### Interactive Mode

**Start Interactive Session:**
```bash
gemini chat
```

**Interactive Features:**
- Multi-turn conversations
- Context preservation
- Command history
- Auto-completion

**Example Session:**
```bash
$ gemini chat
> Hello, I'm learning Gemini CLI
Hello! I'm here to help you learn Gemini CLI. What would you like to know?

> How do I generate code?
You can generate code using the 'generate' command or in chat mode...

> exit
Goodbye!
```

**Exit Interactive Mode:**
- Type `exit` or `quit`
- Press `Ctrl+C`
- Type `/exit`

### Basic Command Structure

**General Syntax:**
```bash
gemini [command] [options] [arguments]
```

**Common Commands:**
- `ask`: Ask a question
- `chat`: Interactive chat mode
- `generate`: Generate code or text
- `analyze`: Analyze code or files
- `config`: Configuration management
- `auth`: Authentication management

**Get Help:**
```bash
gemini --help
gemini [command] --help
```

---

## Basic Commands

### 1. Ask Command

**Simple Questions:**
```bash
gemini ask "What is Python?"
```

**With Options:**
```bash
gemini ask "Explain closures in JavaScript" --model gemini-pro --temperature 0.5
```

**Options:**
- `--model`: Specify model (default: gemini-pro)
- `--temperature`: Control creativity (0.0-1.0)
- `--max-tokens`: Limit response length
- `--format`: Output format (text, json, markdown)

**Examples:**

**Greenshades Context:**
```bash
gemini ask "How do I calculate payroll tax for an employee in California?"
```

**Code Explanation:**
```bash
gemini ask "Explain this Python function: def calculate_net_pay(gross, tax_rate): return gross * (1 - tax_rate)"
```

**Multiple Questions:**
```bash
gemini ask "What is async/await? Give me a Python example."
```

### 2. Chat Command

**Start Chat:**
```bash
gemini chat
```

**Chat Features:**
- **Context Preservation:** Remembers conversation
- **Multi-turn:** Natural conversation flow
- **History:** Access previous messages
- **Commands:** Special commands (see below)

**Chat Commands:**
- `/help`: Show help
- `/clear`: Clear conversation history
- `/save`: Save conversation to file
- `/load`: Load conversation from file
- `/model`: Switch model
- `/exit`: Exit chat

**Example Chat Session:**
```bash
$ gemini chat
> I need to create a payroll calculation function
I can help you create a payroll calculation function. What specific 
requirements do you have?

> It should calculate net pay from gross pay, tax rate, and deductions
Here's a Python function for that:

def calculate_net_pay(gross_pay, tax_rate, deductions):
    tax = gross_pay * tax_rate
    total_deductions = sum(deductions)
    return gross_pay - tax - total_deductions

> Can you add error handling?
Sure! Here's an improved version with error handling:

def calculate_net_pay(gross_pay, tax_rate, deductions):
    if gross_pay < 0:
        raise ValueError("Gross pay cannot be negative")
    if not 0 <= tax_rate <= 1:
        raise ValueError("Tax rate must be between 0 and 1")
    if not isinstance(deductions, (list, tuple)):
        raise TypeError("Deductions must be a list or tuple")
    
    tax = gross_pay * tax_rate
    total_deductions = sum(deductions)
    net_pay = gross_pay - tax - total_deductions
    
    if net_pay < 0:
        raise ValueError("Net pay cannot be negative")
    
    return net_pay

> /exit
```

### 3. Generate Command

**Generate Code:**
```bash
gemini generate "Create a Python function to calculate payroll tax"
```

**Generate with Options:**
```bash
gemini generate "Create a REST API endpoint for payroll processing" \
  --language python \
  --framework flask \
  --output payroll_api.py
```

**Options:**
- `--language`: Programming language
- `--framework`: Framework/library
- `--output`: Output file path
- `--format`: Code format/style

**Examples:**

**Python Function:**
```bash
gemini generate "Create a function that validates employee tax information" \
  --language python \
  --output validate_tax.py
```

**JavaScript Class:**
```bash
gemini generate "Create a PayrollCalculator class in JavaScript" \
  --language javascript \
  --output PayrollCalculator.js
```

**Complete Module:**
```bash
gemini generate "Create a complete payroll processing module with:
- Employee data model
- Tax calculation functions
- Payroll processing logic
- Error handling
- Unit tests" \
  --language python \
  --output payroll_module.py
```

### 4. Analyze Command

**Analyze Code File:**
```bash
gemini analyze payroll_calculator.py
```

**Analyze with Options:**
```bash
gemini analyze payroll_calculator.py \
  --check security \
  --check performance \
  --check best-practices \
  --output analysis.json
```

**Options:**
- `--check`: What to check (security, performance, bugs, style)
- `--output`: Save analysis to file
- `--format`: Output format (text, json, markdown)

**Examples:**

**Security Analysis:**
```bash
gemini analyze api_routes.py --check security
```

**Performance Analysis:**
```bash
gemini analyze data_processor.py --check performance
```

**Comprehensive Analysis:**
```bash
gemini analyze payroll_system.py \
  --check security \
  --check performance \
  --check bugs \
  --check best-practices
```

**Output Example:**
```
Analysis of payroll_system.py:

Security Issues:
- ⚠️ Line 45: SQL injection risk in query construction
- ⚠️ Line 78: Sensitive data logged without encryption

Performance Issues:
- ⚠️ Line 120: N+1 query problem in employee lookup
- ⚠️ Line 200: Inefficient loop, consider using list comprehension

Best Practices:
- ✅ Good use of type hints
- ⚠️ Missing docstrings for public functions
- ⚠️ Magic numbers should be constants

Bugs:
- ⚠️ Line 95: Potential division by zero if hours == 0
```

### 5. Config Command

**View Configuration:**
```bash
gemini config list
```

**Set Configuration:**
```bash
gemini config set model gemini-pro
gemini config set temperature 0.7
gemini config set maxTokens 2048
```

**Get Configuration Value:**
```bash
gemini config get model
```

**Reset Configuration:**
```bash
gemini config reset
```

**Configuration Options:**
- `model`: AI model to use
- `temperature`: Creativity (0.0-1.0)
- `maxTokens`: Maximum tokens
- `topP`: Nucleus sampling
- `topK`: Top-K sampling

### 6. Auth Command

**Login:**
```bash
gemini auth login
```

**Check Status:**
```bash
gemini auth status
```

**Logout:**
```bash
gemini auth logout
```

**Set API Key:**
```bash
gemini auth set-key YOUR_API_KEY
```

---

## Core Features

### 1. Text Generation

**Basic Generation:**
```bash
gemini generate "Write a summary of payroll processing best practices"
```

**With Parameters:**
```bash
gemini generate "Explain tax calculation methods" \
  --temperature 0.3 \
  --max-tokens 500 \
  --format markdown
```

**Greenshades Example:**
```bash
gemini generate "Create documentation for the Avocado payroll platform API endpoints"
```

### 2. Code Generation

**Simple Function:**
```bash
gemini generate "Create a Python function to calculate net pay from gross pay and deductions"
```

**Complete Module:**
```bash
gemini generate "Create a complete Python module for payroll tax calculation:
- Support for federal, state, and local taxes
- Handle different employee types (W2, 1099)
- Include error handling and validation
- Add comprehensive docstrings
- Include type hints" \
  --language python \
  --output tax_calculator.py
```

**With Framework:**
```bash
gemini generate "Create a Flask API endpoint for processing payroll runs" \
  --language python \
  --framework flask \
  --output payroll_api.py
```

### 3. File Processing

**Process Single File:**
```bash
gemini process payroll_data.csv --task "Extract employee information"
```

**Process Multiple Files:**
```bash
gemini process *.py --task "Add type hints to all functions"
```

**Process with Output:**
```bash
gemini process input.txt --task "Summarize this document" --output summary.txt
```

### 4. Multi-Turn Conversations

**In Chat Mode:**
```bash
gemini chat
> Create a payroll calculation function
[AI generates function]
> Add error handling
[AI adds error handling]
> Now add logging
[AI adds logging]
```

**Using Context:**
```bash
gemini ask "Create a function to calculate overtime pay" \
  --context "We're building a payroll system for hourly employees"
```

### 5. Context Management

**Add Context:**
```bash
gemini ask "How do I implement this?" \
  --context-file requirements.txt \
  --context-file existing_code.py
```

**Context from Files:**
```bash
gemini generate "Refactor this code" \
  --context payroll_calculator.py \
  --context tax_engine.py
```

**Context from Environment:**
```bash
export GEMINI_CONTEXT="We're building a payroll system for Greenshades"
gemini ask "What's the best approach for tax calculation?"
```

### 6. Model Selection

**Available Models:**
- `gemini-pro`: General purpose (default)
- `gemini-pro-vision`: Image understanding
- `gemini-ultra`: Most capable (if available)

**Select Model:**
```bash
gemini ask "Analyze this code" --model gemini-pro
```

**Set Default Model:**
```bash
gemini config set model gemini-pro
```

### 7. Temperature and Parameters

**Temperature Control:**
```bash
# Creative (higher temperature)
gemini generate "Write a creative story" --temperature 0.9

# Focused (lower temperature)
gemini generate "Calculate payroll tax" --temperature 0.1
```

**Other Parameters:**
```bash
gemini ask "Explain this" \
  --temperature 0.7 \
  --top-p 0.9 \
  --top-k 40 \
  --max-tokens 1000
```

---

## Advanced Features

### 1. Batch Processing

**Process Multiple Files:**
```bash
gemini batch process *.py --task "Add docstrings to all functions"
```

**Batch with Configuration:**
```bash
gemini batch process data/*.csv \
  --task "Extract key information" \
  --output processed/ \
  --parallel 4
```

**Batch Script:**
```bash
#!/bin/bash
for file in *.py; do
  gemini analyze "$file" --output "analysis_${file}.json"
done
```

### 2. Streaming Responses

**Stream Output:**
```bash
gemini ask "Explain payroll processing" --stream
```

**Stream to File:**
```bash
gemini generate "Create payroll documentation" --stream --output doc.md
```

**Use in Scripts:**
```bash
gemini ask "Generate report" --stream | tee report.txt
```

### 3. Custom Prompts

**Use Prompt File:**
```bash
gemini ask --prompt-file prompt.txt
```

**Prompt File Example (prompt.txt):**
```
You are a senior software engineer at Greenshades, specializing in payroll systems.

Task: Review the provided code and suggest improvements for:
- Security
- Performance
- Maintainability
- Best practices

Code to review:
{{code}}
```

**Template Variables:**
```bash
gemini ask --prompt-file review_prompt.txt \
  --var code="$(cat payroll.py)" \
  --var language="Python"
```

### 4. Template Usage

**Create Template:**
```bash
gemini template create code-review \
  "Review this {{language}} code for security issues: {{code}}"
```

**Use Template:**
```bash
gemini template use code-review \
  --var language="Python" \
  --var code="$(cat file.py)"
```

**List Templates:**
```bash
gemini template list
```

**Delete Template:**
```bash
gemini template delete code-review
```

### 5. Configuration Files

**Project-Specific Config:**
```bash
# .geminirc
{
  "model": "gemini-pro",
  "temperature": 0.7,
  "maxTokens": 2048,
  "defaultLanguage": "python",
  "outputFormat": "markdown"
}
```

**Use Config:**
```bash
gemini ask "Generate code" --config .geminirc
```

### 6. Environment Variables

**Available Variables:**
- `GEMINI_API_KEY`: API key
- `GEMINI_MODEL`: Default model
- `GEMINI_TEMPERATURE`: Default temperature
- `GEMINI_MAX_TOKENS`: Default max tokens
- `GEMINI_OUTPUT_DIR`: Default output directory

**Set in Shell:**
```bash
export GEMINI_API_KEY="your-key"
export GEMINI_MODEL="gemini-pro"
export GEMINI_TEMPERATURE="0.7"
```

**Use in Scripts:**
```bash
#!/bin/bash
export GEMINI_API_KEY="${GEMINI_API_KEY}"
gemini ask "Generate code"
```

### 7. Scripting Integration

**Bash Script:**
```bash
#!/bin/bash
# generate_payroll_module.sh

RESULT=$(gemini generate "Create payroll calculation module" \
  --language python \
  --output payroll.py)

if [ $? -eq 0 ]; then
  echo "Generated successfully"
  python -m pytest payroll_test.py
else
  echo "Generation failed"
  exit 1
fi
```

**Python Script:**
```python
#!/usr/bin/env python3
import subprocess
import json

def generate_code(prompt, language="python"):
    result = subprocess.run(
        ["gemini", "generate", prompt, "--language", language, "--format", "json"],
        capture_output=True,
        text=True
    )
    return json.loads(result.stdout)

code = generate_code("Create payroll tax calculator", "python")
print(code["content"])
```

**Node.js Script:**
```javascript
const { execSync } = require('child_process');

function generateCode(prompt, language = 'javascript') {
  const command = `gemini generate "${prompt}" --language ${language} --format json`;
  const result = execSync(command, { encoding: 'utf-8' });
  return JSON.parse(result);
}

const code = generateCode('Create payroll calculator class', 'javascript');
console.log(code.content);
```

---

## File Operations

### Reading Files

**Read and Process:**
```bash
gemini process payroll_data.csv --task "Extract employee information"
```

**Read with Context:**
```bash
gemini ask "Explain this code" --file payroll_calculator.py
```

**Read Multiple Files:**
```bash
gemini analyze payroll.py tax_engine.py employee.py
```

### Writing Files

**Save Output:**
```bash
gemini generate "Create payroll module" --output payroll.py
```

**Append to File:**
```bash
gemini ask "Generate test cases" --output tests.py --append
```

**Format Output:**
```bash
gemini generate "Create API documentation" \
  --format markdown \
  --output api_docs.md
```

### Processing Multiple Files

**Batch Process:**
```bash
gemini batch process src/*.py --task "Add type hints"
```

**Process with Pattern:**
```bash
gemini batch process "**/*.py" --task "Add docstrings"
```

**Process Directory:**
```bash
gemini batch process ./src --task "Format code" --recursive
```

### File Formats

**Supported Formats:**
- Text files (`.txt`, `.md`)
- Code files (`.py`, `.js`, `.java`, etc.)
- Data files (`.csv`, `.json`, `.xml`)
- Configuration files (`.yaml`, `.toml`, `.ini`)

**Format-Specific Processing:**
```bash
# JSON
gemini process data.json --task "Extract key fields"

# CSV
gemini process employees.csv --task "Calculate statistics"

# Code
gemini analyze *.py --check security
```

### Large File Handling

**Stream Processing:**
```bash
cat large_file.txt | gemini process --stream --task "Summarize"
```

**Chunk Processing:**
```bash
gemini process large_file.txt \
  --task "Process in chunks" \
  --chunk-size 1000 \
  --output processed.txt
```

**Memory-Efficient:**
```bash
gemini process large_file.txt \
  --task "Extract information" \
  --memory-efficient \
  --output result.txt
```

### Directory Operations

**Process Directory:**
```bash
gemini batch process ./src --recursive --task "Add documentation"
```

**Filter Files:**
```bash
gemini batch process ./src \
  --include "*.py" \
  --exclude "test_*" \
  --task "Format code"
```

**Output to Directory:**
```bash
gemini batch process ./src \
  --task "Generate documentation" \
  --output-dir ./docs
```

---

## Code Generation and Development

### Code Generation Workflows

#### Workflow 1: Generate from Specification

**Step 1: Create Specification**
```bash
cat > spec.txt << EOF
Create a Python function that:
- Calculates payroll tax for employees
- Handles federal, state, and local taxes
- Validates input data
- Returns detailed breakdown
EOF
```

**Step 2: Generate Code**
```bash
gemini generate --prompt-file spec.txt \
  --language python \
  --output payroll_tax.py
```

**Step 3: Review and Refine**
```bash
gemini analyze payroll_tax.py --check security --check best-practices
```

#### Workflow 2: Generate with Context

**Generate with Existing Code:**
```bash
gemini generate "Add error handling to this function" \
  --context payroll_calculator.py \
  --output improved_calculator.py
```

**Generate Matching Style:**
```bash
gemini generate "Create similar function" \
  --context existing_functions.py \
  --match-style \
  --output new_function.py
```

#### Workflow 3: Iterative Development

**Iteration 1: Basic Function**
```bash
gemini generate "Create payroll calculation function" --output v1.py
```

**Iteration 2: Add Features**
```bash
gemini generate "Add error handling and logging" \
  --context v1.py \
  --output v2.py
```

**Iteration 3: Optimize**
```bash
gemini generate "Optimize for performance" \
  --context v2.py \
  --output v3.py
```

### Code Review

**Review Single File:**
```bash
gemini analyze payroll.py --check security --check performance
```

**Review with Suggestions:**
```bash
gemini analyze payroll.py \
  --check all \
  --suggest-fixes \
  --output review.md
```

**Review Multiple Files:**
```bash
gemini analyze src/*.py --check security --output security_review.json
```

**Greenshades Example:**
```bash
gemini analyze avocado_payroll.py \
  --check security \
  --check performance \
  --check best-practices \
  --context "This is payroll processing code for Greenshades Avocado platform"
```

### Code Explanation

**Explain Function:**
```bash
gemini explain payroll_calculator.py:calculate_net_pay
```

**Explain File:**
```bash
gemini explain payroll_calculator.py
```

**Explain with Context:**
```bash
gemini explain tax_engine.py \
  --context "This is part of Greenshades payroll system"
```

### Refactoring Assistance

**Refactor Function:**
```bash
gemini refactor payroll_calculator.py:calculate_net_pay \
  --goal "Improve performance and add type hints"
```

**Refactor File:**
```bash
gemini refactor legacy_code.py \
  --goal "Modernize to Python 3.11+ with type hints and async/await"
```

**Refactor with Tests:**
```bash
gemini refactor payroll.py \
  --goal "Improve structure" \
  --preserve-tests \
  --output refactored_payroll.py
```

### Testing Generation

**Generate Unit Tests:**
```bash
gemini generate "Create unit tests for payroll_calculator.py" \
  --context payroll_calculator.py \
  --language python \
  --framework pytest \
  --output test_payroll.py
```

**Generate Test Cases:**
```bash
gemini generate "Generate test cases for tax calculation function" \
  --context tax_calculator.py \
  --output test_cases.json
```

**Generate Integration Tests:**
```bash
gemini generate "Create integration tests for payroll API" \
  --context api_routes.py \
  --output test_integration.py
```

### Documentation Generation

**Generate Docstrings:**
```bash
gemini generate "Add comprehensive docstrings to all functions" \
  --context payroll.py \
  --output documented_payroll.py
```

**Generate API Documentation:**
```bash
gemini generate "Generate API documentation from code" \
  --context api_routes.py \
  --format markdown \
  --output api_docs.md
```

**Generate README:**
```bash
gemini generate "Create comprehensive README for this project" \
  --context src/ \
  --output README.md
```

---

## Integration and Automation

### Shell Scripting Integration

**Simple Script:**
```bash
#!/bin/bash
# generate_payroll_code.sh

PROMPT="Create a Python function to calculate payroll tax"
OUTPUT="payroll_tax.py"

gemini generate "$PROMPT" \
  --language python \
  --output "$OUTPUT"

if [ $? -eq 0 ]; then
  echo "✅ Generated $OUTPUT"
  python -m py_compile "$OUTPUT"
else
  echo "❌ Generation failed"
  exit 1
fi
```

**Advanced Script:**
```bash
#!/bin/bash
# automate_code_review.sh

FILES=("payroll.py" "tax_engine.py" "employee.py")

for file in "${FILES[@]}"; do
  echo "Reviewing $file..."
  gemini analyze "$file" \
    --check all \
    --output "review_${file}.json"
done

echo "All reviews complete!"
```

### Makefile Integration

**Makefile Example:**
```makefile
.PHONY: generate-code review-code generate-docs

generate-code:
	gemini generate "Create payroll calculation module" \
		--language python \
		--output src/payroll.py

review-code:
	gemini analyze src/*.py --check all --output reviews/

generate-docs:
	gemini generate "Generate API documentation" \
		--context src/ \
		--format markdown \
		--output docs/api.md

test: generate-code
	python -m pytest tests/

all: generate-code review-code generate-docs test
```

**Usage:**
```bash
make generate-code
make review-code
make generate-docs
make all
```

### CI/CD Integration

**GitHub Actions Example:**
```yaml
name: Code Review with Gemini

on: [pull_request]

jobs:
  review:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '20'
      
      - name: Install Gemini CLI
        run: npm install -g @google/gemini-cli
      
      - name: Run Code Review
        env:
          GEMINI_API_KEY: ${{ secrets.GEMINI_API_KEY }}
        run: |
          gemini analyze src/*.py \
            --check security \
            --check performance \
            --output review.json
      
      - name: Upload Review
        uses: actions/upload-artifact@v3
        with:
          name: code-review
          path: review.json
```

**GitLab CI Example:**
```yaml
stages:
  - review

code_review:
  stage: review
  image: node:20
  before_script:
    - npm install -g @google/gemini-cli
  script:
    - gemini analyze src/*.py --check all --output review.json
  artifacts:
    paths:
      - review.json
```

### API Integration

**REST API Wrapper:**
```python
#!/usr/bin/env python3
from flask import Flask, request, jsonify
import subprocess
import json

app = Flask(__name__)

@app.route('/api/generate', methods=['POST'])
def generate():
    data = request.json
    prompt = data.get('prompt')
    language = data.get('language', 'python')
    
    result = subprocess.run(
        ['gemini', 'generate', prompt, '--language', language, '--format', 'json'],
        capture_output=True,
        text=True
    )
    
    return jsonify(json.loads(result.stdout))

if __name__ == '__main__':
    app.run(port=5000)
```

**Usage:**
```bash
curl -X POST http://localhost:5000/api/generate \
  -H "Content-Type: application/json" \
  -d '{"prompt": "Create payroll function", "language": "python"}'
```

### Scheduled Tasks

**Cron Job Example:**
```bash
# Run daily code review at 2 AM
0 2 * * * /usr/local/bin/gemini analyze src/*.py --check all --output /var/reviews/daily-$(date +\%Y-\%m-\%d).json
```

**Systemd Timer Example:**
```ini
[Unit]
Description=Daily Code Review with Gemini

[Timer]
OnCalendar=daily
Persistent=true

[Install]
WantedBy=timers.target
```

### Webhook Support

**Webhook Handler:**
```python
from flask import Flask, request
import subprocess

app = Flask(__name__)

@app.route('/webhook/gemini', methods=['POST'])
def webhook():
    event = request.json
    
    if event['type'] == 'code_review':
        subprocess.run([
            'gemini', 'analyze', event['file'],
            '--check', 'all',
            '--output', f"review_{event['file']}.json"
        ])
    
    return {'status': 'ok'}
```

---

## Advanced Techniques

### 1. Prompt Engineering for CLI

#### Effective Prompts

**✅ Good Prompts:**
```bash
gemini generate "Create a Python function that calculates payroll tax:
- Input: gross_pay (float), tax_rate (float), state (string)
- Output: tax_amount (float)
- Handle edge cases: zero pay, invalid state
- Include type hints and docstring
- Add error handling
- Follow PEP 8 style"
```

**❌ Bad Prompts:**
```bash
gemini generate "make tax function"
```

#### Prompt Patterns

**Pattern 1: Specification-Based**
```bash
gemini generate "Create [what] that [does what]:
- Requirement 1
- Requirement 2
- Requirement 3
- Include [features]
- Handle [edge cases]"
```

**Pattern 2: Example-Based**
```bash
gemini generate "Create similar to @existing.py but for [purpose]:
- Similar structure
- Different logic: [describe]
- Same error handling"
```

**Pattern 3: Iterative Refinement**
```bash
# Step 1: Basic
gemini generate "Create payroll function" --output v1.py

# Step 2: Add features
gemini generate "Add error handling and logging" --context v1.py --output v2.py

# Step 3: Optimize
gemini generate "Optimize for performance" --context v2.py --output v3.py
```

### 2. Context Management

#### Managing Context Window

**Add Files to Context:**
```bash
gemini ask "How do these work together?" \
  --file file1.py \
  --file file2.py \
  --file file3.py
```

**Context from Directory:**
```bash
gemini generate "Refactor this codebase" \
  --context-dir src/ \
  --output refactored/
```

**Optimize Context:**
- Be selective about which files to include
- Use file paths, not entire directories
- Focus on relevant files
- Remove unnecessary context

#### Context Strategies

**Strategy 1: Minimal Context**
```bash
gemini generate "Create function" --context relevant_file.py
```

**Strategy 2: Related Context**
```bash
gemini generate "Refactor" \
  --context file1.py \
  --context file2.py \
  --context file3.py
```

**Strategy 3: Full Codebase**
```bash
gemini generate "Analyze architecture" --context-dir ./
```

### 3. Multi-File Processing

**Process Related Files:**
```bash
gemini batch process payroll*.py --task "Add type hints"
```

**Process with Dependencies:**
```bash
gemini process main.py \
  --context utils.py \
  --context models.py \
  --task "Refactor to use dependency injection"
```

**Process Directory Tree:**
```bash
gemini batch process src/ \
  --recursive \
  --task "Add documentation" \
  --output-dir docs/
```

### 4. Performance Optimization

#### Optimization Tips

**1. Batch Operations:**
```bash
# Instead of loop
for file in *.py; do
  gemini analyze "$file"
done

# Use batch
gemini batch process *.py --task "Analyze"
```

**2. Parallel Processing:**
```bash
gemini batch process *.py --task "Process" --parallel 4
```

**3. Cache Results:**
```bash
gemini analyze file.py --cache --output analysis.json
```

**4. Stream Large Files:**
```bash
cat large_file.txt | gemini process --stream
```

**5. Limit Context:**
```bash
# Don't include entire codebase
gemini generate "Create function" --context relevant.py

# Instead of
gemini generate "Create function" --context-dir ./
```

### 5. Error Handling

#### Retry Strategies

**Automatic Retry:**
```bash
gemini ask "Question" --retry 3 --retry-delay 5
```

**Manual Retry Script:**
```bash
#!/bin/bash
MAX_RETRIES=3
RETRY_DELAY=5

for i in $(seq 1 $MAX_RETRIES); do
  if gemini generate "Create code" --output code.py; then
    echo "Success!"
    exit 0
  else
    echo "Attempt $i failed, retrying in $RETRY_DELAY seconds..."
    sleep $RETRY_DELAY
  fi
done

echo "Failed after $MAX_RETRIES attempts"
exit 1
```

#### Error Recovery

**Check for Errors:**
```bash
if ! gemini generate "Create code" --output code.py; then
  echo "Generation failed, trying alternative approach..."
  gemini generate "Create simpler version" --output code.py
fi
```

### 6. Output Formatting

#### Format Options

**Text Format:**
```bash
gemini ask "Explain" --format text
```

**JSON Format:**
```bash
gemini ask "Explain" --format json
```

**Markdown Format:**
```bash
gemini generate "Create documentation" --format markdown --output doc.md
```

**Custom Format:**
```bash
gemini ask "Explain" --format json | jq '.content'
```

#### Post-Processing

**Format with External Tools:**
```bash
gemini generate "Create code" --output code.py
black code.py  # Format Python code
isort code.py  # Sort imports
```

**Pipeline Processing:**
```bash
gemini generate "Create code" \
  | python -m black --stdin \
  | python -m isort --stdin \
  > formatted_code.py
```

---

## Troubleshooting and Optimization

### Common Issues and Solutions

#### Issue 1: Authentication Failed

**Symptoms:**
```
Error: Authentication failed
Error: Invalid API key
```

**Solutions:**

1. **Check API Key:**
   ```bash
   echo $GEMINI_API_KEY
   gemini auth status
   ```

2. **Re-authenticate:**
   ```bash
   gemini auth logout
   gemini auth login
   ```

3. **Set API Key:**
   ```bash
   export GEMINI_API_KEY="your-key-here"
   gemini auth set-key "your-key-here"
   ```

4. **Verify Key:**
   ```bash
   gemini ask "test"  # Should work if key is valid
   ```

#### Issue 2: Rate Limiting

**Symptoms:**
```
Error: Rate limit exceeded
Error: Too many requests
```

**Solutions:**

1. **Check Rate Limits:**
   - Free tier: Limited requests per minute
   - Paid tier: Higher limits
   - Check your quota at https://makersuite.google.com

2. **Implement Backoff:**
   ```bash
   # Add delay between requests
   gemini ask "Question 1"
   sleep 2
   gemini ask "Question 2"
   ```

3. **Use Batch Processing:**
   ```bash
   # More efficient than individual requests
   gemini batch process *.py --task "Process"
   ```

4. **Upgrade Plan:**
   - Consider upgrading to paid tier
   - Higher rate limits
   - Priority access

#### Issue 3: Installation Problems

**Symptoms:**
```
Error: Command not found: gemini
Error: npm install failed
```

**Solutions:**

1. **Check Node.js:**
   ```bash
   node --version  # Should be 18+
   npm --version
   ```

2. **Reinstall:**
   ```bash
   npm uninstall -g @google/gemini-cli
   npm install -g @google/gemini-cli
   ```

3. **Check Permissions:**
   ```bash
   # macOS/Linux
   sudo npm install -g @google/gemini-cli
   
   # Or fix permissions
   sudo chown -R $(whoami) ~/.npm
   ```

4. **Use npx:**
   ```bash
   npx @google/gemini-cli ask "Hello"
   ```

#### Issue 4: API Errors

**Symptoms:**
```
Error: API request failed
Error: Invalid response
```

**Solutions:**

1. **Check Internet Connection:**
   ```bash
   ping google.com
   ```

2. **Check API Status:**
   - Visit https://status.cloud.google.com
   - Check for outages

3. **Retry with Backoff:**
   ```bash
   gemini ask "Question" --retry 3
   ```

4. **Check API Key:**
   ```bash
   gemini auth status
   ```

#### Issue 5: File Processing Errors

**Symptoms:**
```
Error: File not found
Error: Cannot read file
```

**Solutions:**

1. **Check File Path:**
   ```bash
   ls -la file.py
   gemini process ./file.py
   ```

2. **Check Permissions:**
   ```bash
   chmod +r file.py
   gemini process file.py
   ```

3. **Use Absolute Path:**
   ```bash
   gemini process /full/path/to/file.py
   ```

4. **Check File Format:**
   - Ensure file is readable
   - Check encoding (UTF-8 recommended)
   - Verify file isn't corrupted

### Performance Optimization

#### Optimization Strategies

**1. Batch Processing:**
```bash
# Efficient
gemini batch process *.py --task "Process"

# Inefficient
for file in *.py; do
  gemini process "$file" --task "Process"
done
```

**2. Parallel Processing:**
```bash
gemini batch process *.py --task "Process" --parallel 4
```

**3. Caching:**
```bash
gemini analyze file.py --cache --output analysis.json
```

**4. Streaming:**
```bash
cat large_file.txt | gemini process --stream
```

**5. Context Optimization:**
```bash
# Good: Selective context
gemini generate "Create" --context relevant.py

# Bad: Entire codebase
gemini generate "Create" --context-dir ./
```

#### Memory Management

**Process Large Files in Chunks:**
```bash
gemini process large_file.txt \
  --chunk-size 1000 \
  --output processed.txt
```

**Use Streaming:**
```bash
cat large_file.txt | gemini process --stream > output.txt
```

**Limit Memory Usage:**
```bash
gemini process file.txt --memory-efficient
```

### Configuration Optimization

#### Optimal Settings

**For Code Generation:**
```json
{
  "model": "gemini-pro",
  "temperature": 0.3,
  "maxTokens": 2048
}
```

**For Creative Tasks:**
```json
{
  "model": "gemini-pro",
  "temperature": 0.9,
  "maxTokens": 4096
}
```

**For Analysis:**
```json
{
  "model": "gemini-pro",
  "temperature": 0.1,
  "maxTokens": 1024
}
```

---

## Real-World Projects

### Project 1: Automated Code Review

**Scenario:** Set up automated code review for payroll system.

**Solution:**

**1. Create Review Script:**
```bash
#!/bin/bash
# review_payroll_code.sh

FILES=("payroll_calculator.py" "tax_engine.py" "employee_manager.py")
OUTPUT_DIR="reviews"

mkdir -p "$OUTPUT_DIR"

for file in "${FILES[@]}"; do
  echo "Reviewing $file..."
  gemini analyze "$file" \
    --check security \
    --check performance \
    --check best-practices \
    --output "$OUTPUT_DIR/review_${file}.json"
done

echo "Reviews complete! Check $OUTPUT_DIR/"
```

**2. Schedule Daily Reviews:**
```bash
# Add to crontab
0 2 * * * /path/to/review_payroll_code.sh
```

**3. Integrate with Git:**
```bash
#!/bin/bash
# pre-commit-review.sh

# Run on staged files
git diff --cached --name-only | while read file; do
  if [[ "$file" == *.py ]]; then
    gemini analyze "$file" --check security --check bugs
  fi
done
```

### Project 2: Documentation Generator

**Scenario:** Automatically generate API documentation.

**Solution:**

**1. Generate Docs Script:**
```bash
#!/bin/bash
# generate_docs.sh

API_FILES=("api_routes.py" "models.py" "schemas.py")
OUTPUT="docs/api_documentation.md"

echo "# API Documentation" > "$OUTPUT"
echo "" >> "$OUTPUT"
echo "Generated: $(date)" >> "$OUTPUT"
echo "" >> "$OUTPUT"

for file in "${API_FILES[@]}"; do
  echo "## $file" >> "$OUTPUT"
  gemini generate "Generate API documentation for $file" \
    --context "$file" \
    --format markdown >> "$OUTPUT"
  echo "" >> "$OUTPUT"
done

echo "Documentation generated: $OUTPUT"
```

**2. Auto-Generate on Changes:**
```bash
# Git hook
#!/bin/bash
# post-commit hook

if git diff HEAD~1 --name-only | grep -q "api_routes.py\|models.py"; then
  ./generate_docs.sh
  git add docs/api_documentation.md
  git commit --amend --no-edit
fi
```

### Project 3: Test Generation

**Scenario:** Generate comprehensive test suite.

**Solution:**

**1. Generate Tests:**
```bash
#!/bin/bash
# generate_tests.sh

SOURCE_FILE="payroll_calculator.py"
TEST_FILE="test_payroll_calculator.py"

gemini generate "Create comprehensive unit tests for $SOURCE_FILE:
- Test all functions
- Include edge cases
- Test error handling
- Aim for 90%+ coverage
- Use pytest framework" \
  --context "$SOURCE_FILE" \
  --language python \
  --framework pytest \
  --output "$TEST_FILE"

echo "Tests generated: $TEST_FILE"
python -m pytest "$TEST_FILE" -v
```

**2. Continuous Test Generation:**
```bash
# Makefile
.PHONY: generate-tests test

generate-tests:
	@for file in src/*.py; do \
		test_file="tests/test_$$(basename $$file)"; \
		gemini generate "Create tests for $$file" \
			--context "$$file" \
			--output "$$test_file"; \
	done

test: generate-tests
	pytest tests/ -v --cov=src
```

### Project 4: Code Refactoring Automation

**Scenario:** Automatically refactor legacy code.

**Solution:**

**1. Refactor Script:**
```bash
#!/bin/bash
# refactor_legacy.sh

LEGACY_FILE="legacy_payroll.py"
REFACTORED_FILE="refactored_payroll.py"

echo "Analyzing legacy code..."
gemini analyze "$LEGACY_FILE" \
  --check all \
  --output analysis.json

echo "Refactoring..."
gemini refactor "$LEGACY_FILE" \
  --goal "Modernize to Python 3.11+:
  - Add type hints
  - Use async/await where appropriate
  - Improve error handling
  - Add comprehensive docstrings
  - Follow PEP 8
  - Maintain backward compatibility" \
  --output "$REFACTORED_FILE"

echo "Running tests..."
python -m pytest tests/ -v

echo "Refactoring complete: $REFACTORED_FILE"
```

---

## Resources and Next Steps

### Official Resources

- **Gemini CLI Documentation:** https://developers.google.com/gemini-code-assist/docs/gemini-cli
- **Gemini API Reference:** https://ai.google.dev/docs
- **GitHub Repository:** https://github.com/google/gemini-cli
- **Google AI Studio:** https://makersuite.google.com
- **Gemini API Status:** https://status.cloud.google.com

### Community Resources

- **Discord:** Gemini CLI community
- **Stack Overflow:** Tag `gemini-cli`
- **Reddit:** r/gemini, r/googleai
- **GitHub Discussions:** https://github.com/google/gemini-cli/discussions

### Learning Path

**Week 1: Basics**
- Install and configure Gemini CLI
- Learn basic commands (ask, chat, generate)
- Practice simple queries
- Understand authentication

**Week 2: Intermediate**
- Master file operations
- Learn batch processing
- Practice code generation
- Use templates and configuration

**Week 3: Advanced**
- Advanced features (streaming, custom prompts)
- Integration with scripts
- CI/CD integration
- Performance optimization

**Week 4: Mastery**
- Complex workflows
- Automation projects
- Custom integrations
- Expert techniques

### Practice Projects

1. **Simple Automation:** Create script to generate code from specs
2. **Code Review Bot:** Automated code review system
3. **Documentation Generator:** Auto-generate API docs
4. **Test Generator:** Generate test suites
5. **Refactoring Tool:** Automated code refactoring

### Next Steps

1. **Master Basics:** Complete all basic commands
2. **Practice Daily:** Use Gemini CLI for daily tasks
3. **Build Projects:** Create automation workflows
4. **Share Knowledge:** Help team members learn
5. **Stay Updated:** Follow Gemini CLI updates

### Mastery Checklist

By completing this tutorial, you should be able to:

- [ ] Install and configure Gemini CLI on any platform
- [ ] Use all basic commands confidently
- [ ] Master file operations and batch processing
- [ ] Generate code from specifications
- [ ] Integrate Gemini CLI into workflows
- [ ] Automate tasks with scripts
- [ ] Optimize performance
- [ ] Troubleshoot common issues
- [ ] Build complete automation projects
- [ ] Achieve expert-level productivity

---

## Conclusion

Gemini CLI is a powerful tool that brings Google's Gemini AI capabilities directly to your command line. By mastering Gemini CLI, you can:

- **Automate Tasks:** Streamline repetitive coding tasks
- **Generate Code:** Create code from specifications quickly
- **Review Code:** Automated code analysis and review
- **Process Files:** Batch process and analyze files
- **Integrate Workflows:** Seamlessly integrate into development processes

### Key Takeaways

1. **Start Simple:** Master basics before advanced features
2. **Use Context:** Provide good context for better results
3. **Automate:** Integrate into scripts and workflows
4. **Optimize:** Use batch processing and parallel execution
5. **Practice:** Use Gemini CLI for daily development tasks

### Getting Help

- **Documentation:** https://developers.google.com/gemini-code-assist/docs/gemini-cli
- **Community:** GitHub Discussions, Discord, Stack Overflow
- **Support:** Check official support channels

**Start using Gemini CLI today and transform your development workflow!**

---

**Happy coding with Gemini CLI! 🚀**

*This tutorial covers Gemini CLI comprehensively. For the latest features and updates, visit the [official documentation](https://developers.google.com/gemini-code-assist/docs/gemini-cli).*

