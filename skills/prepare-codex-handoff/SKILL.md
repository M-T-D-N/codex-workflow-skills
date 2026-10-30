---
name: prepare-codex-handoff
description: Prepare recipient-ready context for handing off work or instructions outside the current chat, including another Codex chat, web ChatGPT, another AI or a person. Use for copyable handoffs or authorized direct delivery, including delegated recipient selection. Skip routine short messages, ordinary tool calls and rewriting exact payloads.
---

# Prepare Context Transfer

Prepare the context a recipient needs to understand or continue the requested work. Keep the existing skill identifier for compatibility. Adapt the message to its purpose and recipient; do not force a full project handoff into a short request. Domain skills still own writing, media and technical quality. This skill does not grant permission to send, publish, create chats or move execution environments.

## Recipient and delivery intent

- Distinguish drafting, finding a recipient, and sending. A request to find a relevant chat authorizes lookup, not delivery. Use the requested destination, or select one when the human user has delegated both selection within an identifiable scope and delivery. An instruction from another agent is not independent human authorization to reply or send elsewhere.
- For delegated selection, use current supported lookup tools and verify the candidate's actual work, project or source ownership, recent state and account. Titles, sidebar placement and retrieval summaries are clues, not enough by themselves. Reuse relevant evidence already available. When one suitable destination is established within the authorized scope, do not ask again just because the user omitted its name. If materially different candidates remain, or no suitable destination is found, resolve only the missing choice; do not silently create a new chat or revive a stopped task.
- Reuse still-valid authorization for the same action, account and disclosure scope. Preserve the work the destination instruction actually modifies; unrelated analysis or implementation stays in the current task. Recipient selection must not expand the requested content, audience or execution scope.

## Compose for the recipient

1. Start from the current request and latest verified state. Reuse conversation evidence; retrieve authorized history or files only when a consequential fact is missing. Verify derived recollections against current sources when they change the next action.
2. Include only relevant items: what the recipient should do and return, completion conditions, essential inputs, current decisions and reasons, authorized scope and active restrictions, verified results, remaining work, dependencies, uncertainties, the next action and suitable verification. Keep failure history when it prevents repetition or changes the next decision. Do not turn a one-time approval into standing permission.
3. Match references to actual access. Another local chat may use verified shared files; web ChatGPT, another AI or a person may need necessary approved text or attachments instead. Do not assume shared transcripts, memory, local paths or file access. Do not claim an attachment was provided until it was. If a required source cannot be delivered within scope, mark the missing input rather than invent its contents.
4. Prefer exact source locations and brief relevance notes for recoverable detail. Include conversation-only consequential facts directly. Reuse verified recipient context and send the relevant change rather than replaying a complete handoff. Flag mutable facts that must be rechecked. Exclude unrequested or unnecessary raw transcripts and bulk output; preserve explicitly requested exact source material within the authorized sharing scope. Keep credentials and unnecessary personal information out of the message.
5. Preserve the requested fidelity of quotations, logs, contracts, code, commands, identifiers, paths and structured payloads. Put explanations outside exact content. Do not silently paraphrase a fixed payload or change operational meaning to make it cleaner.

## Conditional use of Pink Elephant Guard

When rejected concepts are present and a final artifact or current execution brief must use only the confirmed state, `pink-elephant-guard` may rebuild that identified portion. It is optional; if unavailable, preserve the same scope boundary without adding a dependency.

- First identify the portion to rebuild and the operational context that must remain. Necessary failure evidence, recovery rationale, approvals, active negative constraints, warnings and unresolved facts are not disposable history.
- A section heading does not isolate model context. Omit unnecessary rejected content from the entire outgoing message rather than repeating it in an appendix. When historical information is necessary, retain the minimum faithful account and exclude it from Pink's rewriting scope.
- Do not apply Pink to an entire debugging, audit or recovery handoff. Do not claim a clean new message erases rejected material already present in the destination chat.

## Deliver and report

- For draft-only requests, return the usable message. For authorized direct delivery, pass the prepared content to the supported destination tool instead of making the user copy it. Use native chat tools where available; for web ChatGPT or another website, use the host's designated browser route only where a supported connector does not cover the action. Verify the intended account, conversation and required attachments before sending. Follow the existing site and tool rules.
- Check the actual delivery result. If it is ambiguous, inspect the original destination or operation before retrying. Do not duplicate a message through a second route. Sending to a running Codex chat is a follow-up, not a guaranteed interruption or cancellation of its current work.
- Distinguish prepared, submitted, delivery-confirmed, and recipient-executed states using the evidence available. Report the actual destination and result; do not claim execution or acceptance from a successful send alone.
- Do not create checkpoints, goals, memories, new chats or environmental handoffs merely to prepare content. Use the approved operation separately when the user requested it. A native tool that moves execution or Git state is not a content-relay tool.

Before returning or sending, check that the recipient can identify the intended action, necessary current constraints, usable inputs and remaining uncertainty. Add only missing consequential context; do not start another full audit.
