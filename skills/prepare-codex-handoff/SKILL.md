---
name: prepare-codex-handoff
description: Prepare a prompt to paste into another Codex task when the user requests a handoff or resumption prompt. Exclude actual task creation, forking or transfer, current-task continuation, and handoffs to people or other tools.
---

# Prepare Codex Handoff

Create one copy-ready prompt that lets another Codex task resume without the old transcript. Compress repeated narration, not consequential context. Do not create, fork, open, or hand off a task, continue implementation, write a checkpoint file, or create or replace a goal merely to prepare the prompt.

## Workflow

1. Start from the current request and latest verified checkpoint. Reuse evidence already established in the conversation. Recall prior memory or inspect files only when a consequential fact is missing or uncertain; treat recalled content as derived context and verify it against current authority or files when it affects the next action.
2. Put facts that the new chat cannot safely recover directly in the prompt: the objective and completion condition, exact project or working directory, authorized scope, do-not-touch boundaries, relevant decisions and reasons, verified outcomes, remaining work and dependencies, blockers or unknowns, the next action, and the smallest direct validation.
3. Add a recovery index for facts available elsewhere: exact `AGENTS.md` or authority documents, current-state and evidence files, commits or worktrees, artifacts, and narrowly scoped queries for an available, user-authorized history service when useful. State why each reference matters. Do not copy generic policy text, full histories, raw logs, or bulk tool output.
4. Use adaptive length. Include conversation-only consequential details directly even when that makes the prompt longer. Replace recoverable detail with a path and a short relevance note. Preserve a failed attempt only when it prevents repetition or changes the safe next action.
5. Mark mutable claims that the recipient must revalidate, such as Git status, running processes, external state, or time-sensitive facts. Never convert a one-time approval into standing approval in the new chat.
6. Output only the handoff prompt unless the user asks for commentary. Use these sections when applicable: `Objective`, `Start here`, `Verified checkpoint`, `Decisions and boundaries`, `Remaining work`, `Evidence and recovery`, and `Revalidate before acting`.
7. Before returning, confirm that a recipient can identify what to achieve, why the current approach was chosen, what is already verified, what not to repeat or change, what to do next, and how to verify it. Add only missing consequential context; do not perform a new full audit.

## Boundaries

- Treat requests to actually create, fork, open, navigate to, or hand off a Codex task as native task-management operations, not as prompt preparation.
- Assume the new task has its own transcript even when it shares project files and instructions.
- Keep credentials, authentication material, unnecessary personal data, raw transcripts, and bulk output out of the handoff.
- Do not claim that the handoff was opened, delivered, or executed.
- Do not create or update files, goals, memories, or external state merely to prepare the handoff.
