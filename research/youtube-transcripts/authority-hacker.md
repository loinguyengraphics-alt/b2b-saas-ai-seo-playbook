# YouTube Transcript: Authority Hacker (Gael Breton & Mark Webster)

## Video: 5 Months Of Claude Code (As A Business Owner)
* **Date:** June 2026
* **URL:** [[YouTube URL](https://www.youtube.com/watch?v=OYJa8XPd210)]

### Core Strategy: Progressive Disclosure & Self-Maintaining AI Workflows
The video breaks down the transition from basic AI prompt engineering to building a robust, agentic workflow using Claude Code and the Claude Desktop App. The primary focus is on managing context limits and creating an AI environment that updates its own documentation and executes programmatic tasks (like newsletter generation and CRM management) autonomously.

### Key Workflow Optimizations for B2B Automation

1. **Folder-Based Granularity (VS Code vs. Claude Desktop)**
   * **The Problem:** Dumping everything into a single workspace folder clutters the context window, causing the AI to lose focus or reference outdated information.
   * **The Solution:** Use the Claude Desktop App to manage separate project folders (e.g., Marketing, Support, Website). Each folder runs its own instance and context, while still allowing the user to seamlessly open complex files in VS Code for granular editing using the "diff" view.

2. **Progressive Disclosure in `claude.md`**
   * Keep the root `claude.md` file (the system prompt) short. Instead of stuffing it with exhaustive brand guidelines, use it to link to specific markdown files within a `/documentation` or `/wiki` folder.
   * *Mechanism:* Claude reads the overarching rules in `claude.md` and only pulls specific sub-documents (e.g., target audience, brand voice) when the current task demands it.

3. **The "Self-Updating Wiki" Prompt Rule**
   * **Crucial Takeaway:** Add a rule to the `claude.md` file instructing Claude to *proactively offer to update the documentation* whenever a task deviates from the existing guidelines.
   * *Example:* If Claude drafts an email and the human editor corrects the pricing or tone, Claude should ask: "Should I update the marketing strategy file to reflect this new price/tone?" This ensures the AI's context improves automatically without manual maintenance.

4. **CLI Integration over Heavy MCPs**
   * For connecting third-party tools (like Notion or Google Workspace), prefer Command Line Interfaces (CLIs) over complex Model Context Protocol (MCP) servers. CLIs deliver cleaner markdown payloads, saving massive amounts of context limits and improving the AI's processing speed.

5. **Routine Automation (Agentic Workflows)**
   * Transition from manually triggering tasks to setting up scheduled "Routines" within the Claude App.
   * *Use Case:* Schedule a routine to run every morning at 9 AM to process new CRM applications, draft the response emails, and queue them up for human review. The goal is to automate the workflow *up to the final point of publishing*, eliminating the friction of starting tedious tasks.

### Key Takeaway
B2B SaaS teams must move beyond isolated prompts and treat AI as an operational environment. By structuring folders correctly, utilizing progressive disclosure for brand documentation, and programming the AI to self-update its rules, marketers can create a highly autonomous programmatic content engine.
