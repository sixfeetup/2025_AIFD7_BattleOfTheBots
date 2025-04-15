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

# Battle of the Bots: Which AI Assistant Delivers? {.semi-filtered data-background-image="images/abstract.jpg"}
#### Calvin Hendryx-Parker, CTO
#### Six Feet Up

::::::::::::::{.credits}
<a style="background-color:black;color:white;text-decoration:none;padding:4px 6px;font-family:-apple-system, BlinkMacSystemFont, &quot;San Francisco&quot;, &quot;Helvetica Neue&quot;, Helvetica, Ubuntu, Roboto, Noto, &quot;Segoe UI&quot;, Arial, sans-serif;font-size:12px;font-weight:bold;line-height:1.2;display:inline-block;border-radius:3px" href="https://unsplash.com/@davidclode?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge" target="_blank" rel="noopener noreferrer" title="Download free do whatever you want high-resolution photos from David Clode"><span style="display:inline-block;padding:2px 3px"><svg xmlns="http://www.w3.org/2000/svg" style="height:12px;width:auto;position:relative;vertical-align:middle;top:-2px;fill:white" viewBox="0 0 32 32"><title>unsplash-logo</title><path d="M10 9V0h12v9H10zm12 5h10v18H0V14h10v9h12v-9z"></path></svg></span><span style="display:inline-block;padding:2px 3px">David Clode</span></a>
::::::::::::::

::: notes
Example Notes
:::


# AI Coding Assistants: The New Pair-Programming Partners

Rapid Evolution over the last year:

- Claude Code: Anthropic's CLI tool with advanced context awareness and precise refactoring
  capabilities
- Aider: Git-integrated assistant that understands entire codebases and can commit changes
- Goose: Specialized in API development with strong documentation capabilities
- Cursor: Editor-integrated solution enabling real-time collaborative coding and debugging

From basic code completion to full-fledged pair programmers in just one year

---

# Tool introduction: Claude Code

- Developed by [Anthropic](https://www.anthropic.com/claude)
- Proprietary model and tooling
- Uses only Claude models (Claude 3 Opus/Sonnet/Haiku)
- Fully agentic with reasoning capabilities
- Supports MCP (Multi-Context Prompting)

---

# Tool introduction: Aider

- Developed by Paul Gauthier
- Open-source ([GitHub: paul-gauthier/aider](https://github.com/paul-gauthier/aider))
- Supports multiple LLM models (OpenAI GPT-4, Claude, Llama)
- Semi-agentic with git integration
- No MCP support currently

---

# Tool introduction: Goose

- Developed by Block Inc. (formerly Square)
- Open-source ([GitHub: block/goose](https://github.com/block/goose))
- Supports multiple LLM models (OpenAI, Claude, Ollama)
- Fully agentic with integrated tooling
- Supports MCP: https://block.github.io/goose/docs/getting-started/using-extensions#mcp-servers
- Supports OpenRouter! (openrouter.ai)

---

# Tool introduction: Cursor

- Developed by Cursor team (acquired by Anthropic)
- Proprietary editor with open-source components
- Supports both OpenAI and Anthropic models
- Fully agentic with project navigation
- Supports MCP: https://docs.cursor.com/context/model-context-protocol

---

# What is AI Agent?

An AI agent is a system that can:

- Perceive its environment through tools/APIs
- Make decisions autonomously
- Take actions to achieve specific goals
- Learn from interactions and feedback
- Chain multiple operations together

Key characteristics:

- Tool use capabilities (file system, web search, code execution)
- Planning and reasoning about complex tasks
- Persistent memory within a session
- Self-improvement through feedback loops

---

# What is MCP?

The Model Context Protocol is an open standard that enables developers to build
secure, two-way connections between their data sources and AI-powered tools. The
architecture is straightforward: developers can either expose their data through
MCP servers or build AI applications (MCP clients) that connect to these
servers.

---

# MCP Example: AWS API

- A suite of specialized MCP servers that help you get the most out of AWS:
  https://github.com/awslabs/mcp
- Saves the cost of having all the AWS docs in your own context
- In practice:
  - Connect your AI assistant to AWS MCP servers
  - Ask natural language questions about AWS services
  - Get contextually accurate answers based on latest documentation
  - Generate AWS CLI commands, CloudFormation templates, or IAM policies
  - Troubleshoot AWS-specific issues with current best practices

---

# DEMO: The prompt

This project was bootstrapped with scaf and has a NextJS frontend in the
`frontend` dir and a Django backend in the `backend` dir.

The scaf template only supports a GraphQL API. Refactor the app to use a REST
API.

---

# DEMO: Claude Code

- Allow tools: `claude config add allowedTools "Bash(git:*),Bash(cat:*),Bash(grep:*)"`
- Specify conventions in CLAUDE.md
- Doesn't use git to commit changes. TIP: Ask it to "Review the staged changes
  with `git diff --staged` and git commit using conventional commit standard"
- Show cost with `/cost`
- Compact and clear context with `/compact` and `/clear`

# DEMO: Aider

- Specify conventions in CONVENTIONS.md
- Use different models for architect and edit mode simultaneously
- Use external editor with `/editor`
- Run commands and add to output with `/run`
- Show cost with `/tokens`
- Clear context with `/clear`
- Start with `--lint-command` and `--test-command` run your test suite after
  each time the AI edits your code

# DEMO: Goose

- Specify conventions in .goosehints:
  Global: ~/.config/goose/.goosehints
  Local: .goosehints
- Session support:
  Start a session: `goose session -n rest-api`
  Exit a session: type exit
  Resume session: `goose session -r rest-api`
- Permission Modes:
  Completely Autonomous / Manual Approval / Smart Approval / Chat Only
- Clear context by exiting `/exit`

# DEMO: Cursor

- Specify conventions in Cursor Rules: ./cursor/rules
  https://docs.cursor.com/context/rules-for-ai
- Always start by asking what model you are using.
