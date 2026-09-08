---
name: swarm
description: "Route nontrivial repository implementation to a configured local worker for small, low-risk tasks with settled behavior and a decisive acceptance check. Keep uncertain semantics, risk, and integration with the main agent. Use only when delegation is authorized and useful; skip Q&A, read-only investigation, trivial edits, urgent work, and inseparable changes."
---

# Swarm

Use a shallow delegation plan to reduce the main agent's implementation load. Check ownership during the first targeted reads the task already needs. Do not create a repository-wide survey just to find work for another agent.

This portable edition includes no worker runtime, model weights, executable adapter, or fixed machine paths. Main means the agent responsible for the user's task. A worker means an already available, authorized execution surface.

## Establish availability and authority

- Preserve the user's selected main model and reasoning settings.
- User instructions, repository rules, sandbox restrictions, and external-action approvals still govern every worker. Installing this skill does not authorize an otherwise prohibited delegation, service launch, dependency installation, or external transmission.
- Before dispatch, read [worker setup](references/worker-setup.md) if the current environment does not already establish the worker's entrypoint, isolation, lifecycle, and result contract.
- Prefer an existing configured local worker for eligible bounded work. If it is missing, unavailable, disallowed, or cannot be independently verified, Main owns the task. Do not invent an executable path, model name, or setup requirement.
- Consider at most one additional remote worker for a substantial independent lane only when permitted, useful, and not appropriate for the local worker. Use the host's permitted model selection; do not override the main model.

## Choose an owner before writing

Keep these with Main: unresolved outcome semantics, architecture or shared-core ownership, security, permissions, migrations, deployment, possible data loss, timing or concurrency judgment, novel algorithms, formal or global claims, conflicting material evidence, and work without a decisive independent check.

A local worker may own a whole task or a downstream unit when all apply:

- The expected change is limited to 1–3 explicitly owned UTF-8 source, product, test, or fixture files.
- The desired behavior is settled by the request, existing interface, and acceptance criteria.
- Discovery is limited, the change is low risk and non-urgent, and it introduces no unsettled semantics.
- A fast existing acceptance command independently establishes the required result.
- Workspace ownership is clear and existing user changes can be preserved.

File count alone does not establish eligibility. Main owns root-cause analysis and inseparable upstream decisions; do not write nearly the entire patch as worker instructions. Once Main settles a dependency, check only newly ready downstream work. Do not repeat an unchanged routing decision or split a self-contained task merely to increase delegation.

## Freeze a bounded task packet

Provide only the information the worker needs:

- Exact repository or worktree and current source identity.
- Relevant pre-existing changes that must be preserved.
- User outcome, owned files, settled behavior, and prohibited scope.
- The independent acceptance command and what constitutes failure.
- Uncertainties to report instead of guessing.

Reference accessible source files rather than copying unchanged files into the packet. Do not transmit credentials, unrelated files, or private context to a worker. External workers require authorization covering the supplied content and destination.

## Schedule and track

- Keep one active implementation owner per lane and one active writer per repository or worktree. Concurrent writers require separate authorized worktrees or repositories and disjoint ownership.
- No nested delegation, duplicate implementations, or fixed fan-out.
- Record the exact tool invocation or agent handle in the running task context. Do not dispatch a replacement while that invocation is live.
- Main may continue independent authorized work that does not conflict with the worker's inputs, outputs, or resource needs. Do not design a competing patch for assigned work.
- Use supported waits and progress evidence. Empty output or a wait timeout does not prove failure. Never restart or terminate an unrelated process by a broad name match.
- Reuse an existing healthy service. Start or prewarm a worker only through an explicitly configured and authorized lifecycle, with observable identity and resource ownership. Do not alter shared runtimes to make delegation possible.

## Accept, recover, and integrate

Accept a candidate only when:

1. The exact invocation has completed and the result is well formed.
2. The intended non-empty diff is limited to owned files.
3. No existing test has been weakened and every test or fixture edit was explicitly in scope.
4. The independent acceptance command succeeded.
5. Main inspects the actual diff and confirms it satisfies the settled behavior at the current source identity.

A worker's claim that checks passed is insufficient without accessible command results or equivalent primary evidence. Reuse trustworthy existing validation; do not repeat a full suite merely because another agent ran it.

After failure, timeout with partial output, or an invalid result, first establish whether the invocation is still active. Close only its exact authorized handle as appropriate, attribute its changes against the starting state, and preserve user changes before transferring ownership. If changes cannot be safely attributed, stop and report the uncertainty. Once recovered, Main owns the failed lane; do not retry the writer or cascade through replacement workers.

If the user requirement or relevant source changes before integration, the candidate is stale. Confirm invocation closure and attribute changes before revalidating or discarding it. Never integrate a candidate twice.

## Review when it changes confidence

Use at most one independent critic for the candidate, and only when requested or when material risk, conflicting evidence, or a validation gap justifies it. The critic must not have produced the candidate. Use a read-only surface with access limited to the relevant evidence.

For a bounded local review, require settled low-risk behavior, 1–3 product or source files, unchanged test definitions, and an independent acceptance check. Keep security, concurrency, recovery, architecture, and global claims with Main unless an appropriately qualified independent review is explicitly required and available.

Review failure means review unavailable, not approval or rejection. If independent review is a required acceptance condition and unavailable, report that gap; Main self-review is not independent evidence. Bind every verdict to the exact candidate. After a correction, describe any Main-only verification accurately.

Main owns final synthesis, integration, and the user-facing result. Stop when the requested outcome and required evidence are complete.
