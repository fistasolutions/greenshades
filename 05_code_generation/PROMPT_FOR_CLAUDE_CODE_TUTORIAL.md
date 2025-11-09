# World-Class Prompt: Transform Claude Code Tutorial into Expert-Level Mastery Guide

## Your Role
You are a world-class instructional designer and technical educator specializing in AI-powered development tools. You have deep expertise in Claude Code, software engineering best practices, and creating comprehensive, expert-level tutorials that transform beginners into masters.

## Your Task
Transform the existing Claude Code tutorial into a world-class, comprehensive mastery guide that incorporates ALL content from the official Claude Code course lessons (L0-L8) while maintaining and enhancing the existing structure. The tutorial must be:

1. **Comprehensive**: Cover every feature, command, workflow, and technique from all lessons
2. **Expert-Level**: Go beyond basics to advanced mastery techniques
3. **Pedagogically Sound**: Use world-class teaching methods (progressive disclosure, examples, practice exercises)
4. **Practical**: Include real-world prompts, code examples, and workflows
5. **Well-Organized**: Logical flow from basics to advanced mastery

## Source Material to Incorporate

### Lesson 0: Course Introduction
- Course format and structure
- Prerequisites (Python, Next.js, terminal, git)
- Cost visibility and subscription options
- Course codebase examples (RAG chatbot, e-commerce analysis, Figma mockup)
- Resources and links

### Lesson 1: Installing Claude Code
- System requirements (Node.js 18+, Windows options)
- Installation command: `npm install -g @anthropic-ai/claude-code`
- Troubleshooting guide links
- Launching from terminal and VS Code
- IDE integrations

### Lesson 2: Setup & Codebase Understanding
- `/init` command and CLAUDE.md file creation
- `#` command for quick memory additions
- Context management commands (`/clear`, `/compact`, ESC, ESC ESC)
- Bash commands with `!` prefix
- Codebase exploration prompts (overview, data models, document processing, query flow, chunking, API endpoints)
- Sample prompts for understanding codebases

### Lesson 3: Adding Features
- Using `@` to mention files
- Plan mode vs auto-accept mode (`shift`+`tab`)
- Screenshot shortcuts and pasting
- MCP server integration (`/mcp` command)
- Playwright MCP server setup and usage
- Feature implementation prompts (embedding links, new chat button, adding tools)
- Custom slash commands setup

### Lesson 4: Testing, Error Debugging, Code Refactoring
- Extended thinking mode ("think", "think hard", "think harder", "ultrathink")
- Subagents for complex tasks
- Custom subagents (mentioned but not detailed)
- Testing framework creation
- Error debugging workflows
- Code refactoring for sequential tool calling
- Test-driven development with Claude Code

### Lesson 5: Adding Multiple Features Simultaneously
- Git worktrees workflow
- Custom slash commands (`.claude/commands/` folder)
- Parallel feature development
- Merging worktrees
- Feature implementation examples (UI features, testing, quality tools)

### Lesson 6: GitHub Integration & Hooks
- GitHub Actions integration (`/install-github-app`)
- Mentioning `@claude` in PRs and issues
- Hooks system (before/after tool execution, subagent completion, response completion)
- Hook examples and use cases

### Lesson 7: Refactoring Jupyter Notebooks & Creating Dashboards
- Notebook refactoring workflows
- Structure improvements
- Code quality enhancements
- Converting notebooks to Streamlit dashboards
- Data analysis workflows

### Lesson 8: Creating Web Apps from Figma Mockups
- Figma Dev Mode MCP server setup
- Figma MCP server configuration
- Alternative Framelink Figma MCP server
- Playwright integration for visual verification
- Next.js app generation from designs
- Real-world data integration (FRED API example)

## Transformation Requirements

### 1. Structure Enhancement
- Maintain existing table of contents but expand with lesson-specific sections
- Add "Getting Started" section with installation and setup
- Add "Core Commands Reference" section
- Add "Advanced Workflows" section covering all lessons
- Add "Real-World Projects" section with all three course examples
- Add "Expert Techniques" section for mastery-level content

### 2. Content Integration
- **Installation & Setup**: Detailed installation guide from L1
- **Project Initialization**: `/init` command and CLAUDE.md from L2
- **Context Management**: All commands from L2 (`/clear`, `/compact`, ESC, etc.)
- **File Referencing**: `@` syntax and file mentions from L3
- **MCP Integration**: Complete MCP server guide from L3, L6, L8
- **Planning Mode**: Plan vs auto-accept from L3
- **Screenshots**: Shortcuts and usage from L3
- **Testing & Debugging**: Complete workflows from L4
- **Extended Thinking**: All thinking modes from L4
- **Subagents**: Usage and customization from L4
- **Git Worktrees**: Complete workflow from L5
- **Custom Commands**: Setup and examples from L5
- **GitHub Integration**: Complete setup from L6
- **Hooks**: System and examples from L6
- **Notebook Refactoring**: Complete workflow from L7
- **Dashboard Creation**: Streamlit conversion from L7
- **Figma Integration**: Complete setup and usage from L8

### 3. Prompt Examples
Include ALL real prompts from lessons:
- Codebase exploration prompts (L2)
- Feature implementation prompts (L3)
- Testing prompts (L4)
- Refactoring prompts (L4, L7)
- Multi-feature prompts (L5)
- Dashboard conversion prompts (L7)
- Figma-to-code prompts (L8)

### 4. Teaching Methodology
- **Progressive Disclosure**: Start simple, build complexity
- **Examples First**: Show before explaining
- **Practice Exercises**: Include hands-on activities
- **Real-World Context**: Use actual project examples
- **Troubleshooting**: Common issues and solutions
- **Best Practices**: Expert tips throughout
- **Visual Aids**: Code blocks, diagrams, flowcharts where helpful

### 5. Expert-Level Enhancements
- Advanced MCP server configurations
- Custom subagent creation
- Complex workflow orchestration
- Performance optimization techniques
- Security best practices
- Integration patterns
- Troubleshooting advanced issues

## Output Requirements

### Must Include:
1. ✅ Complete installation guide (L1)
2. ✅ All commands with examples (L2, L3, L4, L5, L6)
3. ✅ All workflows from lessons (L2-L8)
4. ✅ All real prompts from lessons
5. ✅ MCP server setup for Playwright, Figma, GitHub
6. ✅ Git worktrees workflow
7. ✅ Custom commands setup
8. ✅ Hooks system
9. ✅ Extended thinking modes
10. ✅ Subagents usage
11. ✅ Three complete project examples (RAG chatbot, e-commerce, Figma app)
12. ✅ Troubleshooting sections
13. ✅ Best practices throughout
14. ✅ Expert tips and advanced techniques

### Quality Standards:
- **Clarity**: Every concept explained clearly
- **Completeness**: Nothing from lessons is missing
- **Practicality**: All examples are actionable
- **Expertise**: Goes beyond basics to mastery
- **Organization**: Logical flow and easy navigation
- **Engagement**: Keeps readers motivated and learning

## Transformation Process

1. **Preserve Existing Content**: Keep all good content from current tutorial
2. **Integrate Lesson Content**: Add all content from L0-L8 systematically
3. **Enhance with Examples**: Add more real-world examples
4. **Add Practice Exercises**: Include hands-on activities
5. **Improve Organization**: Better structure and flow
6. **Add Expert Sections**: Advanced techniques and mastery content
7. **Enhance Troubleshooting**: More comprehensive problem-solving
8. **Add Visual Elements**: Better formatting, code blocks, diagrams

## Success Criteria

The transformed tutorial should:
- ✅ Be the most comprehensive Claude Code tutorial available
- ✅ Cover every feature and command from the official course
- ✅ Include all real prompts and examples from lessons
- ✅ Enable readers to achieve expert-level mastery
- ✅ Be pedagogically sound and easy to follow
- ✅ Include practical exercises and real-world projects
- ✅ Be well-organized and easy to navigate
- ✅ Go beyond the course content with expert insights

## Begin Transformation

Now transform the Claude Code tutorial file, incorporating all lesson content while maintaining and enhancing the existing structure. Create a world-class, expert-level mastery guide that teaches Claude Code from installation to advanced mastery.

