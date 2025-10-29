---
title-prefix: Six Feet Up
pagetitle: "Battle of the Bots: Which AI Assistant Delivers?"
author: Calvin Hendryx-Parker, CTO, Six Feet Up
author-meta:
    - Calvin Hendryx-Parker
date: IndyPy 2025
date-meta: 2025
keywords:
    - Python
    - AI
    - Agents
    - Code
---

# Battle of the Bots: {.r-fit-text data-background="images/1.png"}
## Which AI Assistant Delivers?
#### Calvin Hendryx-Parker, CTO
#### Six Feet Up

---

# AI Coding Assistants {.r-fit-text data-background="images/2.png"}
## The New Pair-Programming Partners {.r-fit-text}

### Rapid Evolution over the last year:

> More than 97% of respondents reported having used AI coding tools at work
>
> -- [Github AI in Software Survey](More than 97% of respondents reported having used AI coding tools at work at some point)

---

# Why This Matters {.r-fit-text data-background="images/9.png"}

- AI coding assistants are transforming how we build software
- Choosing the right tool can mean the difference between frustration and flow
- Let’s find out which one delivers for real-world developers!

---

# The Contenders {data-background="images/3.png"}

- Aider
- Claude Code
- Cursor
- Goose
- Junie
- OpenAI Codex


::: notes
- Aider: Git-integrated assistant that understands entire codebases and can commit changes
- Claude Code: Anthropic's CLI tool with advanced context awareness and precise refactoring capabilities
- Cursor: Editor-integrated solution enabling real-time collaborative coding and debugging
- Goose: Specialized in API development with strong documentation capabilities
- Junie: JetBrain's new agentic assistant that is current in private beta
- OpenAI Codex: OpenAI’s agentic coding suite with an open-source CLI and IDE extensions
 
 From basic code completion to full-fledged pair programmers in just one year
:::

---

# What is AI Agent? {data-background="images/4.png"}

An AI agent is a system that can:

- Perceive its environment through tools/APIs
- Make decisions autonomously
- Take actions to achieve specific goals
- Learn from interactions and feedback
- Chain multiple operations together

---

# Agents Continued {data-background="images/4.png"}

Key characteristics:

- Tool use capabilities (file system, web search, code execution)
- Planning and reasoning about complex tasks
- Persistent memory within a session
- Self-improvement through feedback loops

---

# What is MCP? {data-background="images/6.png"}

![](images/Model%20Context%20Protocol%20Diagram.png){.r-stretch .r-frame .r-center}

::: notes
The Model Context Protocol is an open standard that enables developers to build
secure, two-way connections between their data sources and AI-powered tools. The
architecture is straightforward: developers can either expose their data through
MCP servers or build AI applications (MCP clients) that connect to these
servers.
:::

---

# MCP Examples {data-background="images/8.png"}

- A [suite of specialized MCP servers](https://github.com/awslabs/mcp) for AWS:
  - Saves the cost of having all the AWS docs in your own context
- Use [Playwright from your AI Tools](https://github.com/microsoft/playwright-mcp)
  - Control a browser and grab the context from various web pages
 
---

# In practice {data-background="images/8.png"}

- Connect your AI assistant to AWS MCP servers
- Ask natural language questions about AWS services
- Get contextually accurate answers based on latest documentation
- Generate AWS CLI commands, CloudFormation templates, or IAM policies
- Troubleshoot AWS-specific issues with current best practices

---

# Tool introduction: Aider {.r-fit-text data-background="images/9.png"}

- Developed by Paul Gauthier
- Open-source ([GitHub: paul-gauthier/aider](https://github.com/paul-gauthier/aider))
- Supports multiple LLM models (OpenAI, Claude, Llama, BYOM)
- Semi-agentic with git integration
- No MCP support currently
- Supports `/voice` interactions
- Use Multiple Models in the same session

---

# What's New in Aider {.r-fit-text data-background="images/9.png"}

- Models: GPT‑5; Claude Sonnet 4/Opus 4; Gemini 2.5; Grok‑4; DeepSeek V3/R1; Responses API (o1/o3/o4‑mini)
- Reasoning: `/think‑tokens` and `/reasoning‑effort`; thinking tokens support and cleaner reasoning output
- OpenRouter: OAuth sign‑in, smarter defaults, local model metadata cache, accurate pricing
- UX/CLI: `/context`, `/editor` (alias `/edit`), shell completions, desktop notifications, faster launch/spinners
- Git: Conventional Commits prompting, Co‑authored‑by by default, `--commit‑language`, clearer `/undo`
- Repo & languages: +130 languages; repo‑map for Scala/OCaml/MATLAB/Clojure; better identifier ranking
- Watcher & web: more robust file watcher (permissions/filters/Lisp comments); optional Playwright scraping

::: notes
Architect mode, IDE file watcher and the browser UI were already available before April 2025.
:::
---

# Tool introduction: Claude Code {.r-fit-text data-background="images/10.png"}

- Developed by [Anthropic](https://www.anthropic.com/claude)
- Proprietary model and tooling
- Uses Claude models: Sonnet 4.5, Opus 4.1, Haiku 4.5 (via Console, Bedrock, Vertex)
- Fully agentic with planning, tools, and subagents
- Supports MCP (Model Context Protocol); MCP support has been in Claude Code since 2024
- Ships as a terminal app and a native VS Code extension

---

# What's New in Claude Code {.r-fit-text data-background="images/10.png"}

- **v2.0**: Native VS Code extension, `/rewind`, `/usage`, thinking toggle, Ctrl‑R history, Agent SDK rename, dynamic subagents
- **Plugins**: Install/enable/disable/marketplace/validate; repo‑level marketplaces; `/doctor` diagnostics
- **Subagents**: Plan and Explore subagents; resume subagents; per‑subagent model selection
- **Models**: Sonnet 4.5 default; Opus 4.1; Haiku 4.5; Sonnet‑plan + Haiku‑execute
- **Bash/Sandbox**: Background long‑running commands; tab completion; BashTool sandbox (macOS/Linux)
- **Skills**: Claude Skills support
- **Hooks**: Hook Events for automation (SessionStart/End, PreToolUse/PostToolUse, Stop/SubagentStop, PreCompact, UserPromptSubmit); per‑command timeouts; systemMessage in outputs
- **MCP**: @‑mention toggles, multi‑config files, import from Claude Desktop, OAuth discovery, SSE/HTTP w/ OAuth, enterprise allow/deny lists
- **UI/UX**: Smoother terminal, better permission prompts, redesigned search, drag‑and‑drop, transcript shows model, `/export`

::: notes
- MCP support isn’t new (added in 2024); the recent changes are usability and enterprise enhancements
- Sources: Claude Code CHANGELOG and docs release notes
  - https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md
  - https://docs.claude.com/en/release-notes/claude-code
:::

---

# Tool introduction: Cursor {.r-fit-text data-background="images/1.png"}

- Developed by Anysphere Inc. (independent company)
- Proprietary editor with open-source components
- Supports OpenAI, Anthropic, and Google models
- Fully agentic with project navigation
- Supports [MCP](https://docs.cursor.com/context/model-context-protocol)

---

# What's New in Cursor {.r-fit-text data-background="images/1.png"}

- **Agent Mode**: Autonomous task planning and execution
- **Composer Mode**: Multi-file coordinated editing
- **Background Agent**: Long-running tasks in background
- **CLI Tools**: Headless operation, GitHub Actions integration
- **Browser Integration**: Web automation capabilities
- **Enhanced MCP Support**: Full Model Context Protocol integration
- **Enterprise Features**: Teams, SSO, SCIM, Admin API, Analytics
- Visit [changelog.cursor.sh](https://changelog.cursor.sh) for detailed updates

---

# Tool introduction: Goose {.r-fit-text data-background="images/2.png"}

- Developed by Block Inc. (formerly Square)
- Open-source ([GitHub: block/goose](https://github.com/block/goose))
- Supports multiple LLM models (OpenAI, Claude, Ollama)
- Fully agentic with integrated tooling
- Supports [MCP](https://block.github.io/goose/docs/getting-started/using-extensions#mcp-servers)
- Supports OpenRouter! (<https://openrouter.ai>)

---

# What's New in Goose {.r-fit-text data-background="images/2.png"}

- **Desktop App**: GUI interface alongside CLI
- **Recipe System**: Repeatable workflow automation (May 2025)
- **Subagents & Subrecipes**: Complex task delegation (Sept 2025)
- **MCP-UI**: Intent-based AI interfaces (Aug 2025)
- **Browser Automation**: "Driver's License" feature (May 2025)
- **Container-use**: Isolated dev environments (June 2025)
- **Multi-Model Support**: Use different models per task
- **OpenRouter Integration**: Access to 100+ models (July 2025)

---

# Tool introduction: Junie {.r-fit-text data-background="images/3.png"}

- Developed by [JetBrains](https://plugins.jetbrains.com/plugin/26104-jetbrains-junie-eap)
- Proprietary tooling and requires PyCharm Subscription
- Appears to be using Anthropic's Claude 3.7 Sonnet
- Fully agentic with project navigation

::: notes
Claims to be using Claude 3 Sonnet, but the discord offical accounts say Sonnet
:::

---

# What's New in Junie {.r-fit-text data-background="images/3.png"}

- **Status Update**: Now in **Public Early Access Program** (was private beta)
- **MCP Support**: Model Context Protocol integration added
- **Remote Development**: macOS & Linux support (not Windows yet)
- **GitHub Integration**: "Junie on GitHub" EAP now open
- **Platform Support**: JVM and PHP projects currently supported
- **Multi-Model**: GPT-5 support mentioned alongside Claude
- **Open Source Grants**: Available for open-source projects

---

# Tool introduction: OpenAI Codex {.r-fit-text data-background="images/7.png"}

- Developed by [OpenAI](https://openai.com/codex/)
- Two parts: open-source CLI (Rust) + IDE extensions (VS Code, Cursor, Windsurf)
- Runs locally and can read/modify/run code in your repo
- Supports MCP via Agents SDK; can be exposed as an MCP server
- Works on macOS/Linux; Windows via WSL2

---

# What's New: OpenAI Codex {.r-fit-text data-background="images/7.png"}

- **Codex CLI**: Local coding agent with TUI; open-source at [openai/codex](https://github.com/openai/codex)
- **Models**: Optimized for **GPT-5-Codex**; switch with `/model` or `--model`
- **Approval Modes**: Auto (default), Read Only, Full Access
- **Non-interactive Mode**: `codex exec "task..."`
- **Images as Input**: `--image` flag or paste into composer
- **Cloud & SDK**: Delegate to Codex Cloud; Agents SDK orchestration; MCP guide
- **Pricing**: Included with ChatGPT Plus/Pro/Team/Edu/Enterprise; or API key

---

# Tool Comparison {.r-fit-text data-background="images/4.png"}

| Tool        | Open Source | MCP Support | Agentic | Models Supported        |
|-------------|-------------|-------------|---------|-------------------------|
| Aider       | Yes         | No          | Semi    | Bring your own          |
| Claude Code | No          | Yes         | Full    | Claude Models           |
| Cursor      | No          | Yes         | Full    | OpenAI, Claude, Gemini  |
| Goose       | Yes         | Yes         | Full    | Bring your own          |
| Junie       | No          | Yes         | Full    | Claude 4.5 + GPT-5      |
| Codex CLI   | Yes         | Yes         | Full    | GPT-5 / GPT-5-Codex     |

---

# Agentic Coding Models {data-background="images/1.png"}

![](images/aider_leaderboar.png)

---

# DEMO: The Prompt {data-background="images/4.png"}

> This project was bootstrapped with scaf and has a NextJS frontend in the `frontend` dir and a Django backend in the `backend` dir.
> 
> The scaf template only supports a GraphQL API. Refactor the app to use a REST API.

---

# DEMO: Aider {data-background="images/5.png"}

- Specify conventions in CONVENTIONS.md
- Use different models for architect and edit mode simultaneously
- Use external editor with `/editor`
- Run commands and add to output with `/run`
- Show cost with `/tokens`
- Clear context with `/clear`
- Start with `--lint-command` and `--test-command` run your test suite after
  each time the AI edits your code
 
# DEMO: Claude Code {data-background="images/6.png"}

- Allow tools: `claude config add allowedTools "Bash(git:*),Bash(cat:*),Bash(grep:*)"`
- Specify conventions in CLAUDE.md
- Doesn't use git to commit changes. TIP: Ask it to "Review the staged changes
  with `git diff --staged` and git commit using conventional commit standard"
- Show cost with `/cost`
- Compact and clear context with `/compact` and `/clear`

# DEMO: Cursor {data-background="images/8.png"}

- Specify conventions in Cursor Rules: ./cursor/rules
  https://docs.cursor.com/context/rules-for-ai
- Ask Cursor to setup a `.cursor-guildeline.json`
 

# DEMO: Goose {data-background="images/9.png"}

- Specify conventions in `.goosehints`:
  Global: `~/.config/goose/.goosehints`
  Local: `.goosehints`
- Session support:
  Start a session: `goose session -n rest-api`
  Exit a session: type exit
  Resume session: `goose session -r rest-api`
- Permission Modes:
  Completely Autonomous / Manual Approval / Smart Approval / Chat Only
- Clear context by exiting `/exit`

# DEMO: Junie {data-background="images/10.png"}

- Specify conventions in `.junie/guidelines.md`
- Use it to help setup those guidelines
- It will require some serious coaxing in complicated setups (like our demo)

---

# Key Takeaways {.r-fit-text data-background="images/3.png"}

- No single assistant is best for every workflow
- MCP is enabling richer, more context-aware coding
- Open source tools are catching up fast
- Try several and see what fits your style!

---

# Talk To Me  {.r-fit-text data-background="images/1.png"}

📩 <calvin@sixfeetup.com>  
🤝 <https://linkedin.com/in/calvinhp>  
🦋 [@calvinhp.com](https://bsky.app/profile/calvinhp.com)  
