---
name: request-grounding
description: Choose the smallest suitable change when the intended behavior, existing capability or owning component is materially uncertain. Skip settled changes and read-only Q&A; route recurrent or multi-cause failures to evidence-driven-debugging.
---

# Request Grounding

Prevent premature implementation by determining what the request actually requires in the current system. This is a bounded preflight and router, not a general architecture audit, diagnosis method, review gate, or implementation workflow.

## Trigger

Apply before selecting a change only when current evidence could materially change the target, semantics, or change mode and at least one condition holds:

- Past work, decisions, or the user's established workflow could change the interpretation.
- An existing capability may already satisfy all or part of the request.
- The user-visible symptom or concept may map to a different internal object.
- The component or layer that should own the change is unclear.
- The choice among configuring, exposing, deleting, refactoring, extending, or implementing is unsettled.
- Skipping current-state inspection creates a material risk of duplicate or misplaced work.

Do not activate merely because a task involves code, past context, or a repository. Skip it when the target, semantics, and acceptance condition are already settled, regardless of task size; when the request is only Q&A, status, or a scope-fixed review; or when a narrower specialist skill already owns the decision.

## Ground the Request

Inspect only the smallest relevant slice of current evidence. Prefer the current request, applicable authority files, actual user entry points, existing code and configuration, and verified history over inferred architecture. If prior context materially affects the decision, use the available history or memory workflow and verify consequential claims against current evidence.

Form a compact internal grounding brief:

- **Actual goal:** the user outcome, not the first proposed implementation.
- **Verified current state:** what the system demonstrably does now.
- **Existing capability and workflow:** what already satisfies or nearly satisfies the goal.
- **Ownership and mapping:** the user-visible concept, its internal representation, and the layer that should own any change.
- **Material unknowns:** only unknowns that could alter the change mode or acceptance condition.
- **Acceptance condition:** the smallest observable condition that establishes success.
- **Change mode:** the action class justified by the evidence.

Do not turn every unknown into a question. Resolve discoverable facts directly. Ask the user only for knowledge or choices that cannot be recovered safely and would materially change the result.

## Choose the Change Mode

Use the narrowest mode that meets the acceptance condition:

- `NO_CHANGE` or `CONFIGURE` when existing behavior already meets the goal or only settings differ.
- `EXPOSE_OR_LINK` when the capability exists but the user workflow cannot reach or see it.
- `SURFACE_ONLY` when semantics are correct and only UI or copy should change.
- `SCOPE_SPLIT` when one request combines already-supported behavior with a genuine gap.
- `DELETE` or `REFACTOR` when confirmed wrong or duplicate logic should be removed or reorganized. Do not assume deletion is always preferable.
- `EXTEND_EXISTING` when an established owner can satisfy the remaining gap without creating a parallel system.
- `IMPLEMENT_NEW` only when verified existing capabilities cannot meet the acceptance condition.
- `DIAGNOSE` when the cause of a technical failure is unresolved; use `evidence-driven-debugging` when installed for recurrent or multi-cause failures; otherwise establish discriminating evidence before patching. Do not declare them architectural by default.
- `HOLD_FOR_EVIDENCE` or `CLARIFY` when the missing evidence or user decision can change the selected mode materially.

## Boundaries and Handoff

Stop investigating when additional inspection is unlikely to change the selected mode or acceptance condition. Do not require a full system map, formal design document, or exhaustive capability inventory by default.

Keep the grounding brief internal unless it changes the requested direction, exposes materially different choices, requires user-only knowledge, or shows that the evidence is insufficient. Otherwise continue the authorized task without adding ceremony.

After selecting a mode, hand the work to the applicable implementation, UI, debugging, review, or execution workflow. Preserve the user's authorization boundary: grounding a request does not authorize unrelated changes, external actions, or broader cleanup.
