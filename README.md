# Hi, I'm an independent developer working on AI coding agents

I am an independent developer focused on AI coding agents, developer tools, long-running agent workflows, and agent evaluation.

My current work explores how coding agents can become more reliable when working on the same software project across multiple conversations. I am especially interested in project-specific memory, self-reflection, automated self-checking, error recovery, and changelog-based audit trails for long-running software engineering tasks.

---

## Current focus

I am currently researching and building systems around:

- AI coding agents for repository-level software engineering tasks
- Project-specific long-term memory across conversations
- Memory isolation between different software projects
- Agent self-reflection after task completion
- Automated self-checking and error recovery loops
- Controlled investigation when self-checking fails
- Changelog-based audit trails for agent file modifications
- Long-running agent reliability and failure-mode analysis
- Evaluation of whether persistent memory improves or harms agent performance

---

## Current private project

I am developing a private prototype coding agent based on `opencode`.

The agent is designed to support long-running development work inside a software project. It keeps project-level memory across conversations, while keeping memory isolated between different projects.

After completing a task, the agent writes a structured self-reflection and stores it inside the relevant project. These reflections can be reused in future conversations to help the agent avoid repeated mistakes, remember project-specific decisions, and improve its understanding of the codebase over time.

The agent also includes a self-checking loop. After making changes, it reviews its own work to detect possible errors. If the self-check fails, the agent enters a controlled investigation mode, searches for relevant documentation or solutions, reasons again about the issue, and attempts to repair the problem before checking again.

Each project also maintains a changelog that records:

- which files were modified,
- when the modifications happened,
- what was changed,
- and why the change was made.

This changelog is intended to make the agent's behavior more traceable and to help it maintain awareness of its previous actions during long-running coding tasks.

The implementation is currently private while the architecture, memory design, and evaluation methodology are being refined.

---

## Research questions

Some of the questions I am currently exploring:

- Can project-specific memory improve coding-agent reliability across repeated tasks?
- Can structured self-reflection reduce repeated mistakes?
- Does changelog awareness help agents avoid losing track of previous file modifications?
- When does memory help, and when does it harm performance?
- Can self-checking loops improve error recovery without causing unnecessary iteration?
- How should agents handle incorrect memories or outdated project assumptions?
- What failure modes appear when an agent repeatedly modifies the same codebase over time?

---

## Evaluation interests

I am interested in evaluating coding agents not only by whether they complete a task, but also by how reliably they behave over time.

Planned evaluation areas include:

- Task success rate on repository-level coding tasks
- Number of iterations needed to complete a task
- Token usage and API cost
- Error recovery after failed attempts
- Quality and usefulness of self-reflections
- Whether project memory reduces repeated mistakes
- Whether changelog awareness improves long-running task consistency
- Cases where memory, self-reflection, or self-checking harms performance

I am also interested in safety and reliability risks, including:

- Prompt drift from repeated memory injection
- Incorrect lessons being stored in memory
- Over-reliance on previous reflections
- Reinforcement of bad strategies
- Unreliable information introduced during web-based investigation
- Long-running agents losing track of previous file modifications
- Memory from one project accidentally influencing another project

---

## Why this matters

Coding agents are becoming more capable, but long-running software work introduces new reliability challenges.

A coding agent may need to understand a project across many conversations, remember previous decisions, avoid repeating mistakes, recover from failed attempts, and remain aware of files it has already modified.

My goal is to study whether project-specific memory, self-checking, and changelog-based audit trails can make coding agents more reliable and more auditable, while also identifying the new risks these mechanisms may introduce.

---

## Status

This work is currently in active development.

The main implementation is private for now, but I plan to publish methodology notes, evaluation results, and selected findings when the project is ready.

---

## Interests

- AI coding agents
- Developer tools
- Agent memory
- Agent evaluation
- Long-running workflows
- Software engineering automation
- AI reliability and safety
- Human-in-the-loop development tools

---

## Contact

If you are interested in coding agents, long-running agent workflows, or agent evaluation, feel free to connect with me through GitHub.
