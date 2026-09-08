# Worker setup

Read this only when the current environment has not established a usable worker contract. These are configuration requirements, not instructions to install or start software.

## Minimum contract

The current user request or applicable repository runbook should establish:

| Field | What must be known |
|---|---|
| Execution surface | An available agent tool, connector, or verified executable entrypoint |
| Model choice | The configured worker model; preserve the user's main model |
| Data boundary | Which files and context may be read or transmitted, especially to remote services |
| Workspace | Exact repository/worktree and allowed write paths |
| Invocation | Actual supported arguments or tool schema; no invented flags |
| Acceptance | An existing independent command, expected outcome, and accessible result |
| Lifecycle | Exact invocation handle and supported wait/cancel; for a managed service, its instance identity/ownership token, readiness check, owner-checked release, active-consumer protection, and persistence intent |
| Result | Completion/failure state, changed files, actual diff, command exit status, and unresolved uncertainty |

Discover missing facts with the smallest read-only inspection of the applicable runbook or tool documentation. If setup would require installations, new accounts, paid resources, permission changes, or unrelated configuration, let Main complete the task when possible. Request setup only if the user actually needs it for the intended outcome.

## Common environments

- **No worker available:** Main completes the task. A separate worker is optional.
- **Local model service already configured:** Use its published control-plane entrypoint and existing lifecycle rules. A stopped service may still be usable when that authorized entrypoint starts it and verifies exact readiness. A model responding to chat alone does not prove safe file editing or verifiable task execution. Distinguish a borrowed instance from one this task started, including prewarm, and retain the identity needed for safe release.
- **Host-native agent tools:** Use only documented spawn, messaging, waiting, and cancellation operations. Check whether child context and sandbox are inherited rather than assuming isolation.
- **Remote worker:** Confirm authorization for external processing of the exact content. Do not infer this from the existence of an API key or an installed connector.

If a worker cannot expose its changes or acceptance evidence, it is not eligible to own implementation under this skill. Do not add an orchestration framework or monitoring service solely to satisfy this optional route.

The personal source workflow uses Local Qwen first and optionally one Luna implementation worker. This portable edition preserves that ordering as configured local-worker first, then at most one additional worker; it deliberately does not ship the author's control-plane script, fixed model overrides, machine paths, or runtime. Use the current environment's documented equivalents, not guessed commands. If no usable contract exists, Main can proceed and state the limitation.
