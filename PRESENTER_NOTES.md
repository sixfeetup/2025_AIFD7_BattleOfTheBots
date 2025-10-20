# Presenter Notes - Battle of the Bots (Updated Oct 2025)

## 🚨 Critical Corrections to Mention

### 1. Cursor Independence
**OLD CLAIM (INCORRECT):** "Cursor acquired by Anthropic"  
**CORRECT:** Cursor is developed by **Anysphere Inc.** - an independent company  
**Why the confusion?** Cursor *uses* Claude API, but that's a partnership, not ownership

### 2. Claude Code Clarification
**Important:** "Claude Code" is a coding agent tool released by Anthropic  
**What it is:**
- Anthropic-built coding agent experience (CLI/Desktop) powered by Claude models
- Supports **MCP** (Model Context Protocol) for tool integration
- Used directly and also via integrations in third-party tools

---

## ⏱️ Timeline Context

**Your original presentation:** April 2025  
**Today:** October 2025  
**Time elapsed:** ~6 months of rapid AI agent evolution

---

## 🎯 Key Talking Points by Tool

### Aider
**Biggest News:**
- **Architect Mode** - Use smart models (o1) for planning + fast models (GPT-4o) for editing
- **40+ releases** since April - incredibly active development
- Now supports **GPT-5, Claude 4, Grok-3/4, DeepSeek R1**
- **Watch files** - Add AI comments in your editor: `# ... AI!`

**Demo Tip:** Show the multi-model workflow if possible

---

### Claude & MCP
**Biggest News:**
- **MCP launched November 2024** - This is the game-changer
- Open protocol for connecting AI to data sources
- Pre-built servers for Google Drive, Slack, GitHub, etc.
- Being adopted by Zed, Replit, Codeium, Sourcegraph

**Key Point:** MCP is becoming the standard way AI tools connect to external context

**Metaphor:** "Think of MCP as USB-C for AI context - one standard, many implementations"

---

### Cursor
**Biggest News:**
- **Agent Mode** - Can plan and execute multi-step tasks autonomously
- **Composer Mode** - Multi-file coordinated editing (game-changer)
- **CLI Tools** - Can integrate into CI/CD pipelines now
- **Enterprise Features** - Teams, SSO, Admin API

**Important:** Emphasize they're independent and support multiple model providers

**Demo Tip:** If showing Cursor, demonstrate Composer Mode across multiple files

---

### Goose
**Biggest News:**
- **Launched publicly January 2025** - Very recent!
- **Recipe System** (May 2025) - Repeatable workflows
- **Desktop App** - Not just CLI anymore
- **OpenRouter** - Access to 100+ models through one integration
- **MCP-UI** - New approach to agentic interfaces

**Story Arc:** "Goose went from internal Block tool to full public release with major features in < 1 year"

**Demo Tip:** Show recipe system or desktop app if possible

---

### Junie
**Biggest News:**
- **Now Public EAP** (was private beta in April)
- **MCP Support Added** - Following the trend
- **Multi-model** - GPT-5 support alongside Claude
- **GitHub Integration** - Can work with GitHub repos now

**Context:** JetBrains moving fast to compete in the agent space

---

## 📊 Comparison Table - Key Changes

| What Changed | From | To |
|--------------|------|-----|
| Junie MCP Support | ❌ No | ✅ Yes |
| Junie Models | Claude 3.7 only | Claude 3.7 + GPT-5 |
| Cursor Ownership | "Acquired by Anthropic" | Independent (Anysphere) |

---

## 🎤 Opening Remarks Suggestion

> "When I gave this presentation in April 2025, the AI coding assistant landscape was already moving fast. But in the 6 months since, it's been transformative. Today, I'm updating you on what's changed - and trust me, a LOT has changed. 
>
> The biggest development? The Model Context Protocol, or MCP, which Anthropic open-sourced in November 2024. It's becoming the standard way AI agents connect to external tools and data - and almost every tool we're discussing today has adopted it."

---

## 🎤 Closing Remarks Suggestion

> "Since April 2025, we've seen:
> - 40+ releases of Aider with revolutionary features like Architect Mode
> - The birth of MCP as an open standard
> - Goose going from stealth to full public release
> - Junie moving from private beta to public EAP
> - New AI models that are more capable than ever: GPT-5, Claude 4, DeepSeek R1
>
> The pace of innovation is *accelerating*, not slowing down. My advice? Don't get too attached to any one tool. Try several, stay curious, and expect this landscape to look completely different again in another 18 months."

---

## ❓ Anticipated Questions & Answers

### Q: "Which tool should I use?"
**A:** It depends on your workflow:
- **Aider** if you love CLI and want maximum model flexibility
- **Cursor** if you want VS Code familiarity with powerful agent features
- **Goose** if you want enterprise-grade + open source + recipes
- **Junie** if you're already in JetBrains ecosystem
- **Claude + MCP** if you're building your own tool integration

### Q: "Is MCP support essential?"
**A:** It's becoming increasingly important. MCP gives tools access to:
- Your company's internal documentation
- Database schemas
- Cloud resources (AWS, GCP, etc.)
- Design files (Figma)
- Communication tools (Slack)

If you need deep integration with your existing tools, MCP support is a must.

### Q: "Why doesn't Aider support MCP?"
**A:** Aider has chosen a different architectural approach - focusing on git integration and direct model API access. It's a valid choice, and Aider remains highly competitive on benchmarks.

### Q: "Are these tools replacing developers?"
**A:** No. They're making developers more productive. Think "power tools" not "replacement." You still need to:
- Understand the code being generated
- Make architectural decisions
- Review AI output
- Know when the AI is wrong

The best developers are learning to work *with* these tools, not compete against them.

### Q: "What about cost?"
**A:** Varies widely:
- **Aider:** Bring your own API keys (you pay model providers directly)
- **Cursor:** Subscription ($20-40/mo) + some API costs
- **Goose:** Open source (bring your own keys) or hosted
- **Junie:** Requires JetBrains subscription + IDE license
- **Claude:** Pay per use via Anthropic

Budget $50-100/month if using these tools daily.

### Q: "Security concerns?"
**A:** Valid concern. Best practices:
- Use `.gitignore` style ignore files
- Review what code is being sent to APIs
- Consider self-hosted models (Ollama, etc.) for sensitive code
- Use enterprise versions with data governance controls
- Check each tool's privacy policy

---

## 🔥 Hot Takes / Controversial Opinions

### 1. "MCP will win"
MCP is becoming the de facto standard. Tools without it will struggle to compete within 12-24 months.

### 2. "Aider's no-MCP stance is bold"
Aider is betting on simplicity and git integration over ecosystem. Time will tell if this pays off.

### 3. "Cursor's real competition is GitHub Copilot Workspace"
Not the other indie tools - it's GitHub/Microsoft they need to worry about.

### 4. "Goose might be the dark horse"
Block's resources + open source + enterprise credibility = potential to dominate the space.

### 5. "We're still in the 'Cambrian explosion' phase"
This market will consolidate. Not all these tools will exist in 5 years.

---

## 📈 Metrics to Share

- **97%** of developers have used AI coding tools (GitHub survey)
- **40+** Aider releases in 18 months
- **100+** models accessible via OpenRouter in Goose
- **130+** programming languages supported by Aider
- **Nov 2024** - MCP launch date (key milestone)

---

## 🎬 Demo Suggestions

### If demoing live:

**Aider:**
```bash
# Show multi-model architect mode
aider --architect-model gpt-4o --editor-model claude-3.5-sonnet
```

**Cursor:**
- Open Composer (Cmd+I or Cmd+Shift+I)
- Show multi-file editing
- Demonstrate @ mentions for context

**Goose:**
- Show Desktop App (if available)
- Demonstrate a recipe
- Show session management

**Tips:**
- Have fallback recordings ready
- Test internet connection
- Pre-stage repos in interesting states
- Have "before and after" examples ready

---

## 🚫 What NOT to Say

 
❌ "Cursor was acquired by Anthropic"  
❌ "AI will replace all developers"  
❌ "You should only use one tool"  
❌ "MCP is just another API standard" (it's more than that)

---

## ✅ What TO Emphasize

✅ "The pace of change is remarkable"  
✅ "MCP is becoming the standard"  
✅ "Try multiple tools - different strengths"  
✅ "Open source tools are competitive with commercial"  
✅ "AI coding is about augmentation, not replacement"  
✅ "This landscape will look different in 18 months"

---

## 🎯 Key Takeaway Message

**Main Point:**
> "We're witnessing the fastest evolution in developer tooling in decades. The tools we use to write code are fundamentally changing. Stay curious, stay flexible, and embrace the change - because it's not slowing down."

---

## 📚 Additional Resources to Share

**Official Sites:**
- Aider: https://aider.chat
- Anthropic MCP: https://modelcontextprotocol.io
- Cursor: https://www.cursor.com
- Goose: https://block.github.io/goose
- Junie: https://www.jetbrains.com/junie

**Community:**
- Aider Discord
- Cursor Forum: forum.cursor.com
- Goose Discord: discord.gg/block-opensource

**Benchmarks:**
- Aider Leaderboard: https://aider.chat/docs/leaderboards/

---

## 🎭 Backup Slides Ideas

If you have time, consider adding:
1. **MCP Architecture Diagram** - Show how it works
2. **Cost Comparison** - Monthly pricing breakdown
3. **Security Best Practices** - What to watch out for
4. **Integration Examples** - Real-world MCP servers
5. **Model Comparison** - GPT-4o vs Claude 3.5 vs others

---

## ⏰ Timing Notes

**Original presentation:** ~45 minutes  
**With new slides:** ~55-60 minutes (5 new slides)

**Pacing:**
- 2-3 minutes per "What's New" slide
- Allow extra time for questions (this is hot topic!)
- Budget 5 minutes for MCP deep-dive if audience is interested

---

**Good luck with the presentation!** 🚀

Remember: You're not just updating them on tools - you're showing them the future of how software gets built.
