# Worker setup

Read this only when the current environment has not established a usable worker contract. These are configuration requirements, not instructions to install or start software.

## Minimum contract

The current user request or applicable repository runbook should establish:

| Field | What must be known |
|---|---|
| Execution surface | An available agent tool, connector, or verified executable entrypoint |
| Model choice | Availability of the selected `gpt-6.1-sol` or `gpt-6-luna` model and its supported effort, or the configured Local Qwen model; preserve explicit user selections and Main settings, and do not invent a replacement |
| Data boundary | Which files and context may be read or transmitted, especially to remote services |
| Workspace | Exact repository/worktree and allowed write paths |
| Invocation | Actual supported arguments or tool schema; no invented flags |
| Acceptance | Independently checkable behavior and accessible evidence; Qwen write work needs its exact decisive command before dispatch; read-only Qwen work needs a cheap source/schema check. Native workers may find suitable existing checks within their assigned scope |
| Lifecycle | Exact invocation handle and supported wait/cancel; for a managed service, its instance identity/ownership token, readiness check, owner-checked release, active-consumer protection, and persistence intent |
| Result | Completion/failure state, changed files and actual diff or inspected scope and source references, command exit status, and unresolved uncertainty; map local adapter states explicitly |

Discover missing facts with the smallest read-only inspection of the applicable runbook or tool documentation. If setup would require installations, new accounts, paid resources, permission changes, or unrelated configuration, let Main complete the task when possible. Request setup only if the user actually needs it for the intended outcome.

## Common environments

- **No worker available:** Main completes the task. A separate worker is optional.
- **Local model service already configured:** Use its published control-plane entrypoint and existing lifecycle rules. A stopped service may still be usable when that authorized entrypoint starts it and verifies exact readiness. A model responding to chat alone does not prove safe file editing or verifiable task execution. Distinguish a borrowed instance from one this task started, including prewarm, and retain the identity needed for safe release.
- **Host-native agent tools:** Use only documented spawn, messaging, waiting, reuse, and cancellation operations. Check model availability, child context, sandbox inheritance, and parallel-work conditions. Include the [native startup and waiting instructions](luna-lane.md) in the handoff; pass relevant changes again when reusing an idle child. Agent handles and app task IDs are different identities.
- **Remote worker:** Confirm authorization for external processing of the exact content. Do not infer this from the existence of an API key or an installed connector.

If a worker cannot expose its changes or acceptance evidence, it is not eligible to own implementation under this skill. Do not add an orchestration framework or monitoring service solely to satisfy this optional route.

The current workflow prefers `gpt-6.1-sol` for ready independent implementation and `gpt-6-luna` for narrow implementation, format conversion, fixture/test branches or bounded evidence with cheap verification. Start both at `high` unless the user selects otherwise, and choose a supported effort for the unit under [Swarm's guidance](../SKILL.md#worker-reasoning-effort). Local Qwen is an opportunistic option for naturally independent, low-risk work when dispatch and verification replace useful Main work; no universal file-count cap applies. Keep the configured adapter's actual format, source-access and ownership limits.

Keep at most one active Luna unit; reuse compatible idle workers only after the prior execution has ended and its effects are attributed. Read the [handoff and result contract](handoff-and-results.md) for native corrections, Qwen failure attribution and safe takeover. Do not create a worker or model retry cascade.

This portable edition retains explicit worker-role defaults but supplies no model access, the author's control-plane script, machine paths, or runtime. If the selected model/effort or a safe adapter contract is unavailable, Main can proceed under the existing scope. Do not install dependencies, change global model settings, or guess equivalent commands solely to activate this skill.
