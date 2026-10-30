# Handoff, scheduling and acceptance

Read before dispatch and reuse for result acceptance. This is the existing Swarm execution contract, not an additional gate.

## Handoff and scheduling

Include the following in the existing handoff, using original file references rather than copying the conversation:

| Packet content | Required scope |
|---|---|
| Identity and baseline | Actual parent handle, project, available host task/session/request ID, exact repository/workspace, starting state and existing changes to preserve. |
| Outcome and ownership | User outcome and this unit's contribution, material exceptions, owned files or narrow feature boundary, exclusions and source locations. |
| Execution choice | Selected native/app model and effort with a brief workload rationale; current writable/protected scope and approval limits, or explicit unknowns. |
| Acceptance and uncertainty | Checkable behavior, known commands, and questions to return rather than guess. Code writes need an executable acceptance command; writing/visual/UI deliverables need an existing saved/rendered-artifact check appropriate to the outcome; read-only units use source/schema checks. Shell syntax requires an explicit shell executable. |

Native workers may choose ordinary internal design and discover suitable existing verification within that boundary. For Qwen, supply its public invocation, cwd, necessary source/owned paths, expected output and cheap acceptance check before dispatch.

A registered project, changed cwd, readable source or chat approval does not establish tool permission for a separate worktree. Use the available permission context; do not add a write probe or request broader access merely to qualify delegation. When a known boundary would block the write, choose its owner before dispatch: Main can retain the protected mutation and delegate useful read-only evidence or preparation in an allowed task location, or the worker can own the exact required approval request. Main still needs its own valid tool permission; this split cannot bypass an approval.

Pass the [result contract](#result-contract) to workers that do not inherit it; include protocol-specific startup/return instructions from the selected lane. Preserve constraints and return concise findings with evidence locations. No new packet files, telemetry, orchestration layer or test framework is required.

Follow the selected [native](luna-lane.md) or authorized [app](app-lane.md) lane, including its capacity and ownership constraints. The host's current parallel-work requirements still apply; when it permits serial offloading, lack of parallel Main work alone is not a reason to reject it. Qwen's existing synchronous route remains available. Start only ready units; dependencies must finish first.

### Scope mixed tasks by their next ready unit

Useful boundaries include an existing failed-case subset while Main analyzes a different cause; one upstream subsystem while Main compares another; or a fixed artifact/trace inventory while Main handles account access or final acceptance. Require original references and a bounded check, not a new full project survey. Evidence about article claims or retention value can be delegated; rights approval, policy adoption and deletion remain with Main.

A blocked UI action does not block an independent local evidence unit, but delegation cannot reproduce an inaccessible screen, unlock a device or override denied permission. Keep a brief release lookup, small date calculation, wait for an existing review, or quota-bound sequential generation on its existing path when handoff would add work. These are examples of the owner criteria, not a dispatch checklist or required fan-out.

For repeated collection or review under unchanged criteria, give a compatible worker one bounded set of ready inputs and let it chunk internally within source and output limits. Main need not redispatch each chunk; do not wait for future inputs or expand an open-ended scope to fill a batch. On follow-up, reference usable prior coverage and its input revision and state what remains, including any new input, changed criterion or localized correction.

Return coverage, exclusions, source-linked findings and unresolved items for that set at completion or a material blocker. Surface evidence conflicts or decisions requiring Main promptly; keep routine progress non-blocking. Return earlier for user deadlines, execution limits or unreliable/truncated output. Main verifies coverage and consequential claims before acceptance.

### Execution and invocation handles

Once assigned, let the worker own implementation, related checks, and ordinary local corrections. Main advances independent work or uses a supported bounded wait; it does not solve the same unit, run its commands one by one, or poll unchanged state repeatedly. Honor explicit user/host call budgets and cancellation limits. Follow the native lane's patient-wait guidance; elapsed time, silence, or a wait timeout alone is not execution failure.

Keep the complete execution-start result before extracting stdout, including any yielded tool/session/cell handle. Continue that invocation through its supported wait/continuation tool. If the handle is lost, reconcile the original invocation before launching a replacement or another large scan; report an unresolved result as unknown. Include still-running invocation handles and observed process identity when returning control so Main can reconcile ownership.

If the user requirement or relevant source changes materially, do not integrate stale output. End or safely interrupt that exact execution and attribute its effects before revalidating or discarding it. Additive guidance that preserves the outcome does not automatically invalidate the unit.

## Accept results and converge

Main compares the actual changed/delivered file set, including required documents and artifacts, against the handed-off scope and latest user acceptance criteria, and inspects the diff/artifacts, directly affected dependencies and real verification evidence. Judge unit acceptance separately from overall completion: a targeted PASS leaves broader unmet user criteria open. At that decision, record accepted, needs correction or discarded in the existing turn/result summary, separately from execution status, with the concrete Main edits/rechecks or none and their evidence. Separate routine acceptance checks from corrective work; attribute corrections to requirement/input changes, worker quality, Main integration or environment/permission issues only when supported by evidence, otherwise mark the cause unknown. Keep this attribution in the same summary without a separate reporting format. Do not defer this record to the final project report. A failed attempt with no usable result is discarded with Main takeover, not accepted; partial usable findings may be accepted only within their stated scope. Resolve missing, extra or mismatched deliverables through the existing correction/takeover flow before final acceptance. A worker's summary or self-reported model identity is not proof. Expected test values must follow the requirement or existing contract; never accept weakened tests or circular implementation-derived expectations.

Match cited checks to the last relevant change; a later patch is not covered by an earlier run. Reuse reliable checks for unchanged code and environment, and repeat only affected checks, integration gaps, unreliable evidence or authority-required scope. Accept the actual artifact and the evidence in the result contract below; worker execution completion is separate from Main quality acceptance.

### Verification before live use

For a new or changed verification harness, run the smallest available check without live provider requests before its first live use. Use existing fixtures or a narrow dry run for the affected argument/config parsing, early-failure or terminal-state cleanup behavior; prefer the actual startup/config parser without a provider request when available. A syntax check alone does not establish those behaviors. If no offline check is available, return that precise unverified boundary; this does not require a new test framework or repeating checks for unchanged inputs.

Normal compile/test corrections within a running unit belong to the worker. For compiled-code changes, use the smallest relevant compile/type check before returning an implementation as verified; formatting or parsing alone is insufficient. If the build is centrally owned, unavailable or approval-blocked, return that precise unverified boundary so Main can perform the existing integration check once. Do not add a duplicate full build or transfer ordinary corrections early merely to finish the worker turn. Return control when meaning needs a new decision, the same failure repeats without progress, or an execution limit is reached.

### Correction or takeover

For native and authorized app workers, retrieve actual artifacts before treating a terse or malformed final message as implementation failure. After the current execution has ended and its effects are attributed, Main may send a clear, localized defect and the existing acceptance check to the same compatible worker when the contract is unchanged and correction plus review is cheaper than takeover. Use the lane's supported follow-up, preserve prior failure evidence, and count correction usage. Misunderstood requirements, repeated same-cause failure without progress, an unrecoverable execution fault, or an execution limit returns ownership to Main under the lane's safe-transfer rules; do not create a retry chain across workers or models. Approval waiting is not a completed failed attempt.

After a failed, invalid, ambiguous or incomplete Qwen result, confirm execution ended, attribute effects and return control to Main. Do not repeat an unchanged failed attempt or start a model retry chain. Main may resume the same unit after a verified in-scope correction when effects are known and another attempt is justified, or continue through the suitable existing worker/Main path. If attribution is unsafe, hold the affected mutation and continue independent work.

After a native spawn is rejected by capacity/model/surface availability, do not repeat it. Inspect `list_agents` at most once if useful; reuse only an exactly compatible idle non-root child via supported `followup_task`, otherwise Main owns the unit. Do not infer a slot leak or create a new task/fork to evade the limit. Reuse an unresolved common execution failure for affected units until evidence changes.

Use independent review only when requested or justified by consequence, conflicting evidence, or a material validation gap. Keep consequential final criticism with Main. For a specifically justified, cheap, non-final Qwen evidence check, read [Qwen critic](qwen-critic.md); it is not a routine stage, and Qwen never reviews its own candidate. Otherwise Main reviews unless independence is an explicit acceptance condition; report unavailable independent review honestly.

## Result contract

Use the selected lane's completion channel: native final/report to the actual parent handle, the authorized app task's final response and actual files for Main's exact-ID retrieval, or the configured local adapter's documented result and actual files. Do not invent submit_result/escalate tools, send unsolicited cross-task messages, or create a separate report file unless that artifact was requested. This is a meaning contract for the existing return format, not a new schema or required prose template.

- Identify the project, task/session/request or native handle and input revision actually used. If a host identity is unavailable, say so; never substitute the most recent task.
- Distinguish completed, partial, failed, cancelled, and blocked execution. Return material findings, actual changed_paths (empty for read-only work), and the requested artifacts. Main owns the separate [acceptance decision and record](#accept-results-and-converge); the worker cannot self-accept. Completion of a tool, process, or worker turn does not establish product correctness or Main acceptance.
- Give each material evidence reference its source location, existing revision or observed modification state, and the range actually read. Mark omissions, truncation, inaccessible sources, and unverified claims. Partial reading remains partial.
- For checks, report command, cwd, scope, passed/failed/not_run, executed_here/reused_prior, evidence reference and valid_for_revision. Reused evidence needs unchanged relevant inputs, environment and acceptance criteria. Never relabel it as executed_here or describe a targeted check as the requested full suite. A not_run check has no execution evidence.
- Keep failures and unique counterexamples in the returned evidence. For bounded listings distinguish total count from shown count; reference readable raw output when preserved, and disclose preservation/readback failure instead of claiming a source exists.

Keep cancellation, approval waiting, provider error, process loss, and supersession distinct. Do not revive a user-cancelled unit or accept duplicate/late output for a different request or revision. After disconnection, reconcile the original execution and partial changes before any new dispatch; in-memory handles alone do not prove restart recovery. Continue independent authorized work after a failure, but require successful prerequisites before dependent effects. Recheck permission against final arguments when the target or arguments change after approval. These are host/evidence decisions, not semantic-model scores.

## Measure effects

Use current [price evidence](luna-lane.md#price-evidence) only when needed to compare costs. Compare qualified outcomes and total handoff/review/rework cost, not nominal price alone; raw token reduction and monetary savings are separate claims. A published unit price alone does not establish completed-work savings or a mandatory fallback.

Distinguish skill selection, successful dispatch, accepted work, and measured savings. Use existing results/logs when available; account for Main preparation/review/takeover and worker usage together, with latency separately. Do not double-count cumulative usage events or token subcategories. A successful example proves that path only. For invocation audits, choose the activity window and task sample independently of dispatch success; include non-dispatch, blocked and genuinely trivial cases. Separate new workers, follow-up work and coordination messages, and state the observation window and denominator. All-turn frequency is not the share of eligible work delegated; tool calls alone do not prove automatic skill selection. Do not target a call quota. Without comparable complete evidence, report token/cost savings and automatic invocation rate as unmeasured.
