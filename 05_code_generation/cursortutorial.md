# Cursor IDE: Complete Tutorial and Mastery Guide

*Master the World's Most Advanced AI-Powered Code Editor from Beginner to Expert*

**Download Cursor:** https://cursor.sh

---

## Table of Contents

1. [Introduction to Cursor IDE](#introduction-to-cursor-ide)
2. [Installation and Setup](#installation-and-setup)
3. [Getting Started with Cursor](#getting-started-with-cursor)
4. [Interface and Navigation](#interface-and-navigation)
5. [Core AI Features](#core-ai-features)
6. [Advanced AI Features](#advanced-ai-features)
7. [Commands and Shortcuts](#commands-and-shortcuts)
8. [Workflows and Best Practices](#workflows-and-best-practices)
9. [Integration and Extensions](#integration-and-extensions)
10. [Advanced Techniques](#advanced-techniques)
11. [Troubleshooting and Optimization](#troubleshooting-and-optimization)
12. [Real-World Projects](#real-world-projects)
13. [Resources and Next Steps](#resources-and-next-steps)

---

## Introduction to Cursor IDE

### What is Cursor?

Cursor is an AI-powered code editor built on VS Code that integrates advanced AI capabilities directly into your development workflow. Unlike traditional IDEs that add AI as an extension, Cursor is designed from the ground up to leverage AI for every aspect of coding.

### Why Cursor?

**Key Advantages:**
- **Deep Code Understanding:** AI understands your entire codebase context
- **Multi-File Editing:** Edit multiple files simultaneously with AI assistance
- **Natural Language Interface:** Chat with AI about your code
- **Codebase-Aware:** AI understands your project structure and patterns
- **Fast and Responsive:** Optimized for speed and efficiency
- **Privacy-Focused:** Local processing options available
- **VS Code Compatible:** Works with VS Code extensions

### Cursor vs. Other Tools

| Aspect | Cursor | VS Code | GitHub Copilot | Claude Code |
|--------|--------|---------|----------------|-------------|
| **AI Integration** | ⭐⭐⭐⭐⭐ Native | ⭐⭐ Extension | ⭐⭐⭐ Extension | ⭐⭐⭐⭐⭐ Native |
| **Codebase Context** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Limited | ⭐⭐ Limited | ⭐⭐⭐⭐⭐ Excellent |
| **Multi-File Editing** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Manual | ⭐⭐ Limited | ⭐⭐⭐⭐ Good |
| **Chat Interface** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐ Extension | ⭐⭐ Limited | ⭐⭐⭐⭐⭐ Excellent |
| **Speed** | ⭐⭐⭐⭐⭐ Fast | ⭐⭐⭐⭐ Fast | ⭐⭐⭐⭐ Fast | ⭐⭐⭐ Web-based |
| **Offline Capability** | ⭐⭐⭐⭐ Good | ⭐⭐⭐⭐⭐ Full | ⭐⭐ Limited | ⭐⭐ None |
| **Extension Support** | ⭐⭐⭐⭐⭐ Full VS Code | ⭐⭐⭐⭐⭐ Full | ⭐⭐⭐⭐ Good | ⭐⭐ Limited |

### Cursor's Unique Features

1. **Composer:** Multi-file editing with AI understanding of relationships
2. **Agent Mode:** AI that can make multiple changes across your codebase
3. **Codebase Indexing:** AI understands your entire project structure
4. **Custom Rules:** Define how AI should behave in your codebase
5. **Chat with Context:** AI understands your files, selection, and codebase
6. **Inline Editing:** AI suggestions directly in your code

---

## Installation and Setup

### System Requirements

**Minimum Requirements:**
- **macOS:** macOS 10.15 (Catalina) or later
- **Windows:** Windows 10 or later
- **Linux:** Ubuntu 18.04+, Debian 10+, or equivalent
- **RAM:** 4GB minimum (8GB+ recommended)
- **Storage:** 500MB for installation

**Recommended:**
- 16GB+ RAM for large codebases
- SSD storage for better performance
- Modern CPU (multi-core recommended)

### Installation Steps

#### macOS Installation

**Method 1: Direct Download**
1. Visit https://cursor.sh
2. Click "Download for Mac"
3. Open the downloaded `.dmg` file
4. Drag Cursor to Applications folder
5. Launch Cursor from Applications

**Method 2: Homebrew**
```bash
brew install --cask cursor
```

#### Windows Installation

1. Visit https://cursor.sh
2. Click "Download for Windows"
3. Run the installer (`.exe` file)
4. Follow installation wizard
5. Launch Cursor from Start menu

#### Linux Installation

**Debian/Ubuntu:**
```bash
# Download .deb package
wget https://downloader.cursor.sh/linux/appImage/x64 -O cursor.AppImage

# Make executable
chmod +x cursor.AppImage

# Run
./cursor.AppImage

# Or install system-wide
sudo mv cursor.AppImage /usr/local/bin/cursor
```

**Alternative: AppImage**
```bash
# Download AppImage
wget https://downloader.cursor.sh/linux/appImage/x64 -O cursor.AppImage
chmod +x cursor.AppImage
./cursor.AppImage
```

### First-Time Setup

#### Step 1: Launch Cursor

On first launch, Cursor will:
- Ask you to sign in or create an account
- Request permissions (file access, etc.)
- Show welcome screen with setup options

#### Step 2: Sign In

**Options:**
- **GitHub:** Sign in with GitHub account
- **Google:** Sign in with Google account
- **Email:** Create account with email

**Why Sign In?**
- Sync settings across devices
- Access premium features
- Save chat history
- Team collaboration features

#### Step 3: Choose AI Model

Cursor offers multiple AI models:

**Free Tier:**
- Claude Sonnet 3.5 (limited requests)
- GPT-4 (limited requests)

**Pro Tier ($20/month):**
- Unlimited Claude Sonnet 3.5
- GPT-4 access
- Faster responses
- Priority support

**Business Tier:**
- Everything in Pro
- Team features
- Admin controls
- Custom models

**Recommendation:** Start with Claude Sonnet 3.5 (best balance of quality and speed)

#### Step 4: Initial Configuration

**Essential Settings:**

1. **Open Settings:**
   - `Cmd+,` (Mac) or `Ctrl+,` (Windows/Linux)
   - Or: File → Preferences → Settings

2. **Configure AI Settings:**
   - **Model:** Choose Claude Sonnet 3.5 or GPT-4
   - **Temperature:** 0.7 (balanced creativity/consistency)
   - **Max Tokens:** 4000 (for longer responses)

3. **Editor Settings:**
   - **Font Size:** 14px (adjustable)
   - **Theme:** Choose light or dark
   - **Word Wrap:** Enable for long lines
   - **Minimap:** Enable for code navigation

4. **File Settings:**
   - **Auto Save:** Enable (saves after delay)
   - **Trim Trailing Whitespace:** Enable
   - **Insert Final Newline:** Enable

### Subscription and Pricing

**Free Tier:**
- Limited AI requests per month
- Basic features
- Community support

**Pro ($20/month):**
- Unlimited AI requests
- All AI models
- Faster responses
- Priority support
- Codebase indexing

**Business (Custom pricing):**
- Everything in Pro
- Team collaboration
- Admin controls
- Custom models
- Enterprise support

**Trial:** 14-day free trial of Pro features

---

## Getting Started with Cursor

### Your First Project

#### Step 1: Open a Folder

**Method 1: From Welcome Screen**
1. Click "Open Folder"
2. Navigate to your project directory
3. Click "Select Folder"

**Method 2: From Menu**
- `File → Open Folder...`
- `Cmd+O` (Mac) or `Ctrl+O` (Windows/Linux)

**Method 3: From Terminal**
```bash
cd /path/to/your/project
cursor .
```

#### Step 2: Explore the Interface

**Main Areas:**
- **Sidebar (Left):** File explorer, search, source control, extensions
- **Editor (Center):** Code editing area
- **Terminal (Bottom):** Integrated terminal
- **AI Chat (Right):** AI assistant panel

#### Step 3: Your First AI Interaction

**Open Chat:**
- `Cmd+L` (Mac) or `Ctrl+L` (Windows/Linux)
- Or click chat icon in sidebar

**Try This:**
```
Explain what this codebase does
```

Cursor will analyze your codebase and provide an overview.

### Basic Navigation

#### Opening Files
- **Click file** in sidebar
- **Cmd+P** (Mac) or `Ctrl+P` (Windows): Quick file open
- **Cmd+Shift+P** (Mac) or `Ctrl+Shift+P` (Windows): Command palette

#### Switching Between Files
- **Cmd+Tab** (Mac) or `Ctrl+Tab` (Windows): Switch between open files
- **Cmd+1, Cmd+2, etc.:** Switch to editor groups
- **Cmd+K, Cmd+Arrow:** Navigate editor groups

#### Closing Files
- **Cmd+W** (Mac) or `Ctrl+W` (Windows): Close current file
- **Cmd+K, W** (Mac) or `Ctrl+K, W` (Windows): Close all files

---

## Interface and Navigation

### Understanding the Layout

```
┌─────────────────────────────────────────────────────────┐
│ File  Edit  View  Go  Run  Terminal  Help  [AI Chat]   │ ← Menu Bar
├──────┬──────────────────────────────────────┬──────────┤
│      │                                        │          │
│ Side │         Editor Area                   │  AI Chat │
│ bar  │         (Your Code)                   │  Panel   │
│      │                                        │          │
│      │                                        │          │
├──────┴──────────────────────────────────────┴──────────┤
│ Terminal / Output / Problems / Debug Console            │
└─────────────────────────────────────────────────────────┘
```

### Sidebar Components

#### 1. Explorer (File Tree)
- **Icon:** Folder icon
- **Shortcut:** `Cmd+Shift+E` (Mac) or `Ctrl+Shift+E` (Windows)
- **Features:**
  - File navigation
  - Folder structure
  - File operations (new, delete, rename)
  - Git status indicators

#### 2. Search
- **Icon:** Magnifying glass
- **Shortcut:** `Cmd+Shift+F` (Mac) or `Ctrl+Shift+F` (Windows)
- **Features:**
  - Text search across files
  - Regex search
  - File filtering
  - Replace functionality

#### 3. Source Control (Git)
- **Icon:** Branch icon
- **Shortcut:** `Cmd+Shift+G` (Mac) or `Ctrl+Shift+G` (Windows)
- **Features:**
  - Git status
  - Stage/unstage changes
  - Commit messages
  - Branch management
  - Diff viewer

#### 4. Run and Debug
- **Icon:** Play icon
- **Shortcut:** `Cmd+Shift+D` (Mac) or `Ctrl+Shift+D` (Windows)
- **Features:**
  - Debug configurations
  - Breakpoints
  - Variable inspection
  - Call stack

#### 5. Extensions
- **Icon:** Blocks icon
- **Shortcut:** `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows)
- **Features:**
  - Browse extensions
  - Install/disable extensions
  - Extension settings

#### 6. AI Chat
- **Icon:** Chat bubble
- **Shortcut:** `Cmd+L` (Mac) or `Ctrl+L` (Windows)
- **Features:**
  - Chat with AI about code
  - Code explanations
  - Code generation
  - Code review

### Editor Area

#### Tab Management
- **Multiple tabs:** Open multiple files
- **Split editor:** `Cmd+\` (Mac) or `Ctrl+\` (Windows)
- **Close tab:** `Cmd+W` (Mac) or `Ctrl+W` (Windows)
- **Reopen closed tab:** `Cmd+Shift+T` (Mac) or `Ctrl+Shift+T` (Windows)

#### Editor Groups
- **Split vertically:** `Cmd+\` (Mac) or `Ctrl+\` (Windows)
- **Split horizontally:** `Cmd+K, Cmd+\` (Mac) or `Ctrl+K, Ctrl+\` (Windows)
- **Focus next group:** `Cmd+K, Cmd+Right` (Mac) or `Ctrl+K, Ctrl+Right` (Windows)
- **Focus previous group:** `Cmd+K, Cmd+Left` (Mac) or `Ctrl+K, Ctrl+Left` (Windows)

### Integrated Terminal

#### Opening Terminal
- **Toggle:** `` Cmd+` `` (Mac) or `` Ctrl+` `` (Windows)
- **New terminal:** `Cmd+Shift+` `` (Mac) or `Ctrl+Shift+` `` (Windows)
- **Split terminal:** `Cmd+\` in terminal (Mac) or `Ctrl+\` (Windows)

#### Terminal Features
- Multiple terminal tabs
- Terminal selection dropdown
- Terminal splitting
- Custom shell configuration

### Command Palette

**Open:** `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)

**Common Commands:**
- `>File: New File`
- `>File: Save`
- `>Preferences: Open Settings`
- `>Git: Commit`
- `>Cursor: Chat`
- `>Cursor: Composer`

---

## Core AI Features

### 1. Chat with AI

The Chat feature allows you to have natural language conversations with AI about your code.

#### Opening Chat

**Methods:**
1. **Keyboard:** `Cmd+L` (Mac) or `Ctrl+L` (Windows)
2. **Sidebar:** Click chat icon
3. **Command Palette:** `>Cursor: Chat`

#### Chat Interface

**Components:**
- **Input box:** Type your questions
- **Chat history:** Previous conversations
- **Context indicators:** Shows what files/context AI can see
- **Model selector:** Switch between AI models

#### Using Chat Effectively

**Basic Usage:**
```
Explain this function
```

**With File Context:**
```
@filename.py Explain how this function works
```

**With Selection:**
1. Select code
2. Open chat (`Cmd+L`)
3. Ask: "Explain this code" or "Refactor this"

**With Multiple Files:**
```
@file1.py @file2.py How do these files work together?
```

#### Chat Features

**1. Code Explanation**
```
Explain what this code does
```

**2. Code Generation**
```
Create a function that calculates payroll tax for an employee
```

**3. Code Review**
```
Review this code for bugs and improvements
```

**4. Debugging Help**
```
Why is this function returning an error?
```

**5. Refactoring Suggestions**
```
How can I refactor this to be more maintainable?
```

#### Chat Best Practices

**✅ Do:**
- Be specific about what you want
- Reference files with `@filename`
- Select code before asking questions
- Provide context about your goals
- Ask follow-up questions

**❌ Don't:**
- Ask vague questions
- Forget to provide context
- Ignore AI's suggestions without trying
- Ask for entire applications in one request

### 2. Composer (Multi-File Editing)

Composer is Cursor's most powerful feature—it allows AI to make coordinated changes across multiple files simultaneously.

#### Opening Composer

**Methods:**
1. **Keyboard:** `Cmd+I` (Mac) or `Ctrl+I` (Windows)
2. **Command Palette:** `>Cursor: Composer`
3. **Chat:** Type `/composer` in chat

#### Composer Interface

**Components:**
- **Input area:** Describe what you want to build/change
- **File list:** Shows files that will be modified
- **Preview:** See changes before applying
- **Apply button:** Apply all changes at once

#### Using Composer

**Example 1: Add a Feature**
```
Add user authentication to this application:
- Create login endpoint
- Add password hashing
- Create user model
- Add JWT token generation
```

**Example 2: Refactor Across Files**
```
Refactor the payroll calculation logic:
- Move calculation functions to a separate module
- Update all imports
- Add comprehensive error handling
- Update tests
```

**Example 3: Fix Bugs**
```
Fix the tax calculation bug:
- The issue is in calculate_tax() function
- Update all places that call this function
- Add validation for edge cases
- Update related tests
```

#### Composer Workflow

1. **Describe Your Goal:**
   ```
   Add a new API endpoint for processing payroll runs
   ```

2. **Review Planned Changes:**
   - Composer shows which files will be modified
   - Preview changes before applying
   - You can exclude files if needed

3. **Apply Changes:**
   - Click "Apply" or press `Cmd+Enter` (Mac) or `Ctrl+Enter` (Windows)
   - All changes applied simultaneously
   - Files are saved automatically

4. **Review and Iterate:**
   - Review the changes
   - Ask for adjustments if needed
   - Test the implementation

#### Composer Best Practices

**✅ Do:**
- Be specific about what you want
- Mention all related files
- Describe the desired outcome clearly
- Review changes before applying
- Test after applying changes

**❌ Don't:**
- Make vague requests
- Apply changes without reviewing
- Forget to test after changes
- Make too many changes at once (break into steps)

### 3. Inline AI Suggestions

Cursor provides AI suggestions directly in your code as you type.

#### How It Works

- **Automatic:** Suggestions appear as you code
- **Context-Aware:** Understands your codebase
- **Multi-Line:** Can suggest entire functions
- **Accept/Reject:** `Tab` to accept, `Esc` to dismiss

#### Using Inline Suggestions

**Basic Usage:**
1. Start typing code
2. AI suggests completions
3. Press `Tab` to accept
4. Press `Esc` to dismiss

**Triggering Suggestions:**
- Type naturally, AI suggests
- Press `Cmd+K` (Mac) or `Ctrl+K` (Windows) for manual trigger
- Select code and ask for completion

#### Inline Suggestion Settings

**Configure in Settings:**
- **Enable/Disable:** Toggle inline suggestions
- **Trigger:** Automatic or manual
- **Suggestion delay:** Adjust timing
- **Model:** Choose AI model for suggestions

### 4. Code Explanation

Get instant explanations of any code.

#### Methods

**Method 1: Select and Ask**
1. Select code
2. `Cmd+L` to open chat
3. Ask: "Explain this code"

**Method 2: Hover Explanation**
- Hover over code
- See tooltip explanation (if enabled)

**Method 3: Command**
- Select code
- `Cmd+Shift+P` → `>Cursor: Explain Code`

#### Example

**Selected Code:**
```python
def calculate_net_pay(gross_pay, tax_rate, deductions):
    tax = gross_pay * tax_rate
    return gross_pay - tax - sum(deductions)
```

**Ask:** "Explain this function"

**AI Response:**
```
This function calculates an employee's net pay by:
1. Calculating tax: gross_pay × tax_rate
2. Subtracting tax and all deductions from gross pay
3. Returning the final net pay amount

Example: If gross_pay=$5000, tax_rate=0.22, deductions=[100, 50]:
- tax = $5000 × 0.22 = $1100
- net_pay = $5000 - $1100 - $150 = $3750
```

### 5. Code Review

Get AI-powered code reviews.

#### Using Code Review

**Method 1: Chat**
```
Review this code for:
- Security issues
- Performance problems
- Best practices
- Potential bugs
```

**Method 2: Select and Review**
1. Select code block
2. Open chat
3. Ask for review

**Method 3: File Review**
```
@payroll_calculator.py Review this entire file
```

#### Review Output

AI provides:
- ✅ **Strengths:** What's good about the code
- ⚠️ **Issues:** Problems found
- 🔧 **Suggestions:** How to improve
- 📝 **Examples:** Code improvements

### 6. Refactoring Assistance

AI helps refactor code safely.

#### Refactoring Workflows

**Workflow 1: Extract Function**
1. Select code to extract
2. Chat: "Extract this into a function called `calculate_tax`"
3. AI creates function and updates calls

**Workflow 2: Rename Variable**
1. Select variable
2. `F2` to rename (with AI assistance)
3. AI updates all references

**Workflow 3: Improve Structure**
```
Refactor this code to:
- Use dependency injection
- Add error handling
- Improve naming
- Add type hints
```

### 7. Documentation Generation

Generate comprehensive documentation.

#### Generating Documentation

**For Functions:**
```
@calculate_payroll.py Generate docstrings for all functions
```

**For Files:**
```
@payroll_module.py Generate module documentation
```

**For API:**
```
@api_routes.py Generate API documentation with examples
```

#### Documentation Types

- **Docstrings:** Function/class documentation
- **README:** Project documentation
- **API Docs:** Endpoint documentation
- **Comments:** Inline code comments

---

## Advanced AI Features

### 1. Agent Mode

Agent Mode allows AI to make multiple sequential changes across your codebase autonomously.

#### Enabling Agent Mode

**Method 1: Command**
- `Cmd+Shift+P` → `>Cursor: Enable Agent Mode`

**Method 2: Settings**
- Settings → Cursor → Enable Agent Mode

#### Using Agent Mode

**Basic Usage:**
```
Implement user authentication:
- Create user model
- Add login endpoint
- Create password hashing
- Add JWT tokens
- Update frontend
- Add tests
```

**Agent Workflow:**
1. You describe the goal
2. Agent plans the changes
3. Agent makes changes sequentially
4. Agent tests and verifies
5. You review and approve

#### Agent Mode Features

- **Multi-step execution:** Makes multiple related changes
- **Context awareness:** Understands codebase relationships
- **Error handling:** Fixes errors automatically
- **Testing:** Can run tests after changes
- **Rollback:** Can undo changes if needed

#### Agent Mode Best Practices

**✅ Do:**
- Use for complex, multi-file changes
- Review each step
- Test after agent completes
- Use for well-defined tasks

**❌ Don't:**
- Use for simple, single-file changes
- Let agent make changes without review
- Use for critical production code without testing
- Use for tasks requiring human judgment

### 2. Codebase Indexing

Cursor indexes your entire codebase to understand structure and relationships.

#### How Indexing Works

- **Automatic:** Indexes on project open
- **Background:** Runs while you work
- **Incremental:** Updates as files change
- **Semantic:** Understands code meaning, not just text

#### Using Indexed Codebase

**Semantic Search:**
```
Find all functions that calculate payroll taxes
```

**Codebase Questions:**
```
How does the payroll processing flow work?
```

**Relationship Understanding:**
```
Show me all files that depend on payroll_calculator.py
```

#### Indexing Settings

**Configure in Settings:**
- **Enable/Disable:** Toggle indexing
- **Index depth:** How deep to index
- **Exclude patterns:** Files/folders to exclude
- **Update frequency:** How often to re-index

### 3. Custom Rules and Guidelines

Define how AI should behave in your codebase.

#### Creating Rules

**Location:** `.cursorrules` file in project root

**Example Rules:**
```
# Cursor Rules for Greenshades Payroll System

## Code Style
- Use Python type hints for all functions
- Follow PEP 8 style guide
- Use async/await for database operations
- Always include docstrings

## Naming Conventions
- Functions: snake_case
- Classes: PascalCase
- Constants: UPPER_SNAKE_CASE
- Private methods: _leading_underscore

## Security
- Never hardcode API keys or passwords
- Always validate user input
- Use parameterized queries for database
- Hash passwords with bcrypt

## Testing
- Write tests for all new functions
- Aim for 80%+ code coverage
- Use pytest for testing
- Mock external dependencies

## Payroll-Specific
- Always validate tax calculations
- Handle edge cases (zero hours, negative values)
- Log all payroll processing steps
- Maintain audit trail
```

#### Using Rules

Once `.cursorrules` is created:
- AI automatically follows these rules
- Suggestions align with your guidelines
- Code generation matches your style
- Refactoring maintains your conventions

#### Rule Best Practices

- **Be Specific:** Clear, actionable rules
- **Update Regularly:** Keep rules current
- **Team Alignment:** Share rules with team
- **Version Control:** Commit `.cursorrules` to git

### 4. Codebase Q&A

Ask questions about your entire codebase.

#### Using Codebase Q&A

**Example Questions:**
```
How does the payroll processing work end-to-end?
```

```
What are all the tax calculation functions?
```

```
Show me how employee data flows through the system
```

```
What are the main components of the Avocado platform?
```

#### Q&A Features

- **Semantic understanding:** Understands code meaning
- **Cross-file analysis:** Connects related code
- **Visualization:** Can create diagrams
- **Documentation:** Can generate docs from answers

### 5. Multi-File Context

Work with multiple files simultaneously.

#### Adding Files to Context

**Method 1: @ Mentions**
```
@file1.py @file2.py How do these work together?
```

**Method 2: Selection**
- Select code in multiple files
- Chat automatically includes all selections

**Method 3: Composer**
- Composer automatically includes related files
- Shows file dependencies

#### Context Management

**View Current Context:**
- Chat shows which files are in context
- Composer shows file list
- Can add/remove files from context

**Context Limits:**
- Token limits apply
- Cursor manages context efficiently
- Large codebases may need selective context

---

## Commands and Shortcuts

### Essential Keyboard Shortcuts

#### Navigation Shortcuts

| Action | macOS | Windows/Linux |
|--------|-------|---------------|
| **Open File** | `Cmd+P` | `Ctrl+P` |
| **Go to Symbol** | `Cmd+Shift+O` | `Ctrl+Shift+O` |
| **Go to Line** | `Cmd+G` | `Ctrl+G` |
| **Command Palette** | `Cmd+Shift+P` | `Ctrl+Shift+P` |
| **Quick Open** | `Cmd+P` | `Ctrl+P` |

#### AI Feature Shortcuts

| Action | macOS | Windows/Linux |
|--------|-------|---------------|
| **Open Chat** | `Cmd+L` | `Ctrl+L` |
| **Open Composer** | `Cmd+I` | `Ctrl+I` |
| **Inline Suggestion** | `Cmd+K` | `Ctrl+K` |
| **Accept Suggestion** | `Tab` | `Tab` |
| **Reject Suggestion** | `Esc` | `Esc` |
| **Trigger Suggestion** | `Cmd+K` | `Ctrl+K` |

#### Editor Shortcuts

| Action | macOS | Windows/Linux |
|--------|-------|---------------|
| **Save** | `Cmd+S` | `Ctrl+S` |
| **Save All** | `Cmd+K, S` | `Ctrl+K, S` |
| **Close Tab** | `Cmd+W` | `Ctrl+W` |
| **Split Editor** | `Cmd+\` | `Ctrl+\` |
| **New File** | `Cmd+N` | `Ctrl+N` |
| **Find** | `Cmd+F` | `Ctrl+F` |
| **Replace** | `Cmd+H` | `Ctrl+H` |
| **Find in Files** | `Cmd+Shift+F` | `Ctrl+Shift+F` |

#### Terminal Shortcuts

| Action | macOS | Windows/Linux |
|--------|-------|---------------|
| **Toggle Terminal** | `` Cmd+` `` | `` Ctrl+` `` |
| **New Terminal** | `Cmd+Shift+` `` | `Ctrl+Shift+` `` |
| **Split Terminal** | `Cmd+\` | `Ctrl+\` |

#### Git Shortcuts

| Action | macOS | Windows/Linux |
|--------|-------|---------------|
| **Source Control** | `Cmd+Shift+G` | `Ctrl+Shift+G` |
| **Stage Changes** | `Cmd+Shift+P` → "Stage" | `Ctrl+Shift+P` → "Stage" |
| **Commit** | `Cmd+Enter` (in SCM) | `Ctrl+Enter` (in SCM) |

### Command Palette Commands

**Open:** `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)

**Essential Commands:**

**File Operations:**
- `>File: New File`
- `>File: Save`
- `>File: Save All`
- `>File: Revert File`

**Cursor AI:**
- `>Cursor: Chat`
- `>Cursor: Composer`
- `>Cursor: Explain Code`
- `>Cursor: Generate Code`

**Git:**
- `>Git: Commit`
- `>Git: Push`
- `>Git: Pull`
- `>Git: Show Output`

**Editor:**
- `>Editor: Format Document`
- `>Editor: Format Selection`
- `>Editor: Indent Lines`
- `>Editor: Outdent Lines`

**View:**
- `>View: Toggle Sidebar`
- `>View: Toggle Terminal`
- `>View: Toggle Problems`
- `>View: Command Palette`

### Custom Keybindings

**Create Custom Shortcuts:**

1. `Cmd+K, Cmd+S` (Mac) or `Ctrl+K, Ctrl+S` (Windows)
2. Search for command
3. Click `+` to add keybinding
4. Press desired key combination
5. Save

**Example Custom Bindings:**
- `Cmd+Shift+C`: Open Composer
- `Cmd+Shift+X`: Explain selected code
- `Cmd+Shift+R`: Review code

---

## Workflows and Best Practices

### Daily Development Workflow

#### Morning Routine

1. **Open Project:**
   ```bash
   cd /path/to/project
   cursor .
   ```

2. **Check Codebase Status:**
   - Open chat: `Cmd+L`
   - Ask: "What changed since yesterday?"

3. **Review Pending Tasks:**
   - Check git status
   - Review TODOs
   - Plan day's work

#### Coding Workflow

**Step 1: Understand Requirements**
```
@requirements.md Explain what needs to be built
```

**Step 2: Plan Implementation**
```
Create a plan for implementing [feature]:
- List all files that need changes
- Outline the approach
- Identify dependencies
```

**Step 3: Implement with Composer**
```
Implement [feature] following the plan:
- Create necessary files
- Update existing files
- Add error handling
- Include tests
```

**Step 4: Review and Test**
- Review generated code
- Run tests
- Fix any issues
- Commit changes

### Code Review Workflow

#### Step 1: Select Code
- Select function, class, or file
- Or use `@filename` in chat

#### Step 2: Request Review
```
Review this code for:
- Security vulnerabilities
- Performance issues
- Code quality
- Best practices
- Potential bugs
```

#### Step 3: Address Issues
- Review AI suggestions
- Apply fixes
- Re-review if needed

#### Step 4: Document
```
Generate documentation for this code
```

### Refactoring Workflow

#### Step 1: Identify Target
```
@legacy_code.py Analyze this code and identify refactoring opportunities
```

#### Step 2: Plan Refactoring
```
Create a refactoring plan:
- What needs to change
- Which files are affected
- How to maintain functionality
- What tests are needed
```

#### Step 3: Execute with Composer
```
Refactor according to the plan:
- Apply modern patterns
- Improve structure
- Add type hints
- Update documentation
```

#### Step 4: Verify
- Run tests
- Check functionality
- Review changes
- Commit

### Testing Workflow

#### Generate Tests
```
@function.py Generate comprehensive unit tests for this function
```

#### Test Coverage
```
@tests/ Analyze test coverage and suggest missing tests
```

#### Fix Failing Tests
```
@test_file.py These tests are failing. Fix them and explain the issues
```

### Debugging Workflow

#### Step 1: Identify Issue
```
@error_log.txt Analyze this error and explain what's wrong
```

#### Step 2: Locate Problem
```
@codebase Find where this error might be occurring
```

#### Step 3: Fix with AI
```
Fix the bug in @problematic_file.py:
- The issue is [description]
- Expected behavior: [description]
- Current behavior: [description]
```

#### Step 4: Verify Fix
- Test the fix
- Ensure no regressions
- Update tests if needed

---

## Integration and Extensions

### Git Integration

Cursor has excellent Git integration built-in.

#### Source Control Panel

**Open:** `Cmd+Shift+G` (Mac) or `Ctrl+Shift+G` (Windows)

**Features:**
- **Changes:** See modified files
- **Staged:** See staged changes
- **Diff View:** Compare changes
- **Commit:** Write commit messages
- **Branch:** Switch branches
- **Merge:** Handle merges

#### Git Workflow in Cursor

**1. View Changes:**
- Source Control panel shows all changes
- Click file to see diff
- `+` to stage, `-` to unstage

**2. Stage Changes:**
- Click `+` next to file
- Or: `Cmd+Shift+P` → "Stage All Changes"

**3. Commit:**
- Write commit message
- `Cmd+Enter` to commit
- Or use AI to generate commit message:
  ```
  Generate a commit message for these changes
  ```

**4. Push/Pull:**
- `...` menu in Source Control
- Push, Pull, Fetch options

#### AI-Powered Git

**Generate Commit Messages:**
```
Review my changes and generate a professional commit message
```

**Explain Changes:**
```
What did I change in this commit?
```

**Suggest Improvements:**
```
Review my staged changes and suggest improvements before committing
```

### Terminal Integration

#### Using Integrated Terminal

**Open Terminal:**
- `` Cmd+` `` (Mac) or `` Ctrl+` `` (Windows)
- Or: View → Terminal

**Terminal Features:**
- Multiple terminals
- Split terminals
- Terminal selection
- Custom shell

#### Terminal + AI

**Ask AI About Commands:**
```
What does this command do: git rebase -i HEAD~3
```

**Generate Commands:**
```
Generate a command to find all Python files modified in the last week
```

**Debug Commands:**
```
This command failed: [paste error]. What's wrong?
```

### Debugger Integration

#### Setting Up Debugging

**1. Create Launch Configuration:**
- `Run and Debug` panel
- `create a launch.json file`
- Choose your environment (Python, Node.js, etc.)

**2. Set Breakpoints:**
- Click left margin
- Or `F9` on line

**3. Start Debugging:**
- `F5` to start
- Use debug controls

#### AI-Assisted Debugging

**Explain Debug Output:**
```
@debug_output.txt Explain what this debug information means
```

**Find Bug:**
```
I'm debugging this issue: [description]. Help me find the bug.
```

**Fix Bug:**
```
Fix the bug causing this error: [error message]
```

### Extension Ecosystem

Cursor supports all VS Code extensions.

#### Installing Extensions

**Method 1: Extensions Panel**
1. `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows)
2. Search for extension
3. Click "Install"

**Method 2: Command Palette**
- `Cmd+Shift+P` → "Extensions: Install Extensions"

#### Recommended Extensions

**Python:**
- Python (Microsoft)
- Pylance
- Black Formatter
- pytest

**JavaScript/TypeScript:**
- ESLint
- Prettier
- TypeScript and JavaScript Language Features

**Git:**
- GitLens
- Git Graph

**Productivity:**
- Todo Tree
- Error Lens
- Better Comments

**AI-Enhanced:**
- GitHub Copilot (works alongside Cursor)
- Codeium (alternative AI assistant)

#### Extension Management

**Enable/Disable:**
- Extensions panel
- Toggle extension on/off

**Configure:**
- Extension settings in Preferences
- Per-extension configuration

---

## Advanced Techniques

### 1. Prompt Engineering for Cursor

#### Effective Prompts

**✅ Good Prompts:**
```
Create a Python function that calculates payroll tax:
- Input: gross_pay (float), tax_rate (float), state (string)
- Output: tax_amount (float)
- Handle edge cases: zero pay, invalid state
- Include type hints and docstring
- Add error handling
```

**❌ Bad Prompts:**
```
Make a tax function
```

#### Prompt Patterns

**Pattern 1: Specification**
```
Create [what] that [does what]:
- Requirement 1
- Requirement 2
- Requirement 3
```

**Pattern 2: Example-Based**
```
Create a function similar to @existing_function.py but for [different purpose]:
- Similar structure
- Different logic: [describe]
- Same error handling approach
```

**Pattern 3: Refactoring**
```
Refactor @file.py to:
- Use [pattern/approach]
- Improve [aspect]
- Maintain [requirement]
```

### 2. Context Management

#### Managing Context Window

**Add Files to Context:**
```
@file1.py @file2.py @file3.py [your question]
```

**Remove from Context:**
- Clear chat to reset context
- Start new conversation

**Optimize Context:**
- Be selective about which files to include
- Use file paths, not entire directories
- Focus on relevant files

#### Context Strategies

**Strategy 1: Minimal Context**
- Only include directly relevant files
- Use for simple tasks

**Strategy 2: Related Context**
- Include related files
- Use for multi-file changes

**Strategy 3: Full Codebase**
- Let Cursor index entire codebase
- Use for architecture questions

### 3. Codebase Understanding

#### Understanding Large Codebases

**Step 1: Get Overview**
```
Give me an overview of this codebase:
- Main components
- Architecture
- Key files
- Entry points
```

**Step 2: Understand Flow**
```
Trace the flow of [process] from start to finish
```

**Step 3: Find Dependencies**
```
Show me all files that depend on @core_module.py
```

**Step 4: Understand Patterns**
```
What patterns are used in this codebase?
```

### 4. Performance Optimization

#### Cursor Performance Tips

**1. Limit Context:**
- Don't include entire codebase unnecessarily
- Use selective file mentions

**2. Indexing Settings:**
- Adjust indexing depth
- Exclude unnecessary files/folders

**3. Model Selection:**
- Use faster models for simple tasks
- Use powerful models for complex tasks

**4. Extension Management:**
- Disable unused extensions
- Keep extensions updated

**5. File Watching:**
- Exclude large directories from file watching
- Use `.cursorignore` file

#### Creating .cursorignore

Create `.cursorignore` in project root:

```
# Exclude from indexing
node_modules/
venv/
__pycache__/
*.pyc
.env
dist/
build/
```

### 5. Team Collaboration

#### Sharing Settings

**Settings Sync:**
- Sign in to sync settings
- Settings → Sync → Enable

**Team Rules:**
- Share `.cursorrules` file
- Commit to version control
- Keep team-aligned

#### Code Review with Cursor

**Review PRs:**
```
Review this pull request:
- Check for bugs
- Verify best practices
- Suggest improvements
```

**Generate Review Comments:**
```
Generate code review comments for these changes
```

---

## Troubleshooting and Optimization

### Common Issues and Solutions

#### Issue 1: AI Not Responding

**Symptoms:**
- Chat doesn't respond
- Composer doesn't work
- Inline suggestions missing

**Solutions:**
1. **Check Internet Connection:**
   - AI requires internet (unless using local model)
   - Verify connection

2. **Check API Limits:**
   - Free tier has limits
   - Upgrade if needed

3. **Restart Cursor:**
   - Quit and reopen
   - Clear cache if needed

4. **Check Model Selection:**
   - Verify model is selected
   - Try different model

#### Issue 2: Slow Performance

**Symptoms:**
- Slow responses
- Laggy interface
- High memory usage

**Solutions:**
1. **Reduce Context:**
   - Don't include entire codebase
   - Be selective with `@` mentions

2. **Disable Unused Extensions:**
   - Extensions panel
   - Disable unnecessary extensions

3. **Optimize Indexing:**
   - Reduce indexing depth
   - Exclude large directories

4. **Close Unused Files:**
   - Close tabs you're not using
   - Limit open editors

5. **Restart Cursor:**
   - Sometimes restart helps
   - Clear cache if persistent

#### Issue 3: Code Suggestions Incorrect

**Symptoms:**
- AI suggests wrong code
- Suggestions don't match style
- Context misunderstood

**Solutions:**
1. **Improve Context:**
   - Add more relevant files
   - Provide better descriptions

2. **Update .cursorrules:**
   - Add specific rules
   - Clarify coding standards

3. **Be More Specific:**
   - Provide detailed requirements
   - Give examples

4. **Use Different Model:**
   - Try Claude vs GPT-4
   - Different models for different tasks

#### Issue 4: Git Integration Issues

**Symptoms:**
- Git not working
- Changes not detected
- Merge conflicts

**Solutions:**
1. **Check Git Installation:**
   ```bash
   git --version
   ```

2. **Verify Repository:**
   - Ensure you're in a git repo
   - Check `.git` folder exists

3. **Refresh Source Control:**
   - Reload window: `Cmd+R` (Mac) or `Ctrl+R` (Windows)
   - Or restart Cursor

4. **Check Git Config:**
   ```bash
   git config --list
   ```

#### Issue 5: Extension Conflicts

**Symptoms:**
- Features not working
- Errors in console
- Performance issues

**Solutions:**
1. **Disable Extensions:**
   - One by one to find conflict
   - Disable recently installed

2. **Update Extensions:**
   - Keep extensions updated
   - Check for compatibility

3. **Check Extension Settings:**
   - Review extension configuration
   - Reset to defaults if needed

### Performance Optimization

#### Memory Management

**Monitor Memory:**
- Activity Monitor (Mac) or Task Manager (Windows)
- Check Cursor memory usage

**Reduce Memory:**
- Close unused files
- Disable heavy extensions
- Reduce indexing scope
- Limit open terminals

#### Indexing Optimization

**Configure Indexing:**
```json
{
  "cursor.indexing.enabled": true,
  "cursor.indexing.depth": 3,
  "cursor.indexing.exclude": [
    "**/node_modules/**",
    "**/venv/**",
    "**/__pycache__/**"
  ]
}
```

#### File Watching Optimization

**Exclude Patterns:**
- Large directories
- Build outputs
- Dependencies
- Cache folders

---

## Real-World Projects

### Project 1: Building a Payroll Calculation Feature

**Scenario:** Add new payroll calculation feature to Avocado platform.

#### Step 1: Understand Requirements
```
@requirements.md Explain what needs to be built for the new payroll calculation feature
```

#### Step 2: Explore Existing Code
```
@payroll_calculator.py @tax_engine.py How does the current payroll calculation work?
```

#### Step 3: Plan Implementation
```
Create an implementation plan for adding overtime calculation:
- Which files need changes
- What new functions are needed
- How to integrate with existing code
- What tests are required
```

#### Step 4: Implement with Composer
```
Implement overtime calculation feature:
- Add calculate_overtime() function
- Update payroll processing workflow
- Add validation for hours > 40
- Include tests
- Update documentation
```

#### Step 5: Review and Test
- Review generated code
- Run existing tests
- Add new tests
- Fix any issues

### Project 2: Refactoring Legacy Tax Code

**Scenario:** Modernize old tax calculation code.

#### Step 1: Analyze Current Code
```
@legacy_tax_code.py Analyze this code and identify:
- Code smells
- Performance issues
- Security concerns
- Areas for improvement
```

#### Step 2: Create Refactoring Plan
```
Create a refactoring plan:
- Modernize to Python 3.11+ features
- Add type hints
- Improve error handling
- Add comprehensive tests
- Maintain backward compatibility
```

#### Step 3: Execute Refactoring
```
Refactor according to plan:
- Use modern Python features
- Add type hints throughout
- Implement proper error handling
- Add logging
- Create comprehensive tests
```

#### Step 4: Verify
- Run all tests
- Check functionality
- Performance testing
- Code review

### Project 3: Adding API Endpoints

**Scenario:** Add new REST API endpoints for payroll operations.

#### Step 1: Understand API Structure
```
@api_routes.py @models.py Explain the current API structure
```

#### Step 2: Design Endpoints
```
Design new endpoints for:
- GET /api/payroll/runs - List payroll runs
- POST /api/payroll/runs - Create payroll run
- GET /api/payroll/runs/{id} - Get specific run

Include:
- Request/response schemas
- Error handling
- Authentication
- Validation
```

#### Step 3: Implement
```
Implement the new API endpoints:
- Create route handlers
- Add request validation
- Implement business logic
- Add error handling
- Create response models
- Add authentication
- Write tests
```

#### Step 4: Document
```
Generate API documentation for the new endpoints:
- Endpoint descriptions
- Request/response examples
- Error codes
- Authentication requirements
```

---

## Resources and Next Steps

### Official Resources

- **Cursor Website:** https://cursor.sh
- **Cursor Documentation:** https://docs.cursor.com
- **Cursor Blog:** https://cursor.sh/blog
- **Cursor Discord:** Community support
- **Cursor GitHub:** https://github.com/getcursor/cursor

### Learning Path

**Week 1: Basics**
- Install and configure Cursor
- Learn basic navigation
- Master chat functionality
- Practice inline suggestions

**Week 2: Intermediate**
- Master Composer
- Learn codebase indexing
- Practice refactoring
- Use code review features

**Week 3: Advanced**
- Agent mode
- Custom rules
- Multi-file workflows
- Performance optimization

**Week 4: Mastery**
- Complex projects
- Team collaboration
- Custom workflows
- Expert techniques

### Practice Projects

1. **Simple Feature:** Add a function to existing codebase
2. **Refactoring:** Modernize legacy code
3. **API Development:** Build REST API endpoints
4. **Testing:** Create comprehensive test suite
5. **Documentation:** Generate project documentation

### Next Steps

1. **Complete Basics:** Master core features
2. **Practice Daily:** Use Cursor for all coding
3. **Explore Advanced:** Try Agent mode and custom rules
4. **Share Knowledge:** Help team members learn
5. **Stay Updated:** Follow Cursor updates and new features

---

## Conclusion

Cursor IDE represents the future of AI-powered development. By mastering Cursor, you can:

- **Code 10× Faster:** AI assistance accelerates development
- **Write Better Code:** AI suggestions improve quality
- **Understand Codebases:** AI helps navigate complex projects
- **Reduce Errors:** AI catches issues early
- **Learn Continuously:** AI explains and teaches

### Key Takeaways

1. **Start Simple:** Master basics before advanced features
2. **Use Context:** Provide good context for better results
3. **Iterate:** Review and refine AI suggestions
4. **Practice:** Use Cursor for all coding tasks
5. **Customize:** Set up rules and preferences for your workflow

### Mastery Checklist

By completing this tutorial, you should be able to:

- [ ] Install and configure Cursor on any platform
- [ ] Navigate interface efficiently
- [ ] Use Chat for code questions and generation
- [ ] Master Composer for multi-file editing
- [ ] Use inline suggestions effectively
- [ ] Configure custom rules
- [ ] Use Agent mode for complex tasks
- [ ] Optimize performance
- [ ] Troubleshoot common issues
- [ ] Build complete features with AI assistance

**Start using Cursor today and transform your development workflow!**

---

**Happy coding with Cursor! 🚀**

*This tutorial covers Cursor IDE comprehensively. For the latest features and updates, visit [cursor.sh](https://cursor.sh) and [docs.cursor.com](https://docs.cursor.com).*

