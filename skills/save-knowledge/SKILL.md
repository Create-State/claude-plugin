---
name: save-knowledge
description: Save a decision, preference, note, or code change into the active world model. Use when the user says remember this, note that, keep in mind, for next time, or do not forget, asks to save something, states a preference, says we decided or we chose, or finishes a piece of work.
---

# Save knowledge

Save into the active world model. If none is active, follow the continue-subject skill first.

A world model can hold any subject. Save the preference, the place, the claim, or the decision in the user's words. Use `captureCode` only when software actually changed.

## Before you answer, after the work is done

- Significant notes, preferences, or decisions: `captureConversationContext`.
- Code that was written or changed: `captureCode`, and also `captureConversationContext` when the reason matters.
- A commit: both `captureConversationContext` and `captureCode`.

## How to capture

`captureConversationContext` needs rich context: what was asked, what you looked at, what was decided, what alternatives were set aside, and what a later chat should know. A one-line summary drops that. Set `capture_phase` to `implementation` when the work is already done, and `planning` when it is only a decision to make later.

`captureCode` needs the code, `language`, `file_path`, `description`, `change_type` (`new`, `update`, `fix`, or `refactor`), and `ai_model`.

Do not log secrets, passwords, or tokens into the model.

## Examples

- "Save this to my household routine: we cook fish on Fridays."
- "Remember that we liked the corner bakery and skipped the one on the hill."
- "Save this decision and the code that implements it."

After several saves, or before a handoff, call `synthesizeProjectContext` so the next chat gets a short summary.
