---
name: swarm
description: Route nontrivial repository implementation, fixes, refactoring, and bounded evidence collection to suitable workers before Main solves the task. Use when a clear work unit has enough execution or investigation left to justify handoff and verification. Keep simple Q&A, status checks, trivial edits, and inseparable Main judgment with Main.
---

# Swarm

Reduce Main's investigation, implementation, and rework while preserving required outcomes and verification. Use native Luna for suitable complete work units and Local Qwen for its verified narrow lane. Do not create work, fragment a coherent task, or count calls as savings.

This portable edition supplies instructions, not a worker runtime, model weights, or executable adapter. Read [worker setup](references/worker-setup.md) when the current environment does not establish an authorized worker contract. Use the named native model only when the host exposes it; otherwise Main owns the unit. Never invent model identifiers, executable paths, or substitute-model cascades.

## Preserve authority

- Keep the user's Main model and reasoning effort unchanged. Main owns scope, approvals, consequential meaning, integration, and the final answer.
- Inherit repository, sandbox, external-data, and scheduling boundaries. This skill requests eligible delegation; it cannot override the available tool's conditions or grant new permissions.
- Use one owner per unit, one active writer per repository or worktree, and no nested delegation or competing implementation. Tests sharing mutable outputs also conflict.
- Track the exact Qwen invocation or Luna handle. Before transferring ownership, confirm its execution ended and attribute changes against the starting state. Completion of a turn does not prove disposal of an agent or release of a slot. Classify each result once as accepted or discarded.

## Choose the next owner before solving the unit

Use the first targeted reads already needed for the request. Consider the whole request first, then natural independently checkable units. Do not run a repository survey, mapper, scoring system, or routing log just to find delegation.

1. **Use an existing tool** when a verified command or converter already completes the work. Main handles genuinely trivial edits whose handoff and review would dominate.
2. **Keep unresolved meaning with Main.** Main decides architecture/shared-core contracts, security, permissions, migration, deployment, possible data loss, temporal/concurrency semantics, novel algorithms, formal/global claims, and material evidence conflicts. Keep inseparably coupled implementation or work without a reliable way to judge its outcome with Main. Complexity or a risky parent task does not exclude a separable, reversible unit with settled behavior.
3. **Hand off ready work.** The required outcome and bounded ownership must be clear, necessary inputs/tools accessible, acceptance independently checkable, and enough work remain to justify handoff plus review. Main may resolve the missing requirement, root cause, or acceptance example, but stops before deriving the patch. Routine internal design and finding the project's relevant test command belong to a capable native worker.
4. **Choose the suitable worker directly.** Local Qwen remains available for low-risk, limited-search, frozen-behavior changes to 1–3 explicitly owned UTF-8 source, product, test, or fixture files with a fast, decisive acceptance command. Choose it when this verified narrow lane fits, considering startup, review, and cleanup. For other ready units, native `gpt-5.6-luna` at `max` is the default execution owner when the native scheduling contract allows it and there is no concrete capability/context mismatch. Luna does not require a failed Qwen attempt, a proof that Qwen is incapable, or Qwen's file-count cap.
5. **Distinguish suitability from availability.** A disabled service, model/capacity limit, approval, or a host rule requiring independent parallel work is an execution condition. Do not disguise it as unsuitable work or bypass it. Main owns a unit that cannot be delegated safely, with one concrete reason.

After Main resolves meaning or a prerequisite, or after an accepted result is integrated, route the next remaining unit before Main designs its patch. Successful completion does not exhaust Luna's allocation for the entire user task: different ready units may be assigned sequentially. Reuse decisions whose inputs are unchanged. Never relabel a failed objective as a new unit.

### Bounded evidence collection

Luna may answer a concrete multi-file question, locate relevant callers/tests, extract specified facts, or classify bounded logs when handoff has useful work to replace. It returns inspected scope, exact file/line or source references, findings, and gaps; a diff is not required. Main retains interpretation of the user's request and consequential conclusions. A failed or limited search does not prove global absence. Do not spawn a researcher for a one-command lookup or open-ended exploration. This does not expand the Qwen writer or critic adapter contract.

## Handoff and scheduling

A packet names the exact repository/workspace and starting state, pre-existing changes to preserve, user outcome and material exceptions, owned files or a narrow feature boundary with exclusions, source locations, acceptance behavior and known commands, and uncertainties to return rather than guess. Native workers may choose ordinary implementation details and discover suitable existing verification within that boundary. Qwen requires its exact executable/arguments, working directory, runtime/environment, owned 1–3 paths, and acceptance command before dispatch. Shell syntax requires an explicit shell executable.

Reference original files instead of copying their full contents or the whole conversation. Do not omit constraints to shorten the packet. Return concise findings and evidence locations instead of full logs. No new packet files, telemetry, orchestration layer, or test framework is required.

Read [Luna execution](references/luna-lane.md) only when choosing a native unit, and include its worker startup instructions in the native handoff. When reusing a child after relevant execution instructions change, pass the changed instructions with the next handoff; do not assume the child reloads edited files. Keep at most one active Luna unit at a time. The host's current parallel-work requirements still apply; when it permits serial offloading, lack of parallel Main work alone is not a reason to reject it. Qwen's existing synchronous route remains available. Start only ready units; dependencies must finish first.

Once assigned, let the worker own implementation, related checks, and ordinary local corrections. Main advances independent work or uses a supported bounded wait; it does not solve the same unit, run its commands one by one, or poll unchanged state repeatedly. Honor explicit user/host call budgets and cancellation limits. Follow Luna's patient-wait guidance; elapsed time, silence, or a wait timeout alone is not execution failure.

If the user requirement or relevant source changes materially, do not integrate stale output. End or safely interrupt that exact execution and attribute its effects before revalidating or discarding it. Additive guidance that preserves the outcome does not automatically invalidate the unit.

## Accept results and converge

Main inspects the actual diff/artifact and directly affected dependencies, owned scope, requested behavior, and real verification evidence. A worker's summary or self-reported model identity is not proof. Expected test values must follow the requirement or existing contract; never accept weakened tests or circular implementation-derived expectations.

Reuse reliable checks for unchanged code and environment. Repeat only for changed inputs/integration state, a concrete gap, unreliable evidence, or required authority. A native worker returns actual commands, working directory, relevant environment, exit status, results, changed paths, and remaining uncertainty.

Normal compile/test corrections within a running unit belong to the worker. Return control when meaning needs a new decision, the same failure repeats without progress, or an execution limit is reached. After a failed, invalid, or rejected candidate, confirm the exact execution ended, attribute partial changes, preserve user changes, and let Main take over. No failed-objective retry, renamed replacement, or Qwen→Luna→other-model cascade. If attribution is unsafe, stop.

After a native spawn is rejected by capacity/model/surface availability, do not repeat it. Inspect `list_agents` at most once if useful; reuse only an exactly compatible idle non-root child via supported `followup_task`, otherwise Main owns the unit. Do not infer a slot leak or create a new task/fork to evade the limit. Reuse an unresolved common execution failure for affected units until evidence changes.

Use independent review only when requested or justified by consequence, conflicting evidence, or a material validation gap. For Qwen's bounded critic option, read [Qwen critic](references/qwen-critic.md); its one-critic contract remains unchanged, and Qwen never reviews its own candidate. Otherwise Main reviews unless independence is an explicit acceptance condition; report unavailable independent review honestly.

## Local Qwen execution and lifecycle

Use the verified local adapter and lifecycle described in [worker setup](references/worker-setup.md). This distribution includes no Qwen executable or control-plane script. Select an eligible unit before starting a service. An off service alone is not a reason to reject it when the configured, authorized entrypoint can start it and verify its exact model, context, and readiness.

Optional prewarm may overlap necessary preparation only through that documented lifecycle; join readiness before dispatch and retain the returned instance identity. Do not prewarm excluded work or retry a failed prewarm through another path.

Invoke the configured public operation once per frozen unit with its actual supported workspace, request, owned-path, and acceptance-command inputs. Its contract must establish resource ownership, readiness, and accessible worker results, including on nonzero exit. Do not bypass its control plane with a lower-level worker script. Retain the service instance and whether this task started it, including prewarm ownership.

Accept only a well-formed adapter `DONE` (or a documented equivalent completion state), a non-empty intended owned diff, only the expected 1–3 changed files, explicitly owned and required test/fixture changes, no weakened or unrelated tests, acceptance exit `0`, and Main's semantic check. Account for nonzero public exit or unresolved release before claiming completion.

Reuse this task's service across successive units and immediately continuing goal turns. Before a normal final response, goal completion/cancellation/block, or open-ended wait, end this task's calls and release only its own instance through the configured owner-checked operation using the recorded instance identity or owner token. Active-consumer protection may defer release; never stop a borrowed or replaced service. A documented stop-after option may request the same owned cleanup for a final isolated call. Report unresolved release. After abrupt interruption, reconcile the recorded identity; host-exit cleanup is a fallback, not proof of turn cleanup. If no safe release contract exists, do not start a temporary service.

## Report only supported effects

Use the dated [model price comparison](references/luna-lane.md#price-evidence) as one factor when choosing native work. Compare qualified outcomes and total handoff/review/rework cost, not nominal price alone; raw token reduction and monetary savings are separate claims. Sol's comparison price does not add an automatic Sol role or fallback.

Distinguish skill selection, successful dispatch, accepted work, and measured savings. Use existing results/logs when available; account for Main preparation/review/takeover and worker usage together, with latency separately. Do not double-count cumulative usage events or token subcategories. A successful example proves that path only. Without comparable complete evidence, report token/cost savings and automatic invocation rate as unmeasured.
