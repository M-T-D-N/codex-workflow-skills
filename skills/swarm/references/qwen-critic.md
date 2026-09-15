# Qwen critic

Use Local Qwen once as a read-only critic only when all are true:

- Qwen did not produce or edit the candidate;
- the candidate changes only 1–3 product or source files and no tests or fixtures;
- requirements are frozen, clear, and low risk;
- an independent decisive oracle exists and the candidate did not change its definition; and
- review excludes temporal or recovery judgment, concurrency, security, permissions, migration, deployment, architecture, formal or global claims, and broad review.

Use the configured adapter from [worker setup](worker-setup.md) with its documented read-only mode, exact workspace, frozen review packet, and independent acceptance command. Confirm that this mode cannot modify the candidate; do not invent a read-only flag or bypass the configured entrypoint.

Map a well-formed Qwen `DONE` (or its documented equivalent) to acceptance. Treat `ESCALATE` as actionable only when it names the exact file and behavior, violated requirement, smallest counterexample, and why the visible check still passes. Transport, runtime, invalid-output, or read-only failure means review unavailable, not a verdict.

Never let Qwen review its own candidate, retry it, or cascade to another critic. A verdict binds only the exact frozen candidate; any correction invalidates it. Under the one-critic cap, report the corrected result as parent-verified rather than independently reviewed.
