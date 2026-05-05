# Hi, I'm an independent developer working on coding agents

I am an independent developer interested in AI coding agents, developer tools, long-running agent workflows, and agent evaluation.

My current work focuses on building and evaluating repository-level coding agents that can work across multiple conversations within the same software project. I am especially interested in how project-specific memory, self-reflection, self-checking, and audit trails can improve the reliability of AI agents that repeatedly modify the same codebase over time.

---

## Current focus

- AI coding agents
- Repository-level software engineering tasks
- Project-specific long-term memory
- Cross-conversation memory within the same project
- Isolated memory between different projects
- Agent self-reflection after task completion
- Automated self-checking and error recovery
- Controlled investigation when self-checking fails
- Changelog-based audit trails for agent file modifications
- Evaluation of long-running agent reliability and failure modes

---

## Current private project

I am currently developing a private prototype coding agent based on opencode.

The agent is designed for long-running work inside a software project. It keeps project-level memory across conversations, while keeping each project's memory separate. After completing a task, the agent records structured self-reflections and stores them inside the relevant project. These reflections can then be used in future conversations to help the agent avoid repeated mistakes and improve its understanding of the codebase.

The agent also includes a self-checking loop. After making changes, it reviews its own work to detect possible errors. If the self-check fails, the agent enters a controlled investigation mode, searches for relevant documentation or solutions, reasons again about the issue, and attempts to repair the problem before checking again.

Each project also maintains a changelog that records which files were modified, when the changes happened, and what was changed. This is intended to make the agent's behavior more traceable and to help it maintain awareness of its previous actions during long-running development tasks.

The implementation is currently private while the architecture and evaluation methodology are being refined.

---

## Evaluation interests

I am interested in evaluating whether project-specific memory, self-reflection, self-checking, and changelog awareness actually improve coding-agent performance and reliability.

Planned evaluation areas include:

- Task success rate on repository-level coding tasks
- Number of iterations needed to complete a task
- Token usage and API cost
- Error recovery after failed attempts
- Quality of self-reflections
- Whether project memory reduces repeated mistakes
- Whether changelog awareness improves long-running task consistency
- Failure cases where memory or self-reflection harms performance

I am also interested in safety and reliability risks, including:

- Prompt drift from repeated memory injection
- Incorrect lessons being stored in memory
- Over-reliance on previous reflections
- Reinforcement of bad strategies
- Unreliable information introduced during web-based investigation
- Long-running agents losing track of previous file modifications

---

## Why this matters

Coding agents are becoming more capable, but long-running software work introduces new reliability challenges.

An agent may need to understand a project over many conversations, remember previous decisions, avoid repeating mistakes, recover from failed attempts, and remain aware of the files it has already modified.

My goal is to study whether project-specific memory, self-checking, and changelog-based audit trails can make coding agents more reliable and more auditable, while also identifying the new risks these mechanisms may introduce.

---

## Status

This work is currently in active development.

The main implementation is private for now, but I plan to publish methodology notes, evaluation results, and selected findings when the project is ready.

---

## Contact

If you are interested in coding agents, long-running agent workflows, or agent evaluation, feel free to connect with me through GitHub.
