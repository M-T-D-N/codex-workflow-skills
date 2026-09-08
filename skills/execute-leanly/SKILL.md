---
name: execute-leanly
description: "Execute or resume authorized multi-step Codex work with minimal repetition: reuse verified checkpoints, batch reads, limit planning and polling, verify proportionally, and use safe wait time from long-running compute for already-authorized independent work. Use for active implementation, audit, cleanup, training or OCR 학습, builds, benchmarks, exports, indexing, batch jobs, 진행해, 이어서 처리해, 다음 작업 진행, 잔여작업 처리, or reducing repeated reads, tests, gates, and status polling during real work. Do not trigger for simple Q&A, one-step edits, status-only or reasoning-level questions, new-chat handoff preparation, casual chat, or when a narrower skill already governs the same execution and monitoring behavior."
---

# Execute Leanly

Apply all applicable instructions and task-specific skills. Use this skill only to choose the leanest compliant execution path; never weaken safety, approvals, exactness, or required validation.

## Workflow

1. Resume the latest verified checkpoint. Treat imperative wording such as `진행해`, `이어서 처리해`, or `다음 작업 진행` as authorization only when an in-scope pending item is clear. Treat questions such as `다음 작업은?`, `무엇을 해야 해?`, or `현황 알려줘` as read-only. If no checkpoint exists, inspect only enough to identify the safe next action; ask only when a missing choice changes the result.
2. Reuse unchanged evidence within the turn. Before a third identical read, status check, or poll, use the cached state or change approach. Recheck only after inputs changed, evidence became uncertain, or authority requires it.
3. Batch independent reads. Skip plans for simple work and update long-work plans only on material state changes. After a yielded operation, choose a useful recheck cadence from the runbook, expected checkpoints, or observed progress instead of inserting unneeded status-list calls. Delegate only when allowed and the parallel benefit exceeds context and coordination cost; never use fixed fan-out.
4. For an authorized command expected or observed to run long, use a supported yield or background mechanism only when the applicable runbook permits it and exact process identity, logs, and exit state remain observable. Infer long-running status from the command, runbook, expected work, or observed progress; do not use a fixed time threshold or task label alone. Do not detach, restart, pause, reprioritize, or terminate the command merely to enable side work.
5. While that command runs normally, advance known pending items from the current request, plan, or verified checkpoint without another prompt only when each item is already authorized, does not depend on the running result, does not write job-owned mutable paths or alter the source, configuration, data, artifacts, or acceptance evidence that define the run, and does not materially contend for required devices, CPU, memory, disk I/O, locks, ports, or external quotas. Treat artifact handling as independent only when current evidence establishes that its inputs are closed or immutable snapshots and the side work will not move, overwrite, or invalidate job-owned state. It may index, verify, or organize still-needed artifacts in separate, provisional outputs; deletion or retirement additionally requires active retention, resume, selection, and evidence rules to mark them disposable. Prefer producer-owned lifecycle operations. Do not invent adjacent work. If independence cannot be established cheaply from current evidence, wait.
6. Choose side-work units that can yield by the next meaningful recheck, then recheck the command at that cadence or when the unit finishes. Stop side work on completion, failure, an evidence-backed stall, an input request, or resource or integrity risk. If no safe pending item remains, wait. Honor explicit monitor-only, wait-only, pause, or do-not-start-next-work instructions.
7. Run the smallest existing check that directly proves the outcome, starting with the affected path or real user entrypoint. Rerun only after input changes, one justified transient retry, or a required final pass. Do not add tests for tests, gates for gates, validation runners, hashes, seals, or approval artifacts without an observed gap or explicit authority.
8. Communicate only meaningful state changes, decisions, blockers, and required long-work updates. Lead with the outcome. In the final response, report material changes, verification, unverified risk, and the next useful action; mention a reasoning level only when requested or materially different work remains.
9. When asked to finish the current work and wait, complete only the current authorized unit, report the verified checkpoint, and stop. Do not start the next item or create a checkpoint artifact unless requested.

## Boundaries

- Combine pending items only when their scope, required reasoning, and validation align.
- Ask only when a missing choice changes the result, scope, approval, or validation; otherwise make the safest in-scope assumption.
- Stop when the requested outcome is verified. Do not expand into adjacent cleanup, documentation, gates, or optimization.
