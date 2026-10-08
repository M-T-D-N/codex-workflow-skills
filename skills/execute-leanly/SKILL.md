---
name: execute-leanly
description: Coordinate authorized multi-step execution with repeated reads, large results or long-running work. Skip simple work, continuation wording alone, and behavior already owned by a narrower skill.
---

# Execute Leanly

Apply all applicable instructions and task-specific skills. Use this skill only to choose the leanest compliant execution path; never weaken safety, approvals, exactness, or required validation.

## Workflow

1. Resume the latest verified checkpoint. Treat imperative wording such as `진행해`, `이어서 처리해`, or `다음 작업 진행` as authorization only when an in-scope pending item is clear. Treat questions such as `다음 작업은?`, `무엇을 해야 해?`, or `현황 알려줘` as read-only. If no checkpoint exists, inspect only enough to identify the safe next action; ask only when a missing choice changes the result.
2. Reuse unchanged evidence within the turn. Before a third identical read, status check, or poll, use the cached state or change approach. Recheck only after inputs changed, evidence became uncertain, or authority requires it.
3. Batch independent reads. Skip plans for simple work and update long-work plans only on material state changes. After a yielded operation, choose a useful recheck cadence from the runbook, expected checkpoints, or observed progress instead of inserting unneeded status-list calls. Delegate only when allowed and the parallel benefit exceeds context and coordination cost; never use fixed fan-out.
4. Before launching or resuming monitoring of a long-running command, read [long-running work](references/long-running-work.md). Use only authorized, observable execution; side work requires independent inputs and resources. Otherwise wait.
5. Run the smallest existing check that directly proves the outcome, starting with the affected path or real user entrypoint. Reuse prior verification only while it still supports the current result. Recheck the affected scope after relevant changes, concrete counterevidence, incomplete or invalid evidence, a justified transient retry, or a required final pass. Recover missing detail from existing results or logs first; do not rerun work merely to change its output format. Do not add tests for tests, gates for gates, validation runners, hashes, seals, or approval artifacts without an observed gap or explicit authority.
6. Communicate only meaningful state changes, decisions, blockers, and required long-work updates. Lead with the outcome. In the final response, report material changes, verification, unverified risk, and the next useful action; mention a reasoning level only when requested or materially different work remains.
7. When asked to finish the current work and wait, complete only the current authorized unit, report the verified checkpoint, and stop. Do not start the next item or create a checkpoint artifact unless requested.

## Output selection

- Choose the needed output before querying: matching paths, selected fields, counts, or bounded text ranges. Prefer source-side filters. Read the needed detail directly when its location is known; do not add a preliminary summary call by habit.
- Keep the project's established test/build entrypoint. Use a supported concise mode only when it preserves the required checks, failure diagnostics, relevant warnings, and exit status. Interpret stderr together with exit status and diagnostic content; its presence alone is not a failure verdict.
- Keep machine-consumed stdout and generated artifacts intact. For structured results, validate and parse them before selecting fields for display. Preserve the distinction between no matches, execution failure, and incomplete or truncated results.
- When returning tool results, preserve failure status, diagnostic locations, and any session or continuation identifier needed to finish or inspect the operation.
- If detail is missing or truncated, retrieve the relevant part from the existing result or log. Repeat only an authorized, safe read when necessary; do not rerun a state-changing or expensive operation merely to reformat its output.

## Boundaries

- Combine pending items only when their scope, required reasoning, and validation align.
- Ask only when a missing choice changes the result, scope, approval, or validation; otherwise make the safest in-scope assumption.
- Stop when the requested outcome is verified. Do not expand into adjacent cleanup, documentation, gates, or optimization.
