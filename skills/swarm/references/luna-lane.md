# Luna execution

Use native `gpt-5.6-luna` at `max` for a bounded, substantial, independently checkable implementation or evidence-collection unit selected by Swarm. It owns implementation → relevant verification → ordinary local corrections → evidence return, or the specified read-only question. No fixed 1–3-file limit applies; ownership and reviewable scope do.

## Dispatch and ownership

- Explicitly request model `gpt-5.6-luna` and reasoning effort `max` using the actual supported spawn arguments. Use `fork_turns="none"` or a bounded positive recent-turn count with the packet. A full-history fork inherits Main's settings and cannot serve as this model override.
- Preserve the user's Main settings and the current native tool's permissions and scheduling conditions. Prefer the existing explicit spawn path; a new custom role, global subagent default, hook, or proxy is not a prerequisite.
- Start only when the unit needs no unfinished Main/Qwen result. If the host requires useful independent parallel work, satisfy that condition or keep this unit with Main. If it permits serial offloading, Main may wait without inventing side work.
- Keep one active Luna unit at a time. Concurrent writers must own disjoint scope in separate repositories/worktrees allowed by project policy; otherwise serialize. Read-only work must not mutate shared state through tests.
- Reuse a healthy idle compatible child for directly related subsequent work when supported. Otherwise a different ready objective can use a new native call after the prior execution has ended and its effects are attributed and integrated. Do not accumulate unrelated work merely to reuse context, assume a reusable slot from turn completion, or evade capacity limits.

## Worker startup instructions

Main includes these instructions in the native handoff so they apply before the worker reads repository files:

- Send useful progress through the native collaboration API to Main's exact agent path, and return the completed result in the final response. When the host exposes `collaboration.send_message` as a top-level tool, call it directly, outside `functions.exec`. If the host provides an `ALL_TOOLS` inventory of nested tools, absence there does not establish that its top-level collaboration API is unavailable.
- If native collaboration messaging is unavailable, omit progress messages and return the completed result in the final response. Do not substitute app task-management tools, memory-service signals, or another messaging store for native parent reporting. Agent paths such as `/root` are not app thread IDs.
- Start ordinary local reads, including `AGENTS.md`, with default sandbox permissions. Request escalation only for a required capability under the host's approval rules; do not request elevated reads merely because later writes may need approval or batch approval requests in parallel.
- Keep a required approval request pending without bypassing it, submitting a duplicate, or treating approval delay as execution failure.

## Return and recovery

Return changed paths or inspected scope, actual commands and working directory, relevant environment and exit statuses, behavior evidence, unresolved uncertainty, and inaccessible owned paths. Main verifies the actual diff/artifact and acceptance independently of the worker summary.

Use supported bounded waits and honor explicit user/host execution budgets. In the absence of such a limit, allow a substantial Luna unit to run to completion without an arbitrary elapsed-time cutoff. Silence, a wait timeout, or an empty progress channel does not establish stalled execution; the worker may have no progress-reporting tool. At a meaningful check-in, inspect the last call and available status, then continue the original run when no concrete failure or cancellation condition is established. Avoid repeated progress prompts, unchanged status polling, and duplicate work while waiting. Evidence of a stuck tool or runtime calls for diagnosis of that execution, not blind waiting or a claim that Luna reasoning has failed.

The worker may fix ordinary errors inside its active unit. Return control when scope/meaning needs a new decision, the same failure repeats without progress, or an explicit execution limit is reached. Confirmed unrecoverable execution faults, material scope changes, explicit stop requests, and user/host limits remain reasons for recovery under the existing ownership rules.

Confirmed approval waiting is excluded from execution timeouts. Approval waiting does not transfer the worker's assigned ownership. An escalation request alone does not establish its current state; if the host does not expose it, report the pending state as unknown. Do not interrupt or resubmit solely because approval is slow. After late approval, consume the original call's result and continue from its actual state.

On stale work, interrupt only the exact active handle if needed, confirm that execution has ended, and attribute changes before revalidation or discard. A completed agent turn, an idle reusable agent, and a disposed agent are different states; report only what the tools confirm.

If spawn is rejected, ownership has not transferred. Follow Swarm's capacity branch without repeated spawn. After execution failure, invalid output, or Main rejection, Main takes over that objective after effect attribution; no worker retry or model cascade. Never integrate one candidate twice.

## Price evidence

Checked 2026-09-14: standard API USD per 1M text tokens for the base context tier (input at most 272K), not a Codex plan-usage conversion.

| Model | Ordinary input | Cached input | Cache write | Output |
|---|---:|---:|---:|---:|
| [GPT-5.6 Luna](https://developers.openai.com/api/docs/models/gpt-5.6-luna) | 0.20 | 0.02 | 0.25 | 1.20 |
| [GPT-5.6 Sol](https://developers.openai.com/api/docs/models/gpt-5.6-sol) | 4.00 | 0.40 | 5.00 | 20.00 |
| [GPT-6 Astra](https://developers.openai.com/api/docs/models/gpt-6-astra) | 10.00 | 1.00 | 12.50 | 50.00 |

Cache writes use the documented 1.25× ordinary-input rate. Longer context, service tier, tools, and actual billing terms can change cost; Sol's published promotional pricing is guaranteed at least through 2026-11-21. Refresh this evidence when those terms matter or change, not as a mandatory lookup for every unit.

At equal ordinary-input/output counts, Astra's rates are 50×/41.67× Luna's and 2.5× Sol's; Sol's are 20×/16.67× Luna's. These ratios support delegating suitable work, not accepting lower quality or predicting equivalent token counts. An expensive model can still have lower total task cost if it avoids enough exploration or rework.

For comparable complete API usage, cost is the sum across Main and workers of ordinary input, cached input, cache writes, and output multiplied by their corresponding rates. Do not add subcategories twice. The relevant break-even condition is that worker execution plus Main handoff/review/rework costs less than the Main work it replaces. Without comparable evidence, retain this as a routing rationale and leave realized savings unmeasured.
