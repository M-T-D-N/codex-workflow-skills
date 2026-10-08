# Native worker execution

Use the exact model and effort selected by Swarm or the explicit user request for a bounded, independently checkable native unit. This reference governs native tools only. It owns implementation → relevant verification → ordinary local corrections → evidence return, or the specified read-only question. No fixed 1–3-file limit applies; ownership and reviewable scope do.

## Dispatch and ownership

- Explicitly pass that model and effort using the actual supported spawn arguments; never silently downgrade or substitute. Use `fork_turns="none"` or a bounded positive recent-turn count with the packet. A full-history fork inherits Main's settings and cannot serve as this model override.
- Preserve the user's Main settings and the current native tool's permissions and scheduling conditions. Prefer the existing explicit spawn path; a new custom role, global subagent default, hook, or proxy is not a prerequisite.
- Start only when the unit needs no unfinished Main/Qwen result. If the host requires useful independent parallel work, satisfy that condition or keep this unit with Main. If it permits serial offloading, Main may wait without inventing side work.
- Keep one active Luna unit at a time. Concurrent writers must own disjoint scope in separate repositories/worktrees allowed by project policy; otherwise serialize. Read-only work must not mutate shared state through tests.
- Reuse a healthy idle compatible child for directly related subsequent work when supported. Compatibility includes the selected model and effort. Native `followup_task` does not expose model/effort overrides; to change that pair, use a supported new spawn after the previous execution has ended and its effects are attributed. Do not rely on a prompt asking an existing child to change its own settings. Check its known model and effort against the intended role using existing creation/settings evidence; a Main model change or edited skill does not update an existing child. If that evidence is unavailable, do not claim the requested model is confirmed. Retain a different model only when it remains suitable and no explicit model requirement is violated. Otherwise a different ready objective can use a new native call after the prior execution has ended and its effects are attributed and integrated. Do not accumulate unrelated work merely to reuse context, assume a reusable slot from turn completion, or evade capacity limits.

## Worker startup instructions

Main includes these instructions in the native handoff so they apply before the worker reads repository files:

- Read the parent-provided scope and the [Swarm result contract](handoff-and-results.md#result-contract); return evidence through the supplied exact parent/task handle. A read-only request must return changed_paths empty.
- Send useful progress through the native collaboration API to Main's exact agent path, and return the completed result in the final response. When the host exposes `collaboration.send_message` as a top-level tool, call it directly, outside `functions.exec`. If the host provides an `ALL_TOOLS` inventory of nested tools, absence there does not establish that its top-level collaboration API is unavailable.
- If native collaboration messaging is unavailable, omit progress messages and return the completed result in the final response. Do not substitute app task-management tools, memory-service signals, or another messaging store for native parent reporting. Agent paths such as `/root` are not app thread IDs.
- Start ordinary local reads, including `AGENTS.md`, with default sandbox permissions. Request escalation only for a required capability under the host's approval rules; do not request elevated reads merely because later writes may need approval or batch approval requests in parallel.
- Before submitting a required approval request, use the available native progress channel to identify the exact target, capability and intended operation, plus any existing tool/session identity and partial changes. Label it as planned; report pending, denied, completed or unknown only from an exposed result. If messaging is unavailable, preserve these facts in the normal tool request and eventual return, without creating another reporting channel.
- Keep a required approval request pending without bypassing it, submitting a duplicate, or treating approval delay as execution failure.

## Return and recovery

Return the Swarm result contract through native final: inspected scope and source revision/ranges, actual changed paths, scoped checks with executed_here/reused_prior and validity, execution status and unresolved uncertainty. Do not invent missing host identities. Main verifies the actual diff/artifact and acceptance independently of the worker summary.

Use supported bounded waits and honor explicit user/host execution budgets. In the absence of such a limit, allow a substantial native unit to run to completion without an arbitrary elapsed-time cutoff. Silence, a wait timeout, or an empty progress channel does not establish stalled execution; the worker may have no progress-reporting tool. At a meaningful check-in, inspect the last call and available status, then continue the original run when no concrete failure or cancellation condition is established. Avoid repeated progress prompts, unchanged status polling, and duplicate work while waiting. Evidence of a stuck tool or runtime calls for diagnosis of that execution, not blind waiting or a claim that Luna reasoning has failed.

The worker may fix ordinary errors inside its active unit. Return control when scope/meaning needs a new decision, the same failure repeats without progress, or an explicit execution limit is reached. Confirmed unrecoverable execution faults, material scope changes, explicit stop requests, and user/host limits remain reasons for recovery under the existing ownership rules.

Confirmed approval waiting is excluded from execution timeouts. Approval waiting does not transfer the worker's assigned ownership. An escalation request alone does not establish its current state; if the host does not expose it, report the pending state as unknown. Do not interrupt or resubmit solely because approval is slow. After late approval, consume the original call's result and continue from its actual state.

When explaining a blocked write, Main identifies the requested target and the host restriction actually observed; a project registry or starting folder alone is insufficient evidence. A user's chat confirmation establishes intent, not completion of the pending tool approval. If an independently justified takeover is necessary, first reconcile or cancel the original tool call through supported controls and confirm it can no longer write, then attribute partial changes and transfer ownership. An interrupt acknowledgement or unchanged files alone does not prove that a pending mutation was cancelled; if termination cannot be established, keep the overlapping write blocked.

On stale work, interrupt only the exact active handle if needed, confirm that execution has ended, and attribute changes before revalidation or discard. A completed agent turn, an idle reusable agent, and a disposed agent are different states; report only what the tools confirm.

If spawn is rejected, ownership has not transferred. Follow Swarm's capacity branch without repeated spawn. For completed units, apply the shared [correction and takeover rules](handoff-and-results.md#accept-results-and-converge); use the same compatible idle child through supported followup_task only when those conditions hold. Never integrate one candidate twice.

## Price evidence

Use current official model rates only when a cost comparison requires them: [GPT-6.1 Sol](https://developers.openai.com/api/docs/models/gpt-6.1-sol), [Luna](https://developers.openai.com/api/docs/models/gpt-6-luna), [Astra](https://developers.openai.com/api/docs/models/gpt-6-astra). Record date, service tier and cache assumptions; these rates are not Codex subscription usage.

Sum nonoverlapping ordinary input, cache read/write and output once. Reasoning already included in output is not added again. Include Main preparation/review/rework and every worker attempt or promotion. Without comparable completed-work evidence, keep realized savings unmeasured.
