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
- **Hooks**: Events (SessionStart/End, Pre/PostToolUse, Stop/SubagentStop, PreCompact, UserPromptSubmit); per-command timeouts; systemMessage support
- **MCP**: @‑mention toggles, multi‑config files, import from Claude Desktop, OAuth discovery, SSE/HTTP w/ OAuth, enterprise allow/deny lists
- **UI/UX**: Smoother terminal, better permission prompts, redesigned search, drag‑and‑drop, transcript shows model, `/export`

::: notes
- MCP support isn’t new (added in 2024); the recent changes are usability and enterprise enhancements
- Hooks docs: https://docs.claude.com/en/docs/claude-code/hooks
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
- Supports [MCP](https://cursor.com/docs/context/mcp)

---

# What's New in Cursor {.r-fit-text data-background="images/1.png"}

- **Background Agents**: Continuous VMs, GitHub/IAM, dashboards
- **Modes**: Agent, Ask, Plan, Custom; reviewable plans
- **Rules**: Project/Team rules (.cursor/rules), AGENTS.md, /Generate Cursor Rules
- **Headless/CI**: Headless CLI; GitHub Actions
- **MCP**: Client + Extension API; directory/install
- **Browser**: Built-in web tool
- **Enterprise**: Admin API, Analytics v2, SSO/SCIM, spend controls
- **Models/Max**: Max‑Mode for long‑running work

::: notes
- Background Agents: docs, API, webhooks — https://cursor.com/docs/background-agent | https://cursor.com/docs/background-agent/api/overview | https://cursor.com/docs/background-agent/api/webhooks
- Modes & Rules: https://cursor.com/docs/agent/modes | https://cursor.com/docs/context/rules
- Headless/CI & MCP: https://cursor.com/docs/cli/headless | https://cursor.com/docs/cli/github-actions | https://cursor.com/docs/context/mcp | https://cursor.com/docs/context/mcp-extension-api | https://cursor.com/docs/context/mcp/directory | https://cursor.com/docs/context/mcp/install-links
- Browser: https://cursor.com/docs/agent/browser
- Enterprise, Models & Changelog: https://cursor.com/docs/enterprise | https://cursor.com/docs/account/teams/admin-api | https://cursor.com/docs/account/teams/analytics-v2 | https://cursor.com/docs/enterprise/usage-and-spend-controls | https://cursor.com/docs/enterprise/model-and-integration-management | https://cursor.com/docs/account/teams/sso | https://cursor.com/docs/account/teams/scim | https://cursor.com/docs/context/max-mode | https://cursor.com/docs/models | https://www.cursor.com/changelog
:::

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

- **Recipes**: Repeatable workflows; cookbook generator
- **Subagents/Subrecipes (experimental)**: Parallel and structured delegation
- **MCP‑UI (early)**: Intent‑based UIs; auto visualizer
- **Containers (via MCP server)**: Dagger/container‑use integration for isolated envs
- **Multi‑model (Lead/Worker)**: Planner/worker orchestration; per‑task routing
- **Providers**: OpenRouter + Tetrate Agent Router
- **ACP**: Agent‑Client‑Protocol editor integration

::: notes
- Multi‑model (Lead/Worker): https://block.github.io/goose/docs/tutorials/lead-worker | https://block.github.io/goose/blog/2025/06/16/multi-model-in-goose
- Recipes + Containers: https://block.github.io/goose/blog/2025/05/06/recipe-for-success | https://block.github.io/goose/blog/2025/06/19/isolated-development-environments
- Subagents/Subrecipes (experimental) + MCP‑UI: https://block.github.io/goose/blog/2025/09/26/subagents-vs-subrecipes | https://block.github.io/goose/blog/2025/09/15/subrecipes-in-goose | https://block.github.io/goose/blog/2025/08/27/autovisualiser-with-mcp-ui
- Providers (OpenRouter/Tetrate) + ACP: https://block.github.io/goose/blog/2025/07/29/openrouter-unlocks-workshops | https://block.github.io/goose/blog/2025/08/27/get-started-for-free-with-tetrate | https://block.github.io/goose/blog/2025/10/24/intro-to-agent-client-protocol-acp
:::

---

# Tool introduction: Junie {.r-fit-text data-background="images/3.png"}

- Developed by [JetBrains](https://plugins.jetbrains.com/plugin/26104-jetbrains-junie-eap)
- Requires a JetBrains IDE + JetBrains AI plan (AI Pro/Ultimate); EAP plugin on Marketplace
- Models: GPT-5 default; Claude also supported
- Fully agentic with project navigation

::: notes
- As of Aug 7, 2025, GPT-5 is the default model for Junie (configurable); source below in What's New notes
:::

---

# What's New in Junie {.r-fit-text data-background="images/3.png"}

- **Status**: Public EAP; plugin available on Marketplace
- **Models**: GPT-5 default in Junie; Claude also supported
- **MCP**: Model Context Protocol support (in-IDE)
- **Remote Dev**: macOS & Linux (Windows not yet)
- **GitHub EAP**: Async multi-tasking from GitHub; JVM + PHP projects only (for GitHub EAP)
- **Performance/UX**: ~30% faster in-IDE; transparent plan/log; Ask mode; Brave mode; guidelines file
- **Grants**: 6‑month licenses for open-source projects (Junie on GitHub)

::: notes
- GPT‑5 default + how to try: https://blog.jetbrains.com/blog/2025/08/07/gpt-5-support-in-ai-assistant-junie-kineto/
- Agentic era (MCP, Remote Dev macOS/Linux, 30% faster, GitHub EAP JVM/PHP, grants): https://blog.jetbrains.com/junie/2025/07/the-agentic-ai-era-at-jetbrains-is-here/
- PhpStorm deep dive (guidelines, Ask mode, Brave mode, allowlist): https://blog.jetbrains.com/phpstorm/2025/06/discover-junie-for-phpstorm/
- Junie main page / plugin: https://www.jetbrains.com/junie/ | https://plugins.jetbrains.com/plugin/26104-jetbrains-junie-eap
:::

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

- Specify conventions in Project Rules: .cursor/rules
  https://cursor.com/docs/context/rules
- Optionally add AGENTS.md at the project root or subdirectories; you can also generate rules via /Generate Cursor Rules
 

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
