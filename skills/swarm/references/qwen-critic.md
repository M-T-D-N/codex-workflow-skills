# Qwen critic

Keep important final criticism with Main. This optional, non-final evidence check needs a concrete cost/verification reason; it is not a routine Swarm stage or a way to rescue a failed Qwen output. Use this optional Local Qwen check only when all are true:

- Qwen did not produce or edit the candidate;
- the candidate has a small, explicitly owned scope in supported product/source files and changes no tests or fixtures;
- requirements are frozen, clear, and low risk;
- an independent decisive oracle exists and the candidate did not change its definition; and
- review excludes temporal or recovery judgment, concurrency, security, permissions, migration, deployment, architecture, formal or global claims, and broad review.

Use the configured adapter from [worker setup](worker-setup.md) with its documented read-only mode, exact workspace, frozen review packet and independent acceptance command. Confirm that this mode cannot modify the candidate; do not invent a read-only flag or bypass the configured entrypoint.

Treat both `DONE` and `ESCALATE` as candidate evidence, not a final verdict. Main must cheaply corroborate the claimed behavior against the frozen source and existing decisive oracle. A reported defect needs the exact file and behavior, violated requirement, smallest counterexample, and why the visible check still passes. Transport, runtime, invalid-output, or read-only failure means review unavailable, not a verdict; continue with Swarm's normal native/Main work. A retry after a verified correction follows the shared handoff-and-results recovery rules; do not repeat an unchanged failed attempt.

Never let Qwen review a candidate it produced or edited. Do not cascade critics without a concrete unresolved verification need. A verdict binds only the exact reviewed candidate; after a correction, determine which affected checks need repeating. Report Main's checks as parent verification, and claim independent review of the corrected result only when it actually occurred.
