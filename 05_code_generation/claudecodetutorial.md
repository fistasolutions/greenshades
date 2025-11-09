# Claude Code: Complete Tutorial and Mastery Guide

*Master Anthropic's AI-Powered Code Editor for World-Class Development*

**Access Claude Code:** https://claude.ai/code

---

## Table of Contents

1. [Introduction to Claude Code](#introduction-to-claude-code)
2. [Installation and Setup](#installation-and-setup)
3. [Getting Started with Claude Code](#getting-started-with-claude-code)
4. [Core Commands Reference](#core-commands-reference)
5. [Project Initialization and Memory Management](#project-initialization-and-memory-management)
6. [Core Features and Capabilities](#core-features-and-capabilities)
7. [MCP (Model Context Protocol) Integration](#mcp-model-context-protocol-integration)
8. [Claude Code Prompting Strategies](#claude-code-prompting-strategies)
9. [Advanced Features and Techniques](#advanced-features-and-techniques)
10. [Language-Specific Examples](#language-specific-examples)
11. [Advanced Workflows](#advanced-workflows)
12. [Real-World Projects](#real-world-projects)
13. [GitHub Integration and Hooks](#github-integration-and-hooks)
14. [Best Practices and Tips](#best-practices-and-tips)
15. [Real-World Case Studies](#real-world-case-studies)
16. [Troubleshooting Claude Code](#troubleshooting-claude-code)
17. [Resources and Next Steps](#resources-and-next-steps)

---

## Introduction to Claude Code

### What is Claude Code?

Claude Code is Anthropic's AI-powered code editor, specifically designed for software development with deep integration of Claude AI. Unlike traditional code editors that add AI as a feature, Claude Code is built from the ground up to leverage AI for every aspect of development.

### Why Claude Code?

**Key Advantages:**
- **Deep Code Understanding:** Claude's advanced reasoning understands complex codebases
- **Multi-File Context:** Seamlessly works across entire projects
- **Natural Language Interface:** Conversational development experience
- **Comprehensive Documentation:** Auto-generates excellent documentation
- **Code Review Excellence:** Superior code review and suggestions
- **Web-Based:** Access from anywhere, no installation needed

### Claude Code vs. Other Tools

| Aspect | Claude Code | GitHub Copilot | Cursor |
|--------|-------------|----------------|--------|
| **Primary Focus** | Deep understanding | Quick completions | Full editor |
| **Code Review** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Basic | ⭐⭐⭐ Good |
| **Documentation** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Basic | ⭐⭐⭐ Good |
| **Multi-File** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Limited | ⭐⭐⭐⭐ Strong |
| **Natural Language** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Basic | ⭐⭐⭐⭐ Advanced |
| **Interface** | Web-based | IDE extension | Standalone editor |

---

## Installation and Setup

### Prerequisites

Before installing Claude Code, ensure you have:

**Required:**
- **Node.js 18 or newer** - [Download Node.js](https://nodejs.org/en/download/)
- Basic familiarity with terminal/command line
- Basic git knowledge (`git add`, `commit`, `pull`, `push`)

**Helpful but Not Required:**
- Basic Python knowledge (for lessons 2-7)
- Next.js familiarity (for lesson 8)
- Understanding of basic terminal commands

### System Requirements

**macOS/Linux:**
- Node.js 18+ installed
- Terminal access
- Git installed

**Windows:**
You have two options:

**Option 1: Native Windows with Git Bash**
- Install [Git for Windows](https://git-scm.com/downloads/win)
- Use Git Bash for all commands
- In VS Code, select `Git Bash` as your terminal

**Option 2: WSL (Windows Subsystem for Linux)**
- Install [WSL 1 or 2](https://learn.microsoft.com/en-us/windows/wsl/install)
- Use WSL terminal for Claude Code

### Installation Steps

#### Step 1: Install Claude Code

Open your terminal and run:

```bash
npm install -g @anthropic-ai/claude-code
```

#### Step 2: Verify Installation

Check if Claude Code is installed correctly:

```bash
claude --version
```

#### Step 3: Troubleshooting Installation Issues

If you encounter permission errors or "command not found" errors:

**Linux/macOS Permission Issues:**
```bash
# Option 1: Use sudo (not recommended for global installs)
sudo npm install -g @anthropic-ai/claude-code

# Option 2: Fix npm permissions (recommended)
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
export PATH=~/.npm-global/bin:$PATH
# Add to ~/.bashrc or ~/.zshrc for persistence
npm install -g @anthropic-ai/claude-code
```

**Windows Issues:**
- Ensure Git Bash is selected in VS Code terminal
- Check that Node.js is in your PATH
- Restart terminal after installation

For detailed troubleshooting, see the [official troubleshooting guide](https://docs.anthropic.com/en/docs/claude-code/troubleshooting#linux-and-mac-installation-issues%3A-permission-or-command-not-found-errors).

### Launching Claude Code

#### Option 1: From Terminal

1. Navigate to your project directory:
   ```bash
   cd /path/to/your/project
   ```

2. Launch Claude Code:
   ```bash
   claude
   ```

#### Option 2: From VS Code Integrated Terminal

1. Open VS Code
2. Open integrated terminal (`` Ctrl+` `` or `Cmd+` `)
3. Navigate to your project
4. Type `claude`

**Note:** The VS Code extension will auto-install when you first run `claude` from the integrated terminal.

**If VS Code extension doesn't install automatically:**
- Ensure you're running from VS Code's integrated terminal
- Install the `code` command: Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows/Linux)
- Search for "Shell Command: Install 'code' command in PATH"
- Run the command
- Restart VS Code

For more information, see [Claude Code IDE Integrations](https://docs.anthropic.com/en/docs/claude-code/ide-integrations).

### Subscription and Cost

**Subscription Options:**
- **Pro ($20/month):** Sufficient for most lessons (doesn't include Opus model)
- **Max ($100/month):** Includes Opus and higher usage limits

**Pay-as-you-go:**
- API usage billing (if using Sonnet for all activities)
- Estimated cost: $12-$20 for all course lessons
- Monitor costs with `/cost` command during sessions

### Next Steps

Once installed, you're ready to:
1. Initialize your first project (see [Project Initialization](#project-initialization-and-memory-management))
2. Learn core commands (see [Core Commands Reference](#core-commands-reference))
3. Start building with Claude Code!

---

## Getting Started with Claude Code

### Step 1: Access Claude Code

1. **Visit:** https://claude.ai/code
2. **Sign In:** Use your Anthropic account (create one if needed)
3. **Navigate:** Click "Code" or "Code Editor" in the interface

### Step 2: Create Your First Project

**Option A: New Project**
```
1. Click "New Project"
2. Choose project type (Web App, API, Library, etc.)
3. Select programming language
4. Start coding!
```

**Option B: Import Existing Code**
```
1. Click "Import Project"
2. Connect GitHub/GitLab repository
3. Or upload code files directly
4. Claude Code analyzes your codebase
```

### Step 3: Your First Code Generation

**Try This Simple Example:**

```
Create a Python function that calculates the factorial of a number using recursion, 
with proper error handling for negative numbers and type validation.
```

**Claude Code will generate:**
```python
def factorial(n: int) -> int:
    """
    Calculate the factorial of a non-negative integer using recursion.
    
    Args:
        n: A non-negative integer
    
    Returns:
        The factorial of n (n!)
    
    Raises:
        ValueError: If n is negative
        TypeError: If n is not an integer
    
    Example:
        >>> factorial(5)
        120
        >>> factorial(0)
        1
    """
    if not isinstance(n, int):
        raise TypeError(f"Expected integer, got {type(n).__name__}")
    
    if n < 0:
        raise ValueError("Factorial is not defined for negative numbers")
    
    if n == 0 or n == 1:
        return 1
    
    return n * factorial(n - 1)
```

### Step 4: Explore Claude Code Features

- **Code Composer:** Multi-step code generation
- **Chat:** Ask questions about your code
- **Code Review:** Get automated code reviews
- **Documentation:** Auto-generate docs
- **Refactoring:** AI-powered code improvements

---

## Core Commands Reference

Claude Code provides powerful commands to manage your development workflow. Here's a comprehensive reference:

### Project Memory Commands

#### `/init` - Initialize Project Memory

Scans your codebase and creates a `CLAUDE.md` file that guides Claude through your project structure, architecture, and coding style.

**Usage:**
```bash
/init
```

**What it does:**
- Analyzes your codebase structure
- Identifies key files and patterns
- Creates `CLAUDE.md` in your project root
- Automatically includes `CLAUDE.md` in context for all future sessions

**Example `CLAUDE.md` content:**
```markdown
# Project Overview
This is a FastAPI application with...
- Backend: Python/FastAPI
- Database: PostgreSQL with SQLAlchemy
- Frontend: React with TypeScript

# Key Commands
- Use `uv` to run Python files or add dependencies
- Run tests with `pytest`
- Start server with `uvicorn app:app --reload`

# Architecture
- API routes in `routes/`
- Models in `models/`
- Database config in `database.py`
```

**Best Practice:** Run `/init` when starting a new project or when onboarding Claude Code to an existing codebase.

#### `#` - Quick Memory Addition

Add quick notes to `CLAUDE.md` without running full initialization.

**Usage:**
```
# Use uv to run python files or add dependencies
```

**When to use:**
- Adding project-specific context
- Documenting database schemas
- Noting coding conventions
- Recording important patterns

**Examples:**
```
# The vector database has two collections:
# - course_catalog: stores course titles for name resolution
# - course_content: stores text chunks for semantic search

# Always use async/await for database operations

# Follow PEP 8 style guide strictly
```

### Context Management Commands

#### `/clear` - Clear Conversation History

Clears the current conversation history while keeping project memory (`CLAUDE.md`).

**Usage:**
```bash
/clear
```

**When to use:**
- Starting a new task unrelated to current conversation
- Conversation getting too long
- Wanting a fresh start while keeping project context

#### `/compact` - Summarize Conversation

Summarizes the current conversation history to save tokens while preserving key context.

**Usage:**
```bash
/compact
```

**When to use:**
- Long conversation history
- Want to preserve context but reduce token usage
- Before starting a related but different task

#### `ESC` - Interrupt Claude

Interrupts Claude's current response to redirect or correct it.

**Usage:**
- Press `ESC` once: Interrupt current response
- Press `ESC` twice: Rewind conversation to an earlier point

**When to use:**
- Claude is going in wrong direction
- You want to clarify requirements
- You need to stop and provide more context

### File Referencing

#### `@` - Mention Files

Include file contents in your request by mentioning them with `@`.

**Usage:**
```
@filename.py Explain how this function works
```

**Examples:**
```
@backend/app.py Add error handling to the /api/query endpoint

@models.py @schemas.py Ensure these models match the database schema

@tests/test_api.py Review these tests and suggest improvements
```

**Best Practices:**
- Mention specific files for targeted requests
- Use multiple `@` mentions for cross-file operations
- Claude Code automatically includes file contents in context

### Bash Commands

#### `!` - Execute Bash Commands

Run terminal commands within Claude Code by prefixing with `!`.

**Usage:**
```
!pwd
!ls -la
!git status
!npm install
```

**Examples:**
```
!python -m pytest tests/
!git log --oneline -10
!docker ps
```

**Note:** Type `exit` to quit Claude Code and return to regular terminal.

### Cost Monitoring

#### `/cost` - Check Session Cost

Monitor API usage costs for the current session.

**Usage:**
```bash
/cost
```

**Output:**
```
Current session cost: $2.45
Tokens used: 45,230
Model: claude-sonnet-4
```

### Mode Switching

#### `Shift + Tab` - Toggle Planning Mode

Switch between planning mode and auto-accept mode.

**Planning Mode:**
- Claude shows you what it plans to do
- You review and approve before execution
- Better for complex changes

**Auto-Accept Mode:**
- Claude executes changes immediately
- Faster workflow for simple tasks
- Use when you trust Claude's judgment

**When to use Planning Mode:**
- Complex refactoring
- Multiple file changes
- Critical production code
- Learning Claude's approach

**When to use Auto-Accept Mode:**
- Simple fixes
- Documentation updates
- Test generation
- Quick iterations

### Screenshot Integration

#### Taking Screenshots

**macOS:**
- `Cmd + Shift + Ctrl + 4`: Take screenshot

**Windows:**
- `Win + Shift + S`: Take screenshot

#### Pasting Screenshots

**Usage:**
- `Ctrl + V` (may not work on Windows)
- Paste screenshot directly into Claude Code

**When to use:**
- Show UI issues
- Verify visual changes
- Debug layout problems
- Share design mockups

**Example:**
```
[Paste screenshot]
These links are hard to read. Make them more visually appealing.
```

---

## Project Initialization and Memory Management

### Understanding CLAUDE.md

`CLAUDE.md` is Claude Code's project memory file. It helps Claude understand your codebase structure, conventions, and important patterns.

### Creating CLAUDE.md

#### Method 1: Automatic Initialization

```bash
/init
```

This scans your entire codebase and generates a comprehensive `CLAUDE.md` file.

#### Method 2: Manual Creation

Create `CLAUDE.md` in your project root with:

```markdown
# Project Name

## Overview
Brief description of your project

## Tech Stack
- Language: Python 3.11+
- Framework: FastAPI
- Database: PostgreSQL

## Key Commands
- Run: `uvicorn app:app --reload`
- Test: `pytest`
- Format: `black .`

## Architecture
- API routes: `routes/`
- Models: `models/`
- Utils: `utils/`

## Coding Conventions
- Use type hints everywhere
- Follow PEP 8
- Async/await for I/O operations
```

### Maintaining Project Memory

#### Adding Context with `#`

Quickly add information to `CLAUDE.md`:

```
# Database Schema:
# - users table: id, email, name, created_at
# - posts table: id, user_id, title, content, published_at

# Always use transactions for multi-step database operations

# API endpoints require JWT authentication except /auth/login and /auth/register
```

#### Updating CLAUDE.md

Claude Code can update `CLAUDE.md` automatically when you:
- Add new patterns
- Change architecture
- Update conventions

**Example:**
```
Update CLAUDE.md to reflect that we're now using Redis for caching
```

### Codebase Exploration Prompts

Once initialized, use these prompts to understand your codebase:

#### Get Overview
```
Give me an overview of this codebase
```

#### Understand Data Models
```
What are the key data models in this project?
```

#### Trace Functionality
```
Trace the process of handling user's query from frontend to backend
```

#### Understand Architecture
```
Explain how the documents are processed in this system
```

#### Get API Documentation
```
Describe the API endpoints in this application
```

#### Understand Configuration
```
What is the format of the document expected by the document_processor?
```

#### Visualize Flow
```
Draw a diagram that illustrates the query flow
```

#### Understand Implementation Details
```
Explain how the text is transformed into chunks? What is the size of each chunk?
```

### Best Practices for Project Memory

1. **Keep it Updated:** Update `CLAUDE.md` when architecture changes
2. **Be Specific:** Include concrete examples and patterns
3. **Document Conventions:** Note coding style, naming conventions
4. **Include Commands:** Document common commands and workflows
5. **Reference External Docs:** Link to important documentation

---

## Core Features and Capabilities

### 1. Code Composer

**What It Does:**
Code Composer allows you to build complex code through multi-step conversations, refining and iterating on your requirements.

**How to Use:**
1. Open Code Composer (Cmd/Ctrl + K)
2. Describe what you want to build
3. Claude Code generates initial code
4. Refine and iterate based on results
5. Finalize when satisfied

**Example Workflow:**
```
Step 1: "Create a user authentication system"

Claude Code generates: Basic auth structure

Step 2: "Add JWT token support with refresh tokens"

Claude Code adds: JWT implementation

Step 3: "Add rate limiting and security headers"

Claude Code adds: Security features

Step 4: "Generate comprehensive tests"

Claude Code generates: Full test suite
```

### 2. Natural Language Chat

**What It Does:**
Have conversations with Claude about your code, ask questions, get explanations, and request modifications.

**Example Conversations:**

**Q: "Explain how this sorting algorithm works"**
```
Claude Code provides:
- Step-by-step algorithm explanation
- Time and space complexity analysis
- Visual representation of the process
- Comparison with other sorting algorithms
```

**Q: "How can I optimize this function for better performance?"**
```
Claude Code provides:
- Performance analysis
- Specific optimization suggestions
- Before/after code comparison
- Benchmarking recommendations
```

**Q: "Add error handling to this function"**
```
Claude Code:
- Identifies potential error points
- Adds comprehensive error handling
- Includes proper exception types
- Adds logging and error messages
```

### 3. Code Review Mode

**What It Does:**
Automated code review that checks for:
- Security vulnerabilities
- Performance issues
- Code quality and maintainability
- Best practices compliance
- Potential bugs

**How to Use:**
1. Select code to review
2. Open Code Review (Cmd/Ctrl + Shift + R)
3. Claude Code analyzes and provides feedback
4. Review suggestions and apply improvements

**Example Review Output:**
```
Code Review Results:

✅ Strengths:
- Clean, readable code
- Good function naming
- Proper type hints

⚠️ Issues Found:
1. Security: SQL injection risk in line 45
   - Suggestion: Use parameterized queries
   
2. Performance: N+1 query problem in line 78
   - Suggestion: Use eager loading
   
3. Code Quality: Magic numbers in line 23
   - Suggestion: Extract to constants

🔧 Improvements:
- Add input validation
- Add comprehensive error handling
- Improve documentation
```

### 4. Documentation Generator

**What It Does:**
Auto-generates comprehensive documentation including:
- Function/class docstrings
- API documentation
- README files
- Code examples
- Usage guides

**Example:**
```
Generate documentation for this API including:
- Endpoint descriptions
- Request/response schemas
- Authentication requirements
- Error codes
- Usage examples in Python, JavaScript, and cURL
```

**Claude Code generates:**
- Complete API documentation
- OpenAPI/Swagger spec
- Code examples in multiple languages
- Error handling guide

### 5. Multi-File Code Generation

**What It Does:**
Understands relationships across multiple files and generates connected code.

**Example:**
```
Create a complete REST API with these files:
- models.py: User and Product models
- schemas.py: Pydantic validation schemas
- routes.py: FastAPI endpoints
- database.py: Database connection
- main.py: Application setup
- requirements.txt: Dependencies
- README.md: Documentation

Ensure all files are properly connected.
```

**Claude Code generates all files with:**
- Proper imports and relationships
- Consistent code style
- Complete functionality
- Documentation

---

## Claude Code Prompting Strategies

### Strategy 1: Be Specific and Contextual

**❌ Bad:**
```
Create a function to process data
```

**✅ Good:**
```
Create a Python function that:
- Takes a list of dictionaries with 'name', 'email', 'age' keys
- Validates email format using regex
- Filters users aged 18-65
- Sorts by age in ascending order
- Returns list of valid user dictionaries
- Includes comprehensive error handling
- Has type hints and docstring
- Logs validation failures
```

### Strategy 2: Provide Examples

**Example:**
```
Create a function similar to this one but for products instead of users:

def create_user(name: str, email: str, age: int) -> dict:
    """Creates a user with validation"""
    if not name or len(name) < 2:
        raise ValueError("Name must be at least 2 characters")
    if not email or '@' not in email:
        raise ValueError("Invalid email format")
    if age < 0 or age > 150:
        raise ValueError("Age must be between 0 and 150")
    
    return {
        'id': generate_id(),
        'name': name,
        'email': email,
        'age': age,
        'created_at': datetime.now()
    }

Now create create_product function with similar validation for:
- name (string, required, min 3 chars)
- price (float, required, must be positive)
- category (string, must be from predefined list)
- stock (int, must be non-negative)
```

### Strategy 3: Use Iterative Refinement

**Step 1: Basic Functionality**
```
Create a function to calculate total price of items in a shopping cart
```

**Step 2: Add Features**
```
Add discount calculation (10% if total > $100, 20% if total > $500)
```

**Step 3: Add Error Handling**
```
Add validation for negative prices, invalid quantities, and missing items
```

**Step 4: Add Documentation**
```
Add comprehensive docstring with examples and edge cases
```

### Strategy 4: Specify Framework and Libraries

**Example:**
```
Create a FastAPI endpoint using:
- Pydantic for request/response validation
- SQLAlchemy for database operations
- JWT for authentication
- Python-dotenv for configuration

The endpoint should:
- Accept POST requests to /api/users
- Validate user data (name, email, password)
- Hash password with bcrypt
- Save to PostgreSQL database
- Return user ID and JWT token
- Handle duplicate email errors
- Include rate limiting
```

### Strategy 5: Request Code Review

**Example:**
```
Review this code for:
- Security vulnerabilities
- Performance bottlenecks
- Code quality issues
- Best practices compliance
- Potential bugs

Then refactor to address all issues found.
```

---

## Language-Specific Examples

### Python Examples

#### Example 1: Data Processing Class

**Prompt:**
```
Create a Python class for processing CSV data with:
- Read CSV files with error handling
- Validate data types and required fields
- Clean data (remove duplicates, handle missing values)
- Transform data (normalize, encode categorical)
- Export to multiple formats (CSV, JSON, Parquet)
- Comprehensive logging
- Type hints throughout
- Follow PEP 8 style
```

**Claude Code generates complete class with all methods.**

#### Example 2: FastAPI REST API

**Prompt:**
```
Create a FastAPI REST API for a blog system with:

Endpoints:
- GET /posts - List all posts with pagination
- GET /posts/{id} - Get single post
- POST /posts - Create new post (authenticated)
- PUT /posts/{id} - Update post (author only)
- DELETE /posts/{id} - Delete post (author only)

Features:
- SQLAlchemy models (Post, User, Comment)
- Pydantic schemas for validation
- JWT authentication
- Role-based access control
- Input validation and error handling
- API documentation with Swagger
- Database migrations with Alembic
```

**Claude Code generates complete API with all files.**

### JavaScript/TypeScript Examples

#### Example 1: React Component

**Prompt:**
```
Create a TypeScript React component for a user dashboard with:
- User profile display (avatar, name, email)
- Statistics cards (total posts, followers, following)
- Recent activity feed
- Settings panel (collapsible)
- Responsive design with Tailwind CSS
- Loading and error states
- Accessibility (ARIA labels, keyboard nav)
- State management with React hooks
- API integration with fetch/axios
```

**Claude Code generates complete component.**

#### Example 2: Node.js API

**Prompt:**
```
Create an Express.js API with TypeScript for a task management system:

Features:
- REST API with CRUD operations
- MongoDB with Mongoose
- JWT authentication
- Input validation with Joi
- Error handling middleware
- Rate limiting
- CORS configuration
- API documentation
- Environment variables
- Logging with Winston
```

**Claude Code generates complete API structure.**

### Java Examples

#### Example 1: Spring Boot Application

**Prompt:**
```
Create a Spring Boot REST API for an e-commerce system with:
- Product CRUD operations
- User authentication with Spring Security
- JPA entities and repositories
- DTOs for request/response
- Exception handling with @ControllerAdvice
- Validation with Bean Validation
- Swagger documentation
- Database with H2 (development) and PostgreSQL (production)
- Unit and integration tests
```

**Claude Code generates complete Spring Boot application.**

---

## MCP (Model Context Protocol) Integration

MCP (Model Context Protocol) allows Claude Code to connect to external tools and services, dramatically expanding its capabilities. MCP servers provide specialized tools that Claude can use during development.

### Understanding MCP

MCP servers expose tools that Claude Code can use, such as:
- Browser automation (Playwright)
- Design tool integration (Figma)
- Database access
- API integrations
- File system operations

### Managing MCP Servers

#### `/mcp` - Manage MCP Connections

View and manage connected MCP servers.

**Usage:**
```bash
/mcp
```

**What it shows:**
- List of connected MCP servers
- Available tools from each server
- Server status and configuration

### Setting Up MCP Servers

#### Playwright MCP Server

Browser automation for testing and visual verification.

**Installation:**
```bash
# Exit Claude Code first
claude mcp add playwright npx @playwright/mcp@latest
```

**Usage:**
After setup, Claude Code can:
- Take screenshots of web pages
- Navigate websites
- Verify UI changes
- Test user interactions

**Example Prompt:**
```
Using the playwright MCP server, visit 127.0.0.1:8000 and view the '+ New Chat' button. I want that button to look the same as the other links below for Courses and Try Asking. Make sure this is left aligned and that the border is removed.
```

**Permissions:**
- Claude Code will ask permission to use screenshot tools
- You can always allow or configure manually:
  - Type `/permissions`
  - Add rule: Allow `mcp__playwright__browser_take_screenshot`

#### Figma Dev Mode MCP Server

Import designs directly from Figma into Claude Code.

**Prerequisites:**
- Figma Dev or Full seat (Professional, Organization, or Enterprise plans)
- [Figma Desktop App](https://www.figma.com/downloads/) installed

**Setup Steps:**

1. **Enable MCP Server in Figma:**
   - Open your Figma design file
   - Click Figma menu (upper-left)
   - Preferences → Enable Dev Mode MCP Server
   - Server runs at `http://127.0.0.1:3845/mcp`

2. **Configure for Claude Code:**
   ```bash
   claude mcp add --transport http figma-dev-mode-mcp-server http://127.0.0.1:3845/mcp
   ```

3. **Also add Playwright for verification:**
   ```bash
   claude mcp add playwright npx @playwright/mcp@latest
   ```

4. **Verify Connection:**
   ```bash
   /mcp
   ```
   Should show both Figma and Playwright servers.

**Usage Example:**
```
Using the following figma mockup [paste link] use the figma dev MCP server to analyze the mockup and build the underlying code in this next.js application. Use the recharts library for creating charts to make this a web application. Check how this application looks using the playwright MCP server and verify it looks as close to the mock as possible.
```

**Copying Figma Design:**
- In Figma Desktop: Select design → `Ctrl+L` (Windows) or `Cmd+L` (Mac)
- Paste the link in Claude Code

#### Alternative: Framelink Figma MCP Server

Free alternative to official Figma MCP server.

**Setup:**
1. Get API key from [Framelink](https://www.framelink.ai/)
2. Configure:
   ```bash
   claude mcp add "Framelink Figma MCP" -- npx -y figma-developer-mcp --figma-api-key=YOUR-KEY --stdio
   ```

**Best Practices:**
- See [Framelink Quickstart Guide](https://www.framelink.ai/docs/quickstart)
- Check [Best Practices](https://www.framelink.ai/docs/best-practices)

### MCP Server Best Practices

1. **Verify Connections:** Always check `/mcp` after adding servers
2. **Set Permissions:** Configure tool permissions for security
3. **Test Tools:** Verify tools work before complex workflows
4. **Document Usage:** Note which MCP servers your project uses

### Common MCP Workflows

#### Visual Verification Workflow
```
1. Make code changes
2. Use Playwright to take screenshot
3. Compare with design mockup
4. Iterate until match
```

#### Design-to-Code Workflow
```
1. Import Figma design via MCP
2. Claude analyzes design structure
3. Generate code matching design
4. Verify with Playwright screenshots
```

---

## Advanced Features and Techniques

### Extended Thinking Mode

For complex tasks requiring deep reasoning, use extended thinking mode.

**Levels of Thinking:**
- `think` - Basic extended thinking
- `think hard` - More reasoning budget
- `think harder` - Even more reasoning
- `ultrathink` - Maximum reasoning budget

**Usage:**
```
The RAG chatbot returns 'query failed' for any content-related questions. I need you to:
1. Write tests to evaluate the outputs of the execute method
2. Write tests to evaluate if ai_generator correctly calls for the CourseSearchTool
3. Write tests to evaluate how the RAG system handles content-query related questions

Save the tests in a tests folder. Run those tests against the current system to identify which components are failing. Propose fixes based on what the tests reveal is broken.

Think.
```

**When to use:**
- Complex architectural changes
- Debugging complicated issues
- Multi-step problem solving
- Strategic planning

### Subagents

Claude Code can use subagents to handle complex, multi-step tasks in parallel.

#### Built-in Subagents

**Task Subagent:**
Claude Code automatically uses subagents for complex tasks. You can explicitly request them:

```
Use two parallel subagents to brainstorm possible plans for refactoring this codebase. Do not implement any code.
```

**When to use:**
- Brainstorming multiple approaches
- Investigating different aspects
- Parallel problem exploration
- Complex multi-step tasks

#### Custom Subagents

Create specialized subagents with custom system prompts and tools.

**Setup:**
1. Define subagent in `.claude/subagents/` folder
2. Specify system prompt
3. Assign specific tools
4. Use in workflows

**Example Use Case:**
- Frontend subagent: Specialized in React/UI
- Backend subagent: Specialized in API/database
- Testing subagent: Specialized in test generation

**Note:** Custom subagents are advanced feature. See [Subagents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents) for details.

### Custom Slash Commands

Create your own commands for repetitive tasks.

#### Creating Custom Commands

1. **Create commands folder:**
   ```bash
   mkdir -p .claude/commands
   ```

2. **Create command file:**
   Create `.claude/commands/implement-feature.md`:
   ```markdown
   You will be implementing a new feature in this codebase

   $ARGUMENTS

   IMPORTANT: Only do this for front-end features.
   Once this feature is built, make sure to write the changes you made to file called frontend-changes.md
   Do not ask for permissions to modify this file, assume you can always do it.
   ```

3. **Use the command:**
   ```bash
   /implement-feature Add a dark mode toggle button
   ```

**Best Practices:**
- Use `$ARGUMENTS` placeholder for user input
- Be specific about what the command does
- Include any constraints or requirements
- Document command purpose in comments

### Git Worktrees for Parallel Development

Worktrees allow you to work on multiple features simultaneously in separate directories.

#### Workflow

1. **Commit current changes:**
   ```bash
   git add .
   git commit -m "Current work"
   ```

2. **Create worktrees folder:**
   ```bash
   mkdir .trees
   ```

3. **Create worktrees for each feature:**
   ```bash
   git worktree add .trees/ui_feature
   git worktree add .trees/testing_feature
   git worktree add .trees/quality_feature
   ```

4. **Work in each worktree:**
   - Open terminal in each worktree directory
   - Launch Claude Code: `claude`
   - Implement feature independently

5. **Commit in each worktree:**
   ```bash
   cd .trees/ui_feature
   git add .
   git commit -m "Add UI feature"
   ```

6. **Merge all worktrees:**
   ```bash
   # In main directory
   claude
   ```
   ```
   Use the git merge command to merge in all the worktrees of the .trees folder into main and fix any conflicts if there are any
   ```

**Benefits:**
- Parallel feature development
- Isolated changes
- Easy merging
- No branch switching

### Testing and Debugging Workflows

#### Creating Test Frameworks

**Prompt:**
```
The RAG chatbot returns 'query failed' for any content-related questions. I need you to:
1. Write tests to evaluate the outputs of the execute method of the CourseSearchTool in @backend/search_tools.py
2. Write tests to evaluate if @backend/ai_generator.py correctly calls for the CourseSearchTool
3. Write tests to evaluate how the RAG system is handling the content-query related questions.

Save the tests in a tests folder within @backend. Run those tests against the current system to identify which components are failing. Propose fixes based on what the tests reveal is broken.

Think.
```

#### Code Refactoring with Tests

**Prompt:**
```
Refactor @backend/ai_generator.py to support sequential tool calling where Claude can make up to 2 tool calls in separate API rounds.

Current behavior:
- Claude makes 1 tool call → tools are removed from API params → final response
- If Claude wants another tool call after seeing results, it can't (gets empty response)

Desired behavior:
- Each tool call should be a separate API request where Claude can reason about previous results
- Support for complex queries requiring multiple searches for comparisons, multi-part questions, or when information from different courses/lessons is needed

Example flow:
1. User: "Search for a course that discusses the same topic as lesson 4 of course X"
2. Claude: get course outline for course X → gets title of lesson 4
3. Claude: uses the title to search for a course that discusses the same topic → returns course information
4. Claude: provides complete answer

Requirements:
- Maximum 2 sequential rounds per user query
- Terminate when: (a) 2 rounds completed, (b) Claude's response has no tool_use blocks, or (c) tool call fails
- Preserve conversation context between rounds
- Handle tool execution errors gracefully

Notes:
- Update the system prompt in @backend/ai_generator.py
- Update the test @backend/tests/test_ai_generator.py
- Write tests that verify the external behavior (API calls made, tools executed, results returned) rather than internal state details.

Use two parallel subagents to brainstorm possible plans. Do not implement any code.
```

### Feature Implementation Examples

#### Example 1: Embedding Links in Source Citations

**Context:** Chatbot returns lesson sources. Need to make sources clickable links.

**Prompt (with plan mode):**
```
The chat interface displays query responses with source citations. I need to modify it so each source becomes a clickable link that opens the corresponding lesson video in a new tab:
- When courses are processed into chunks in @backend/document_processor.py, the link of each lesson is stored in the course_catalog collection
- Modify _format_results in @backend/search_tools.py so that the lesson links are also returned
- The links should be embedded invisibly (no visible URL text)
```

**Follow-up:**
```
[Ctrl + V to paste screenshot] these links are hard to read. Make them more visually appealing.
```

#### Example 2: Adding Tools to Chatbot

**Context:** Need to add a course outline tool alongside existing content search tool.

**Prompt:**
```
In @backend/search_tools.py, add a second tool alongside the existing content-related tool. This new tool should handle course outline queries.
- Functionality:
   - Input: Course title
   - Output: Course title, course link, and complete lesson list
   - For each lesson: lesson number, lesson title
- Data source: Course metadata collection of the vector store
- Update the system prompt in @backend/ai_generator so that the course title, course link, the number and title of each lesson are all returned to address an outline-related queries.
- Make sure that the new tool is registered in the system.
```

#### Example 3: UI Feature with Visual Verification

**Context:** Add dark/light theme toggle button.

**Prompt:**
```
Add a toggle button that allows users to switch between dark and light themes.

1. Toggle Button Design
    - Create a toggle button that fits the existing design aesthetic
    - Position it in the top-right
    - Use an icon-based design (sun/moon icons or similar)
    - Smooth transition animation when toggling
    - Button should be accessible and keyboard-navigable

2. Light Theme CSS Variables
    Add a light theme variant with appropriate colors:
    - Light background colors
    - Dark text for good contrast
    - Adjusted primary and secondary colors
    - Proper border and surface colors
    - Maintain good accessibility standards

3. JavaScript Functionality
    - Toggle between themes on button click
    - Smooth transitions between themes

4. Implementation Details
    - Use CSS custom properties (CSS variables) for theme switching
    - Add a `data-theme` attribute to the body or html element
    - Ensure all existing elements work well in both themes
    - Maintain the current visual hierarchy and design language
```

**Verification with Playwright:**
```
Using the playwright MCP server, visit 127.0.0.1:8000 and verify the theme toggle works correctly. Test both light and dark themes.
```

#### Example 4: Testing Framework Enhancement

**Prompt:**
```
Enhance the existing testing framework for the RAG system in @backend/tests. The current tests cover unit components but are missing essential API testing infrastructure:

- API endpoint tests - Test the FastAPI endpoints (/api/query, /api/courses, /) for proper request/response handling
- pytest configuration - Add pytest.ini_options in pyproject.toml for cleaner test execution
- Test fixtures - Create conftest.py with shared fixtures for mocking and test data setup

The FastAPI app in backend/app.py mounts static files that don't exist in the test environment. Either create a separate test app or define the API endpoints inline in the test file to avoid import issues.
```

#### Example 5: Code Quality Tools

**Prompt:**
```
Add essential code quality tools to the development workflow. Set up black for automatic code formatting. Add proper formatting consistency throughout the codebase and create development scripts for running quality checks.
```

---

## Advanced Workflows

### Workflow 1: Building a Complete Feature

**Step 1: Describe the Feature**
```
Add user profile editing functionality to our app:
- Profile update endpoint
- Avatar upload with image validation
- Email change with verification
- Password change with current password check
- Profile visibility settings
```

**Step 2: Generate Implementation**
Claude Code generates all necessary code files.

**Step 3: Code Review**
```
Review the generated code for:
- Security best practices
- Performance optimization
- Error handling completeness
- Code quality
```

**Step 4: Generate Tests**
```
Generate comprehensive tests covering:
- Happy path scenarios
- Edge cases
- Error conditions
- Security tests
- Integration tests
```

**Step 5: Generate Documentation**
```
Create API documentation with:
- Endpoint descriptions
- Request/response examples
- Authentication requirements
- Error codes
```

### Workflow 2: Refactoring Legacy Code

**Step 1: Analyze Current Code**
```
Analyze this legacy code and identify:
- Code smells
- Performance issues
- Security vulnerabilities
- Areas for improvement
```

**Step 2: Create Refactoring Plan**
```
Create a refactoring plan that:
- Maintains functionality
- Improves code quality
- Enhances performance
- Adds proper error handling
- Improves testability
```

**Step 3: Execute Refactoring**
```
Refactor this code to:
- Use modern language features
- Apply design patterns
- Improve structure
- Add type hints
- Enhance documentation
```

**Step 4: Verify Changes**
```
Generate tests to verify refactored code:
- Unit tests for all functions
- Integration tests
- Performance benchmarks
- Regression tests
```

### Workflow 3: Debugging with Claude Code

**Step 1: Describe the Problem**
```
This function is returning incorrect results:
- Returns wrong values for edge cases
- Fails with certain input types
- Has performance issues with large datasets

Function code: [paste code]
```

**Step 2: Get Analysis**
Claude Code analyzes and identifies issues.

**Step 3: Generate Fix**
```
Fix all identified issues and:
- Add proper error handling
- Improve performance
- Add input validation
- Include regression tests
```

**Step 4: Verify Solution**
```
Generate comprehensive tests to ensure:
- All bugs are fixed
- No regressions introduced
- Performance is improved
- Edge cases are handled
```

---

## Best Practices and Tips

### ✅ Best Practices

#### 1. **Start with Clear Requirements**
- Be specific about what you want
- Include all necessary details
- Specify frameworks and libraries
- Define expected behavior

#### 2. **Use Iterative Development**
- Start with basic functionality
- Add features incrementally
- Refine based on results
- Test at each step

#### 3. **Leverage Code Review**
- Always review generated code
- Request security reviews
- Check for performance issues
- Ensure best practices

#### 4. **Request Documentation**
- Always ask for code documentation
- Request usage examples
- Get explanations for complex code
- Generate API documentation

#### 5. **Test Everything**
- Request test generation
- Cover all scenarios
- Include edge cases
- Add integration tests

### ❌ Common Mistakes

#### 1. **Being Too Vague**
❌ "Create a function"
✅ "Create a Python function that validates email addresses using regex, handles international domains, and returns (is_valid: bool, suggestions: list)"

#### 2. **Ignoring Error Handling**
❌ "Create a login function"
✅ "Create a secure login function with input validation, password hashing verification, rate limiting, and comprehensive error handling"

#### 3. **Skipping Documentation**
❌ Generate code without docs
✅ Always request documentation and examples

#### 4. **Not Reviewing Code**
❌ Accept first generated code
✅ Review, refine, and iterate

---

## Real-World Case Studies

### Case Study 1: Building a REST API from Scratch

**Scenario:** Need to build a complete REST API for a task management system.

**Claude Code Prompt:**
```
Create a complete REST API for task management:

Backend Stack:
- Node.js + Express + TypeScript
- PostgreSQL with Prisma ORM
- JWT authentication
- Input validation with Zod

Features:
- User registration and login
- CRUD operations for tasks
- Task assignment to users
- Task status tracking (todo, in-progress, done)
- Due date management
- Task filtering and search
- User profiles

Requirements:
- RESTful API design
- Proper error handling
- Rate limiting
- API documentation
- Database migrations
- Environment configuration
```

**Claude Code Generated:**
- Complete project structure
- All API endpoints
- Database schema and migrations
- Authentication middleware
- Validation schemas
- Error handling
- API documentation
- Configuration files

**Result:** Complete, production-ready API in minutes.

### Case Study 2: Refactoring Legacy Python Code

**Scenario:** Legacy code needs modernization and improvement.

**Before (Legacy Code):**
```python
def process_users(users):
    result = []
    for u in users:
        if u['age'] > 18:
            if u['email'].find('@') > 0:
                result.append(u)
    return result
```

**Claude Code Prompt:**
```
Refactor this function to:
- Use modern Python 3.10+ features
- Add type hints
- Improve error handling
- Add validation
- Follow PEP 8
- Add comprehensive documentation
- Include unit tests
```

**After (Refactored Code):**
```python
from typing import List, Dict, Any
import re

def process_users(users: List[Dict[str, Any]]) -> List[Dict[str, Any]]:
    """
    Process a list of users, filtering for adults with valid email addresses.
    
    Args:
        users: List of user dictionaries with 'age' and 'email' keys
    
    Returns:
        List of valid adult users with proper email addresses
    
    Raises:
        TypeError: If users is not a list
        KeyError: If required keys are missing
    
    Example:
        >>> users = [
        ...     {'age': 25, 'email': 'user@example.com'},
        ...     {'age': 17, 'email': 'minor@example.com'},
        ...     {'age': 30, 'email': 'invalid-email'}
        ... ]
        >>> process_users(users)
        [{'age': 25, 'email': 'user@example.com'}]
    """
    if not isinstance(users, list):
        raise TypeError("users must be a list")
    
    EMAIL_PATTERN = re.compile(r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$')
    ADULT_AGE = 18
    
    result = []
    for user in users:
        if not isinstance(user, dict):
            continue
        
        try:
            age = user['age']
            email = user['email']
        except KeyError as e:
            raise KeyError(f"Missing required key: {e}")
        
        if not isinstance(age, int) or age < 0:
            continue
        
        if not isinstance(email, str) or not EMAIL_PATTERN.match(email):
            continue
        
        if age >= ADULT_AGE:
            result.append(user)
    
    return result
```

**Result:** Modern, maintainable, well-documented code.

### Case Study 3: Generating Complete Test Suite

**Scenario:** Need comprehensive tests for existing code.

**Claude Code Prompt:**
```
Generate comprehensive unit tests for this function using pytest:

Function: [paste function code]

Requirements:
- Test happy path scenarios
- Test edge cases (empty inputs, None values, boundary conditions)
- Test error cases (invalid inputs, exceptions)
- Test performance with large datasets
- Use fixtures and parametrize where appropriate
- Achieve 100% code coverage
- Include integration tests
```

**Claude Code Generated:**
- Complete test suite
- All test cases
- Fixtures and helpers
- Performance tests
- Integration tests
- Coverage report setup

**Result:** Comprehensive test coverage in minutes.

---

## Troubleshooting Claude Code

### Problem 1: Generated Code Doesn't Match Requirements

**Symptoms:**
- Code doesn't do what you asked
- Missing features
- Wrong implementation

**Solutions:**
1. Be more specific in your prompt
2. Break down into smaller requests
3. Provide examples of desired output
4. Use iterative refinement
5. Request clarification from Claude

**Example Fix:**
```
Before: "Create a login function"

After: "Create a secure login function that:
- Accepts email and password
- Validates email format
- Hashes password with bcrypt
- Queries database for user
- Compares hashed passwords
- Returns JWT token on success
- Implements rate limiting (5 attempts per 15 minutes)
- Logs failed attempts
- Returns appropriate error messages"
```

### Problem 2: Code Has Security Vulnerabilities

**Symptoms:**
- SQL injection risks
- XSS vulnerabilities
- Missing authentication
- Insecure data handling

**Solutions:**
1. Always request security review
2. Specify security requirements upfront
3. Use Code Review mode
4. Request security best practices
5. Test for vulnerabilities

**Example:**
```
Generate this code with security best practices:
- Input validation and sanitization
- Parameterized queries (no SQL injection)
- CSRF protection
- XSS prevention
- Secure password handling
- Rate limiting
- Security headers
```

### Problem 3: Code Performance Issues

**Symptoms:**
- Slow execution
- High memory usage
- Doesn't scale

**Solutions:**
1. Specify performance requirements
2. Request optimization
3. Use Code Review for performance analysis
4. Request benchmarking
5. Ask for algorithmic improvements

**Example:**
```
Optimize this code for:
- O(n log n) time complexity
- O(1) space complexity where possible
- Handle datasets with 1M+ records
- Minimize memory footprint
- Include performance benchmarks
```

### Problem 4: Missing Documentation

**Symptoms:**
- No docstrings
- Unclear code purpose
- Missing examples

**Solutions:**
1. Always request documentation
2. Specify documentation requirements
3. Request usage examples
4. Ask for API documentation
5. Generate README files

**Example:**
```
Generate this code with:
- Comprehensive docstrings (Google style)
- Type hints throughout
- Usage examples in docstrings
- README with setup instructions
- API documentation
- Code comments for complex logic
```

---

## Real-World Projects

This section covers three complete projects that demonstrate Claude Code's capabilities across different domains.

### Project 1: RAG Chatbot Application

A complete Retrieval-Augmented Generation (RAG) system for querying course materials using semantic search.

#### Project Overview

**Tech Stack:**
- Backend: Python/FastAPI
- Vector Database: ChromaDB
- AI: Anthropic Claude Sonnet 4
- Frontend: HTML/CSS/JavaScript
- Embeddings: sentence-transformers

**Key Features:**
- Semantic search across course materials
- AI-powered responses with source citations
- Session-based conversation history
- Course analytics and statistics
- Automatic document processing

#### Getting Started

1. **Fork the Repository:**
   ```bash
   # Starting codebase
   git clone https://github.com/https-deeplearning-ai/starting-ragchatbot-codebase.git
   
   # Final state (after lessons)
   git clone https://github.com/https-deeplearning-ai/ragchatbot-codebase.git
   ```

2. **Setup:**
   ```bash
   cd starting-ragchatbot-codebase
   # Follow README.md instructions
   # Create .env with ANTHROPIC_API_KEY
   ```

3. **Run Application:**
   ```bash
   chmod +x run.sh
   ./run.sh
   # Or manually:
   cd backend
   uv run uvicorn app:app --reload --port 8000
   ```

#### Key Learning Points

**Lesson 2: Codebase Understanding**
- Use `/init` to understand project structure
- Explore with prompts like "Give me an overview of this codebase"
- Understand data models, API endpoints, and processing flows

**Lesson 3: Adding Features**
- Embed links in source citations
- Add '+ New Chat' functionality
- Add custom tools to the chatbot

**Lesson 4: Testing & Refactoring**
- Create comprehensive test frameworks
- Debug with extended thinking mode
- Refactor for sequential tool calling

**Lesson 5: Multiple Features**
- Use git worktrees for parallel development
- Create custom slash commands
- Implement UI, testing, and quality features simultaneously

**Example Feature Implementation:**
```
Add a '+ NEW CHAT' button to the left sidebar above the courses section. When clicked, it should:
- Clear the current conversation in the chat window
- Start a new session without page reload
- Handle proper cleanup on both @frontend and @backend
- Match the styling of existing sections (Courses, Try asking) - same font size, color, and uppercase formatting
```

### Project 2: E-Commerce Data Analysis & Dashboard

Refactoring Jupyter notebooks and creating interactive Streamlit dashboards.

#### Project Overview

**Tech Stack:**
- Data Analysis: Python/Pandas
- Visualization: Plotly
- Dashboard: Streamlit
- Data: E-commerce sales data

#### Getting Started

1. **Get Project Files:**
   ```bash
   git clone https://github.com/https-deeplearning-ai/sc-claude-code-files.git
   cd sc-claude-code-files/lesson7_files
   ```

2. **Files Included:**
   - Starting notebook: `EDA.ipynb`
   - Refactored notebook: `EDA_Refactored.ipynb`
   - Dashboard: `dashboard.py`
   - Data folder with e-commerce data

#### Notebook Refactoring Workflow

**Prompt:**
```
The @EDA.ipynb contains exploratory data analysis on e-commerce data in @ecommerce_data, focusing on sales metrics for 2023. Keep the same analysis and graphs, and improve the structure and documentation of the notebook.

Review the existing notebook and identify:
- What business metrics are currently calculated
- What visualizations are created
- What data transformations are performed
- Any code quality issues or inefficiencies

**Refactoring Requirements**

1. Notebook Structure & Documentation
   - Add proper documentation and markdown cells with clear header and a brief explanation for the section
   - Organize into logical sections:
       - Introduction & Business Objectives
       - Data Loading & Configuration
       - Data Preparation & Transformation
       - Business Metrics Calculation (revenue, product, geographic, customer experience analysis)
       - Summary of observations
   - Add table of contents at the beginning
   - Include data dictionary explaining key columns and business terms

2. Code Quality Improvements
   - Create reusable functions with docstrings
   - Implement consistent naming and formatting
   - Create separate Python files:
       - business_metrics.py containing business metric calculations only
       - data_loader.py loading, processing and cleaning the data

3. Enhanced Visualizations
   - Improve all plots with:
       - Clear and descriptive titles
       - Proper axis labels with units
       - Legends where needed
       - Appropriate chart types for the data
       - Include date range in plot titles or captions
       - use consistent color business-oriented color schemes

4. Configurable Analysis Framework
   The notebook shows the computation of metrics for a specific date range (entire year of 2023 compared to 2022). Refactor the code so that the data is first filtered according to configurable month and year & implement general-purpose metric calculations.

**Deliverables Expected**
- Refactored Jupyter notebook (EDA_Refactored.ipynb) with all improvements
- Business metrics module (business_metrics.py) with documented functions
- Requirements file (requirements.txt) listing all dependencies
- README section explaining how to use the refactored analysis

**Success Criteria**
- Easy-to read code & notebook (do not use icons in the printing statements or markdown cells)
- Configurable analysis that works for any date range
- Reusable code that can be applied to future datasets
- Maintainable structure that other analysts can easily understand and extend
- Maintain all existing analyses while improving the quality, structure, and usability of the notebook.
- Do not assume any business thresholds.
```

#### Dashboard Creation

**Prompt:**
```
Convert @EDA_Refactored.ipynb into a professional Streamlit dashboard with this exact layout:

## Layout Structure
- **Header**: Title + date range filter (applies globally)
    - Title: left
    - Date range filter: right
- **KPI Row**: 4 cards (Total Revenue, Monthly Growth, Average order Value, Total Orders)
    - Trend indicators for Total Revenue, Average Order Value and Total Orders
    - Use red for negative trends and green for positive trend
- **Charts Grid**: 2x2 layout
  - Revenue trend line chart:
      - solid line for the current period
      - dashed line for the previous period
      - Add grid lines for easier reading
      - Y-axis formatting - show values as $300K instead of $300,000
  - Top 10 categories bar chart sorted descending:
      - Use blue gradient (light shade for lower values)
      - Format values as $300K and $2M
  - Revenue by state: US choropleth map Color-coded by revenue amount
      - Use blue gradient
  - Bar chart showing satisfaction vs delivery time:
      - x-axis: Delivery time buckets (1-3 days, 4-7 days, etc.)
      - y-axis: Average review score
- **Bottom Row**: 2 cards
   - Average delivery time with trend indicator
   - Review Score:
       - Large number with stars
       - Subtitle: "Average Review Score"

## Key Requirements
- Use Plotly for all charts
- Filter update charts correctly
- Professional styling with trend arrows/colors
- Do not use icons
- Use uniform card heights for each row
- Show two decimal places for each trend indicator
- Include requirements.txt and README.md
```

### Project 3: Figma Design to Next.js Application

Building a complete web application from a Figma design mockup.

#### Project Overview

**Tech Stack:**
- Framework: Next.js
- Charts: Recharts
- Data Source: FRED API (optional)
- Design Tool: Figma

#### Getting Started

1. **Initialize Next.js:**
   ```bash
   npx create-next-app@latest .
   ```

2. **Get Figma Design:**
   - Download [Figma mockup](https://github.com/https-deeplearning-ai/sc-claude-code-files/blob/main/additional_files/key-indicators.fig)
   - Open with [Figma Desktop App](https://www.figma.com/downloads/)

3. **Setup MCP Servers:**
   ```bash
   # Figma Dev Mode MCP (requires Dev/Full seat)
   claude mcp add --transport http figma-dev-mode-mcp-server http://127.0.0.1:3845/mcp
   
   # Playwright for verification
   claude mcp add playwright npx @playwright/mcp@latest
   ```

4. **Enable Figma MCP Server:**
   - Open Figma design file
   - Figma menu → Preferences → Enable Dev Mode MCP Server
   - Server runs at `http://127.0.0.1:3845/mcp`

#### Implementation Workflow

**Step 1: Import Design**
```
Using the following figma mockup [paste link] use the figma dev MCP server to analyze the mockup and build the underlying code in this next.js application. Use the recharts library for creating charts to make this a web application. Check how this application looks using the playwright MCP server and verify it looks as close to the mock as possible.
```

**Step 2: Add Real Data (Optional)**
```
Populate these charts with real-world data from FRED
```

**Note:** Get FRED API key from [FRED API Documentation](https://fred.stlouisfed.org/docs/api/api_key.html)

#### Alternative: Framelink Figma MCP

If you don't have Figma Dev seat:

```bash
claude mcp add "Framelink Figma MCP" -- npx -y figma-developer-mcp --figma-api-key=YOUR-KEY --stdio
```

See [Framelink Guide](https://www.framelink.ai/docs/quickstart) for setup.

### Project Learning Outcomes

After completing these projects, you'll be able to:
- ✅ Understand and navigate complex codebases
- ✅ Add features to existing applications
- ✅ Create comprehensive test frameworks
- ✅ Refactor code for better architecture
- ✅ Work on multiple features in parallel
- ✅ Refactor notebooks into production code
- ✅ Create interactive dashboards
- ✅ Build applications from design mockups
- ✅ Integrate external tools via MCP
- ✅ Use visual verification workflows

---

## GitHub Integration and Hooks

### GitHub Actions Integration

Claude Code can integrate directly with GitHub to review code, implement features, and create pull requests.

#### Setup

**Easiest Method:**
```bash
/install-github-app
```

This sets up Claude Code GitHub Actions automatically.

#### Usage

Once configured, you can mention `@claude` in:
- **Pull Requests:** Code review, suggestions, implementations
- **Issues:** Feature requests, bug fixes, discussions

**Example in PR:**
```
@claude Please review this PR for:
- Security vulnerabilities
- Performance issues
- Code quality
- Best practices compliance
```

**Example in Issue:**
```
@claude Implement a user authentication system with:
- JWT tokens
- Password hashing
- Rate limiting
- Session management
```

#### Capabilities

Claude Code can:
- Review code and suggest improvements
- Implement features from issue descriptions
- Create pull requests
- Respond to comments
- Fix bugs
- Refactor code

**Documentation:** See [Claude Code GitHub Actions](https://docs.anthropic.com/en/docs/claude-code/github-actions) for complete guide.

### Hooks System

Hooks allow you to execute shell commands at various points in Claude Code's lifecycle.

#### Hook Types

1. **Before Tool Execution:** Run before Claude executes a tool
2. **After Tool Execution:** Run after Claude executes a tool
3. **Subagent Completion:** Run when a subagent finishes a task
4. **Response Completion:** Run when Claude finishes responding

#### Creating Hooks

Hooks are defined in `.claude/hooks/` directory.

**Example Hook:**
```bash
#!/bin/bash
# .claude/hooks/after_tool_execution.sh

# Log tool execution
echo "$(date): Tool executed: $TOOL_NAME" >> .claude/hooks.log

# Run tests after code changes
if [[ "$TOOL_NAME" == "write_file" ]]; then
    python -m pytest tests/ --quiet
fi
```

#### Common Use Cases

**Auto-formatting:**
```bash
# After code generation, auto-format
black .
isort .
```

**Auto-testing:**
```bash
# Run tests after file changes
pytest tests/ --quiet || echo "Tests failed"
```

**Notifications:**
```bash
# Send notification when subagent completes
notify-send "Claude Code" "Subagent task completed"
```

**Documentation:**
- [Hooks Guide](https://docs.anthropic.com/en/docs/claude-code/hooks-guide)
- [Hooks Reference](https://docs.anthropic.com/en/docs/claude-code/hooks)
- [Claude Code In Action - Hooks](https://anthropic.skilljar.com/claude-code-in-action/312000)

#### Best Practices

1. **Keep Hooks Fast:** Don't block Claude Code with slow operations
2. **Handle Errors:** Always handle potential failures gracefully
3. **Log Actions:** Log hook executions for debugging
4. **Test Hooks:** Verify hooks work before relying on them
5. **Document Purpose:** Comment what each hook does

---

## Resources and Next Steps

### Official Resources

- **Claude Code:** https://claude.ai/code
- **Claude Code Documentation:** https://docs.anthropic.com/en/docs/claude-code/overview
- **Claude Code Common Workflows:** https://docs.anthropic.com/en/docs/claude-code/common-workflows
- **Claude Code Best Practices:** https://www.anthropic.com/engineering/claude-code-best-practices
- **Claude Code Use Cases:** https://www.anthropic.com/news/how-anthropic-teams-use-claude-code
- **Claude Code In Action (Anthropic Academy):** https://anthropic.skilljar.com/claude-code-in-action
- **Anthropic Documentation:** https://docs.anthropic.com
- **Claude API:** https://docs.anthropic.com/claude/reference

### Course Codebases

**Project 1: RAG Chatbot**
- Starting codebase: https://github.com/https-deeplearning-ai/starting-ragchatbot-codebase.git
- Final state: https://github.com/https-deeplearning-ai/ragchatbot-codebase.git

**Project 2: E-Commerce Analysis**
- Lesson files: https://github.com/https-deeplearning-ai/sc-claude-code-files/tree/main/lesson7_files

**Project 3: Figma Dashboard**
- Figma mockup: https://github.com/https-deeplearning-ai/sc-claude-code-files/blob/main/additional_files/key-indicators.fig
- Final app: https://github.com/https-deeplearning-ai/FRED-dashboard.git

### MCP Server Resources

- **Playwright MCP:** https://github.com/microsoft/playwright-mcp
- **Figma Dev Mode MCP:** https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Dev-Mode-MCP-Server
- **Framelink Figma MCP:** https://www.framelink.ai/docs/quickstart
- **MCP with Claude Code:** https://docs.anthropic.com/en/docs/claude-code/mcp

### Additional Learning

- **Claude Code IDE Integrations:** https://docs.anthropic.com/en/docs/claude-code/ide-integrations
- **Claude Code GitHub Actions:** https://docs.anthropic.com/en/docs/claude-code/github-actions
- **Claude Code Hooks:** https://docs.anthropic.com/en/docs/claude-code/hooks-guide
- **Claude Code Subagents:** https://docs.anthropic.com/en/docs/claude-code/sub-agents
- **Claude Code Troubleshooting:** https://docs.anthropic.com/en/docs/claude-code/troubleshooting

### Comprehensive Learning Path

**Week 1: Installation & Fundamentals**
- ✅ Install Claude Code (see [Installation](#installation-and-setup))
- ✅ Learn core commands (`/init`, `#`, `@`, `/clear`, `/compact`)
- ✅ Initialize first project
- ✅ Understand CLAUDE.md
- ✅ Practice basic code generation
- ✅ Learn file referencing with `@`

**Week 2: Core Features & Workflows**
- ✅ Master planning mode vs auto-accept
- ✅ Learn screenshot integration
- ✅ Explore codebase with prompts
- ✅ Add features to existing code
- ✅ Practice code review workflows
- ✅ Generate documentation

**Week 3: Advanced Techniques**
- ✅ Setup MCP servers (Playwright, Figma)
- ✅ Use extended thinking mode
- ✅ Work with subagents
- ✅ Create custom slash commands
- ✅ Implement testing frameworks
- ✅ Refactor complex code

**Week 4: Real-World Projects**
- ✅ Build RAG chatbot (Project 1)
- ✅ Refactor notebook to dashboard (Project 2)
- ✅ Create app from Figma design (Project 3)
- ✅ Use git worktrees for parallel development
- ✅ Integrate GitHub Actions
- ✅ Setup hooks for automation

**Week 5: Mastery & Integration**
- ✅ Build complete applications from scratch
- ✅ Integrate Claude Code into daily workflow
- ✅ Create custom workflows
- ✅ Optimize for your team
- ✅ Share knowledge and best practices
- ✅ Contribute to community

### Practice Projects

**Beginner:**
1. **Todo App:** Full-stack application with CRUD operations
2. **Calculator:** Build a calculator with UI and logic
3. **Blog API:** REST API with authentication and posts

**Intermediate:**
4. **REST API:** Complete backend system with database
5. **Data Pipeline:** ETL processing system
6. **Dashboard:** Data visualization dashboard
7. **RAG System:** Build your own RAG chatbot

**Advanced:**
8. **Machine Learning:** ML model with API and frontend
9. **Microservices:** Distributed system architecture
10. **Design-to-Code:** Build app from Figma mockup
11. **Notebook Refactoring:** Refactor analysis notebook to production code
12. **Multi-Feature Project:** Use worktrees for parallel development

### Course Prerequisites Checklist

Before starting, ensure you have:

- [ ] Node.js 18+ installed
- [ ] Git installed and configured
- [ ] Basic terminal/command line knowledge
- [ ] Claude Code installed (`npm install -g @anthropic-ai/claude-code`)
- [ ] Anthropic account with API key
- [ ] (Optional) Python 3.11+ for backend projects
- [ ] (Optional) Next.js knowledge for frontend projects
- [ ] (Optional) Figma Desktop App for design projects

---

## Conclusion

Claude Code represents the future of AI-assisted development, combining Claude's advanced reasoning with a purpose-built coding environment. By mastering Claude Code, you can:

- **Generate high-quality code faster** than ever before
- **Understand and improve existing code** with AI assistance
- **Create comprehensive documentation** automatically
- **Review and optimize code** systematically
- **Build complete applications** from natural language descriptions

The key to success is:
1. **Be specific** in your prompts
2. **Iterate and refine** based on results
3. **Use code review** to ensure quality
4. **Request documentation** always
5. **Test everything** thoroughly
6. **Leverage MCP servers** for extended capabilities
7. **Use extended thinking** for complex problems
8. **Work in parallel** with git worktrees
9. **Automate with hooks** for efficiency
10. **Integrate with GitHub** for team workflows

### Mastery Checklist

By completing this tutorial, you should be able to:

- [ ] Install and configure Claude Code on any platform
- [ ] Initialize projects and manage project memory
- [ ] Use all core commands effectively
- [ ] Reference files and manage context
- [ ] Setup and use MCP servers (Playwright, Figma)
- [ ] Use extended thinking modes for complex tasks
- [ ] Work with subagents for parallel problem-solving
- [ ] Create custom slash commands
- [ ] Use git worktrees for parallel development
- [ ] Implement comprehensive testing frameworks
- [ ] Refactor code and notebooks effectively
- [ ] Build complete applications from designs
- [ ] Integrate GitHub Actions
- [ ] Setup and use hooks for automation
- [ ] Build all three course projects independently

### Next Steps for Mastery

1. **Complete All Three Projects:**
   - RAG Chatbot (Lessons 2-6)
   - E-Commerce Dashboard (Lesson 7)
   - Figma to Next.js App (Lesson 8)

2. **Build Your Own Projects:**
   - Start with simple applications
   - Gradually increase complexity
   - Apply all techniques learned

3. **Share Your Knowledge:**
   - Document your workflows
   - Share custom commands
   - Help others learn Claude Code

4. **Stay Updated:**
   - Follow Anthropic updates
   - Join Claude Code community
   - Experiment with new features

Start practicing with Claude Code today, and you'll be amazed at how it transforms your development workflow!

---

**Happy coding with Claude Code! 🚀**

*This tutorial incorporates content from the official Claude Code course (Lessons 0-8) and extends it with expert-level techniques and real-world examples. For the latest updates and additional resources, visit the [official Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/overview).*

