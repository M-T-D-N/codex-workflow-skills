---
name: swarm
description: "For nontrivial repository implementation, check local-worker routing before Main designs or writes the patch, then re-route newly ready work at dependency checkpoints. Delegate small, low-risk tasks with settled behavior and a decisive acceptance check to a configured worker. Keep uncertain semantics, risk, and integration with Main. Skip Q&A, read-only investigation, trivial edits, urgent work, and inseparable changes."
---

# Swarm

Reduce Main's implementation load by handing suitable semantic units to the configured local worker. Check ownership during the first targeted reads the task already needs, then repeat at real dependency checkpoints until all authorized implementation lanes close. An initial Main decision does not end routing. Do not create a repository-wide survey, split work artificially, or invent work just to increase delegation.

This portable edition includes no worker runtime, model weights, executable adapter, or fixed machine paths. Main means the agent responsible for the user's task. A worker means an already available, authorized execution surface.

## Establish availability and authority

- Preserve the user's selected main model and reasoning settings.
- User instructions, repository rules, sandbox restrictions, and external-action approvals still govern every worker. Installing this skill does not authorize an otherwise prohibited delegation, service launch, dependency installation, or external transmission.
- Before dispatch, read [worker setup](references/worker-setup.md) if the current environment does not already establish the worker's entrypoint, isolation, lifecycle, and result contract.
- Prefer a configured local worker for eligible bounded work. Separate eligibility from service readiness: a stopped service is not a reason to skip eligible work when its configured, authorized entrypoint can start it and verify exact readiness. If the worker contract is missing, disallowed, or unverifiable, Main owns the task. Report a launch, permission, identity, or consumer conflict as an execution condition; do not describe it as absence of suitable work or invent an executable path.
- Only after the local-worker check, consider at most one additional host-native or remote worker in the entire task for a substantial independent lane that is not local-worker eligible and has no known capability or context mismatch. Use the host's permitted model selection; do not override the main model. This worker is not a repository mapper, leaf finder, critic, or fallback after local-worker failure.

## Choose an owner before writing

Apply Main exclusions to the actual unit: unresolved outcome semantics, architecture or shared-core ownership, security, permissions, migrations, deployment, possible data loss, timing or concurrency judgment, novel algorithms, formal or global claims, conflicting material evidence, and work without a decisive independent check. A parent task involving deployment or shared state does not exclude separately verifiable downstream implementation.

Distinguish Main preparation from Main implementation. Main may perform a necessary bounded clarification, diagnosis, contract, or acceptance example that makes a low-risk unit ready, then re-route before designing or writing its product patch. If preparation would substantially derive the patch, or a hard exclusion remains, Main implements that unit. Do not manufacture tests or speculative tasks to enable delegation.

A local worker may own a whole task or a downstream unit when all apply:

- The expected change is limited to 1–3 explicitly owned UTF-8 source, product, test, or fixture files.
- The desired behavior is settled by the request, existing interface, and acceptance criteria.
- Discovery is limited, the change is low risk and non-urgent, and it introduces no unsettled semantics.
- A fast acceptance command independently establishes the required result. Reuse an existing check; Main may first add a minimal independently specified acceptance case already required by the request. Worker-invented expected values are not an independent oracle.
- Workspace ownership is clear and existing user changes can be preserved.

File count alone does not establish eligibility. Unchosen implementation details are not unsettled outcome semantics. Do not keep an otherwise eligible unit with Main merely because Main could write it faster or has no parallel work; a short synchronous wait is acceptable. The whole request may be one eligible unit.

After Main settles a requirement or root cause, finishes a prerequisite, or observes a new in-scope defect, route the next implementation unit before designing or writing it. Recheck only units whose relevant facts changed. After a worker closes and its effects are attributed, route the next ready unit without waiting for another user turn. Otherwise keep the unit with Main for a concrete reason such as risk, coupling, no oracle, excessive discovery, writer conflict, urgency, or a trivial edit. No routing log is required.

## Freeze a bounded task packet

Provide only the information the worker needs:

- Exact repository or worktree and current source identity.
- Relevant pre-existing changes that must be preserved.
- User outcome, owned files, settled behavior, and prohibited scope.
- The independent acceptance command and what constitutes failure.
- Uncertainties to report instead of guessing.

Reference accessible source files rather than copying unchanged files into the packet. Do not transmit credentials, unrelated files, or private context to a worker. External workers require authorization covering the supplied content and destination.

The acceptance command must name the executable and arguments in the verified working directory and environment. Shell expressions require an explicit shell executable; do not pass them to a shell-free runner. Preserve project-specific signing, data, and cache identities across execution permissions. Ask for a short summary of unresolved uncertainty and owned paths the worker could not inspect or change; use primary result fields for the diff and test evidence.

## Schedule and track

- Keep one active implementation owner per lane and one active writer per repository or worktree. Concurrent writers require separate authorized worktrees or repositories and disjoint ownership.
- No nested delegation, duplicate implementations, or fixed fan-out.
- Record every exact tool invocation or agent handle in the running task context. Feed local-worker units sequentially; dispatch the next only after the previous invocation closes and its effects are attributed. Classify each result once as accepted or discarded before overall completion. Do not dispatch a replacement while its invocation is live.
- Main may continue independent authorized work that does not conflict with the worker's inputs, outputs, or resource needs. Do not design a competing patch for assigned work.
- Use supported bounded waits tied to the next decision point and progress evidence. A longer additional-worker lane should have useful independent Main work to overlap it and must not block the critical path. Empty output or a wait timeout does not prove failure. Never restart or terminate an unrelated process by a broad name match.
- Reuse an existing healthy service. Start or prewarm a worker only through an explicitly configured and authorized lifecycle, with observable identity and resource ownership. Prewarm only eligible work, join readiness before dispatch, and do not retry a failed prewarm through another launch path. Do not alter shared runtimes to make delegation possible.

If an additional-worker or critic spawn is rejected by capacity or an unavailable model/tool, do not retry the spawn. Inspect the visible agent tree at most once and reuse only an exactly compatible idle child through supported operations; otherwise Main owns the lane. Do not infer a slot leak or create a new task, fork, or replacement-model cascade. Report a required independent critic as unavailable rather than substituting Main self-review.

## Accept, recover, and integrate

Accept a candidate only when:

1. The exact invocation has completed and the result is well formed.
2. The intended non-empty diff is limited to owned files.
3. No existing test has been weakened and every test or fixture edit was explicitly in scope.
4. The independent acceptance command succeeded.
5. Main inspects the actual diff and confirms it satisfies the settled behavior at the current source identity.

A worker's claim that checks passed is insufficient without accessible command results or equivalent primary evidence. Reuse trustworthy existing validation; do not repeat a full suite merely because another agent ran it.

Account for a nonzero public-entrypoint exit or unresolved service cleanup even if candidate files and checks appear successful.

After failure, timeout with partial output, or an invalid result, first establish whether the invocation is still active. Close only its exact authorized handle as appropriate, attribute its changes against the starting state, and preserve user changes before transferring ownership. If changes cannot be safely attributed, stop and report the uncertainty. Once recovered, Main owns the failed lane; do not retry the writer or cascade through replacement workers.

A genuinely different objective or newly observed defect may be routed after the failed invocation closes and its effects are settled, even if it owns the same files. Renaming the failed task, making a commit, or choosing another patch for the same objective does not create a new lane. Reuse a known common execution failure for affected lanes until evidence shows it is resolved; do not repeat known failing launches.

If the user requirement or relevant source changes materially before integration, active or returned output is stale. Confirm invocation closure and attribute changes before revalidating or discarding it, or dispatching a replacement. Additive guidance that leaves settled behavior unchanged does not invalidate a lane. Never integrate a candidate twice.

## Release owned services

Retain whether this work started a service, including prewarm, and its exact instance identity or ownership token. Reuse it across successive units and immediately continuing goal turns. Before a normal final response, or when work completes, is cancelled, becomes blocked, or enters an open-ended wait, close this work's invocations and release only the instance it started through the configured owner-checked lifecycle. An active goal alone is not a reason to keep a service warm.

Preserve borrowed or replaced instances and let the control plane protect other active consumers. Report deferred or unresolved cleanup rather than claiming shutdown. After interruption, reconcile the recorded instance on resume; a host-exit fallback is not evidence that turn cleanup happened. If no safe release contract exists, do not start a temporary service.

## Review when it changes confidence

Use at most one independent critic for the candidate, and only when requested or when material risk, conflicting evidence, or a validation gap justifies it. The critic must not have produced the candidate. Use a read-only surface with access limited to the relevant evidence.

For a bounded local review, require settled low-risk behavior, 1–3 product or source files, unchanged test definitions, and an independent acceptance check. Keep security, concurrency, recovery, architecture, and global claims with Main unless an appropriately qualified independent review is explicitly required and available.

Review failure means review unavailable, not approval or rejection. If independent review is a required acceptance condition and unavailable, report that gap; Main self-review is not independent evidence. Bind every verdict to the exact candidate. After a correction, describe any Main-only verification accurately.

Main owns final synthesis, integration, and the user-facing result. Stop when the requested outcome and required evidence are complete.
