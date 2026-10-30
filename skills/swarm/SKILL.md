---
name: swarm
description: Delegate substantial, bounded implementation, investigation, verification or document work before Main solves it, including later units, resumed handoffs and result acceptance. Use for independently checkable evidence audits, trace comparisons and document consistency work; skip trivial tool-complete work and inseparable Main judgment.
---

# Swarm

Delegate worthwhile, independently checkable work before Main solves it. Reduce Main's investigation, implementation and rework while preserving the user's outcome and verification. Do not invent work, fragment a coherent unit or count calls as savings.

This portable edition supplies instructions, not a worker runtime, model weights or executable adapter. Read [worker setup](references/worker-setup.md) only when the current environment does not establish an authorized worker contract. Use the selected model and effort only when the host exposes them; otherwise Main owns the unit. Never invent model identifiers, executable paths or substitute-model cascades.

## Preserve authority

- Keep Main's selected model and effort unchanged. Main owns scope, approvals, consequential meaning, integration and the final answer.
- Inherit repository, sandbox, external-data and scheduling boundaries. This skill requests eligible delegation; it grants no permissions.
- Keep one owner per unit, one active writer per repository/worktree, and no nested delegation or competing implementation. Tests sharing mutable outputs also conflict.
- Track the exact invocation and native handle or app thread ID. Before ownership transfer, confirm execution ended and attribute its effects against the starting state. Turn completion does not prove disposal or a free slot. Accept or discard each result once.

## Choose the next owner before solving the unit

Use the targeted reads needed to establish scope, inputs and acceptance, then choose an owner before substantial investigation, comparison, drafting or implementation. Apply the boundary to the next ready unit, including later in the same turn. Reuse unchanged decisions; do not survey the project, create a mapper/scoring log or add periodic checks to find work to delegate.

1. **Reuse results or an existing tool** when they cover the unit. For unchanged inputs and criteria, retrieve the prior result and reuse its verified scope; a missing chat summary alone does not justify reconstructing it. Main or a tool handles trivial restatement/reformatting and other work whose handoff and review would cost more than it replaces.
2. **Keep unresolved meaning with Main:** architecture/shared-core contracts, security, permissions, migration, deployment, possible data loss, temporal/concurrency semantics, novel algorithms, formal/global claims and material evidence conflicts. Keep inseparably coupled work or work without reliable acceptance with Main; serialize conflicting writes and mutable device/test state.
3. **Delegate ready work:** the outcome and ownership are bounded, inputs/tools accessible, acceptance independently checkable, and enough work remains to justify handoff plus review. Main may resolve a missing requirement, root cause or acceptance example, then stops before deriving the patch. Routine internal design and finding relevant existing tests belong to the worker.
4. **Select a suitable worker and effort** using the guidance below. Explicit user choices take precedence; these defaults are workload choices, not universal model rankings or global routing. No worker must first fail another model.
5. **Separate suitability from availability.** Capacity, a disabled service, approval or a host requirement for independent parallel work is an execution condition. Do not disguise or bypass it. Main retains a unit that cannot be delegated safely, with one concrete reason.

At a natural boundary—concrete failure cases, resolved prerequisites/meaning, or an accepted integration—apply this choice to newly ready work before solving it. An earlier assignment does not cover the next unit. Do not relabel a failed objective as new work.

### Worker selection

| Worker | Suitable ready unit |
|---|---|
| Local Qwen | Naturally separable, low-risk reading, extraction, structuring, classification or small changes with clear scope/output, cheap verification and low startup/handoff/review cost. Use explicitly owned paths and supported adapter formats/tools. |
| `gpt-6-luna` | Narrow implementation, conversion, fixture/test branch or bounded evidence collection whose result is cheap to verify. |
| `gpt-6.1-terra` | Bounded visual/screen interpretation, defined UI workflows, writing or adaptation from supplied material, and scoped code/UI fixes with direct verification. The chosen surface must actually receive the required images, tools and permissions. |
| `gpt-6.1-sol` | Preferred for multi-step implementation, cross-file logic, debugging and validation needing substantial interpretation or autonomous follow-through within the agreed scope. |

If Qwen suitability is unclear, or its output would require consequential final review or near-complete rework, select a suitable native implementation worker or Main. Make this choice in existing planning; the user need not mention Qwen. Do not add a classifier call, availability loop, per-turn health probe, mandatory critic or Qwen-specific summary. Run its existing preflight only for a selected dispatch.

### Adapt to the selected Main

Use these workload splits as starting points, informed by [official model selection](https://developers.openai.com/api/docs/guides/model-selection). They do not establish equal quality, savings or host availability; preserve Main's selected model and effort.

- **Astra Main:** keep ambiguous requirements, consequential design choices, evidence conflicts and final integration with Main. Delegate ready implementation and validation to Sol, visual/writing/scoped UI work to Terra, and focused extraction/tests to Luna or eligible Qwen. Main still handles inseparably coupled work; it need not design the worker's entire patch before handoff.
- **GPT-6.1 Sol High Main:** Main may own a cohesive implementation/integration path while delegating worthwhile independent evidence, tests and visual/writing/UI units. Use another Sol for a substantial independent implementation unit when offloading or parallel work benefits the outcome, without duplicating Main's implementation. Keep unresolved meaning with Main; do not insert an Astra review or change Main merely because Sol is selected.

For either Main, select by the unit and handoff/review cost, not a fixed model ladder or quota. Reuse the same worker for directly related changes; a different audience, artifact or input/tool boundary may justify a fresh bounded handoff when old context is no longer useful. Model choice does not authorize concurrent control of the same UI or shared mutable state.

### Worker reasoning effort

Choose capability first, then effort for the ready unit before dispatch. These starting points follow [subagent guidance](https://learn.chatgpt.com/docs/agent-configuration/subagents) and [model guidance](https://learn.chatgpt.com/docs/models); they do not prove equivalence between models.

| Effort | Work and acceptance |
|---|---|
| `low` | Straightforward lookup, extraction or transformation with a direct inexpensive check. Do not create a worker for a trivial command. |
| `medium` | Settled implementation with few interactions and a direct inexpensive check. |
| `high` | Logic tracing, several integrated steps, assumptions/edge cases, or material uncertainty after assessing the unit. |
| `xhigh` / `max` | Substantial planning or dense dependencies / especially difficult ready work where added depth justifies latency and usage. |

For a settled Terra unit, `medium` is a workload starting point; use `high` when bounded visual ambiguity or interacting changes require deeper reasoning. Visual input alone does not select effort. Honor explicit user model/effort choices. Parent-task risk, file count or elapsed time alone does not select effort. Greater effort neither settles consequential meaning nor expands permissions; resolve those decisions with Main. If work exceeds Luna's focused role, choose Sol or Main rather than Luna at `max`.

Before dispatch, pass both the selected model and effort through the actual supported native/app arguments, with a brief workload rationale in the handoff. A reused worker may retain its known compatible pair; do not silently substitute unknown, default or inherited settings for the selected pair. Change settings only through a supported override or compatible/new worker after reconciling ownership; never use a low-to-max retry ladder or treat permission/tool failures as reasoning failures.

### Bounded evidence collection

Evidence units may locate callers/tests, answer a concrete multi-file question or classify fixed logs. Require inspected scope, exact source references, findings and gaps; a diff or invented test command is unnecessary for read-only work. A limited search does not prove global absence. Keep open-ended research and consequential final criticism with Main unless a useful independent evidence unit can be scoped under the same owner criteria.

## Handoff and scheduling

Read the entrypoint and relevant [handoff and acceptance sections](references/handoff-and-results.md) when applying this skill. Reuse applicable original text still in context across dispatch, follow-up and acceptance; reread only after a relevant instruction change, missing source context or concrete uncertainty. Pass relevant updates in the existing handoff before reusing a worker; do not assume it reloads the skill or interrupt an in-flight unit just to refresh instructions. The reference owns execution, correction/takeover and the [result contract](references/handoff-and-results.md#result-contract); no polling, version marker or separate workflow is needed.

Read only the selected lane's execution instructions and include its startup/return requirements:

| Lane | When to read |
|---|---|
| [Native workers](references/luna-lane.md) | Available native tools under their host scheduling, permission and capacity conditions. |
| [App workers and file delivery](references/app-lane.md) | User-authorized ordinary local app tasks; never a native-capacity workaround. |
| Local Qwen | A selected eligible local unit; use the lifecycle below and [worker setup](references/worker-setup.md) when its adapter contract is unknown. |

## Local Qwen execution and lifecycle

Select an eligible unit under the opportunistic conditions above before any Qwen-specific state check or startup. Use the verified local adapter and lifecycle described in [worker setup](references/worker-setup.md). This distribution includes no Qwen executable or control-plane script. Select an eligible unit before starting a service. An off service alone is not a reason to reject it when the configured, authorized entrypoint can start it and verify its exact model, context, and readiness.

Optional prewarm may overlap necessary preparation only through that documented lifecycle; join readiness before dispatch and retain the returned instance identity. Do not prewarm excluded work or retry a failed prewarm through another path.

Invoke the configured public operation for the initial attempt at a frozen unit with its actual supported workspace, request, source/owned-path and acceptance inputs. For read-only work, use its documented read-only mode, identify the requested output and source/schema check, and omit an executable acceptance command when none is needed. Read-only work must not run mutating tests. Its contract must establish resource ownership, readiness, and accessible worker results, including on nonzero exit. Do not bypass its control plane with a lower-level worker script. Retain the service instance and whether this task started it, including prewarm ownership.

For writes, accept only a well-formed adapter `DONE` (or a documented equivalent completion state), the intended diff within explicitly owned paths, only required test/fixture changes, no weakened or unrelated tests, current acceptance exit `0`, and Main's semantic check. For read-only work, require `DONE`, no changed files, complete requested output with source references, and the specified cheap source/schema check. `DONE` alone is not proof. If checking requires Main to redo the work, the unit is not a suitable opportunistic choice. Account for nonzero public exit or unresolved release before claiming completion.

A busy/unavailable service or failed, ambiguous or incomplete result returns control to the normal native/Main path under the handoff contract. Do not loop on availability, force reclaim, create a second instance, or repeat an unchanged failed attempt with altered prompts/profiles. Main may authorize a retry after a verified in-scope correction under the shared [recovery rules](references/handoff-and-results.md#correction-or-takeover), once the original execution has ended and its effects are known. Existing resource leases and active-consumer protection remain authoritative; do not change another consumer's service, data or profile for this unit.

Reuse this task's service across successive units and immediately continuing goal turns. Before a normal final response, goal completion/cancellation/block, or open-ended wait, end this task's calls and release only its own instance through the configured owner-checked operation using the recorded instance identity or owner token. Active-consumer protection may defer release; never stop a borrowed or replaced service. A documented stop-after option may request the same owned cleanup for a final isolated call. Report unresolved release. After abrupt interruption, reconcile the recorded identity; host-exit cleanup is a fallback, not proof of turn cleanup. If no safe release contract exists, do not start a temporary service.

## Report only supported effects

Use the shared [measurement guidance](references/handoff-and-results.md#measure-effects) for invocation/efficiency audits and savings claims. Consult [current price evidence](references/luna-lane.md#price-evidence) only when comparing costs. Main verifies actual artifacts and evidence; worker completion is not quality acceptance.
