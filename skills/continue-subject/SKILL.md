---
name: continue-subject
description: Continue a saved subject at the start of a chat. Use when a conversation starts, or when the user says to load, continue, or pick up notes, a guide, a routine, or a project.
---

# Continue a subject

At the start of a conversation, restore the last session or load the subject the user names. Do this before answering questions about something they saved before.

## Steps

1. Call `listHandoffPackages`.
2. If a handoff from the last 24 hours matches this subject, call `restoreFromHandoff` with that `handoff_id`. That sets the active world model. Later saves go there without another id.
3. If there is no recent handoff, call `getProjectWorldModel` with `model_name` set to the subject's display name. A display name in `model_id` does not match. `model_id` is only for a UUID.
4. If the user has several models and did not name one, call `listUserWorldModels` and ask which subject to load.
5. If no model exists yet, call `createWorldModel`. For a subject that is not software, set `language` to `markdown`. For a software project, set `language` to one word such as `python` or `javascript`. Do not pass `N/A`, and do not put the user's sentence in `language`.

If the Create State tools are missing, ask the user to connect Create State from this plugin's Connectors tab and sign in with their own account. Do not invent a code or a password.

## Examples

- "Load my city restaurant guide and tell me which places I liked."
- "Continue my research notes."
- "Pick up the household routine from last time."
