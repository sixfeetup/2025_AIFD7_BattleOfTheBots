\
---\
title: Agentic AI and the MCP Ecosystem\
description: A 101 introduction to AI Agents\
authors: \
    - angie\
---\
\
![blog banner](agentic-ai-with-mcp.png)\
\
It seems like yesterday when we all were wowed by generative AI and specifically the chat interfaces that made interacting with large language models (LLMs) accessible to everyday people.\
\
As amazing as this was, it was only the beginning. The next wave of AI is agentic, meaning AI systems that don't just respond to prompts but take actions, make decisions, and interact with external systems. This is accomplished via **AI agents**.\
\
<!--truncate-->\
\
## What are AI Agents?\
\
When you interact with chatbots that use AI, like ChatGPT, you can ask it how to do something, and it'll provide step-by-step instructions.\
\
For example, if I ran into an error while coding, I could paste the error message into ChatGPT and ask it to help me debug. Because ChatGPT doesn't have access to my codebase, it would speculate on the cause of my error and give me a couple of possible solutions to try. I'd then manually try these proposed solutions and return to inform ChatGPT of the results. We'd continue this back and forth until the error is resolved or I give up.\
\
AI Agents greatly simplify this flow by talking with the LLM on my behalf and taking direct action to fix the problem.\
\
> _**An AI agent is a system that operates autonomously to accomplish a goal.**_\
\
Because AI agents are connected to systems, they can analyze a situation, determine the next action, and execute it without much, if any, human intervention. This capability turns them from passive chatbots into automation assistants.\
\
By using an AI agent, I can simply say \\\"fix the error\\\" and it'll have context about what's wrong and automatically fix the error for me.\
\
## How AI Agents Work with LLMs\
\
LLMs (e.g. GPT-4o, Claude 3.5 Sonnet, Gemini 2.0, etc) provide cognitive abilities to AI agents. Most AI agents will have a chat interface themselves where you type your prompt, and the agent will send this prompt to an LLM. At the same time, the agent will also inform the LLM of what **tools** it has access to.\
\
### Tool Calling\
\
Tools are one of the most important aspects of agentic AI. AI agents are able to execute API calls via **tool calling**.\
\
Let's look at an example:\
\
1. A user sends a prompt to their AI agent: _\\\"Fix the NullPointerException in my UserService.java file.\\\"_\
\
2. The agent sends the user request and the list of its available tools to the LLM in a structured format.\
