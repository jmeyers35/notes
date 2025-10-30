# Just Talk To It – Notes

## Summary
Just Talk To It – the no‑bs Way of Agentic Engineering is a long‑form article by Peter Steinberger describing his personal workflow for AI‑assisted coding. He argues that modern agentic coding is effective enough to write almost all of his code. Steinberger prefers to work with OpenAI’s GPT‑5‑Codex model using the codex CLI rather than building complex multi‑agent orchestration systems. The article emphasizes focusing on productive dialogue with a single capable agent instead of building charades (RAG pipelines, subagents, Agents 2.0), and describes his tech stack (a TypeScript React app, Chrome extension, CLI, Tauri client and Expo mobile app) along with his context and harness choices. He compares codex favourably against Anthropic’s Claude Code and other tools, noting better context management, efficiency and reliability. He discusses how he manages “blast radius” by anticipating the scale of code changes, uses tmux for background tasks, and iterates on features using conversation and minimal specs rather than rigid plan files.

## Key Takeaways
- **Use GPT‑5‑Codex as primary agent:** Steinberger uses codex CLI as his daily driver and runs multiple instances in parallel. He finds it to offer a better balance of smartness and speed compared with competitors, and appreciates its larger effective context window.
- **Skip the charade:** He argues that many trendy techniques (RAG, subagents, Agents 2.0, elaborate harnesses) add complexity without much benefit. Instead of building multi‑agent pipelines and orchestrators, just talk to a capable model and let it handle tasks.
- **Context management and blast radius:** Think about how big a change will be and control the “blast radius” by limiting the number of files modified at once. If a task seems too large, ask the agent for options or interrupt it to steer the process.
- **Keep prompts short and use screenshots:** When using codex, he often writes prompts of one or two sentences and attaches a screenshot to provide additional context. The model is good at reading the codebase and matching images to relevant code.
- **Avoid heavy plan files:** Codex doesn’t require big plan mode – simple discussions ("let’s discuss", "give me options") are sufficient to guide the model. He seldom writes extensive specifications and instead iterates interactively.
- **tmux for background tasks:** Since codex lacks built‑in background task management, Steinberger uses tmux to run long‑running CLI tasks in persistent sessions. This avoids paying the token cost of additional MCPs.
- **Refactoring and maintenance:** Around 20 % of his time is spent on refactoring – jscpd for duplication, knip for dead code, eslint plugins, updating dependencies, splitting large files, adding tests, etc. He lets the agent handle most of this.
- **Minimal slash commands:** He only uses a handful of slash commands (/commit, /automerge, /massageprs, /review) and rarely needs them, preferring to rely on the agent’s intuition.
- **Build intuition through practice:** The core message is that the more you work with agents and treat them like teammates, the better your results will be. Developing intuition about how to interact with them is more valuable than engineering complex toolchains.

## Open Questions
- **Future of codex vs. competitors:** Will Anthropic or other labs catch up or surpass Codex in terms of context management and stability? How will open models like GLM 4.6 or Kimi compare as they mature?
- **Scalability of single-agent workflows:** Can a single agent continue to handle very large codebases and projects effectively as complexity grows, or will multi-agent coordination become necessary at some scale?
- **Long‑term viability of harnesses:** Are there scenarios where harnesses or orchestrators (e.g., MCPs, Factory, Conductor) provide clear benefits that justify their cost? How might these tools evolve to become genuinely useful?
- **Best practices for sharing agent files:** Steinberger maintains a long Agents.md file containing prompts and context for codex; is there a better way to manage and standardize these agent configuration files across different models?

## Additional Notes
- The article stresses that agentic workflows are still evolving. While GPT‑5‑Codex currently performs best for Steinberger’s use case, new releases from OpenAI or Anthropic could change the landscape quickly.
- Steinberger highlights the importance of human oversight: even when agents write most of the code, you still need to think deeply about architecture, system design, features and user experience.
- This note file was generated on 30 October 2025, summarizing the key points from the article published on 14 October 2025.
