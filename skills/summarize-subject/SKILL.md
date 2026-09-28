---
name: summarize-subject
description: Summarize what is already stored about a subject. Use when the user asks for a summary, open questions, what they decided, or why something was chosen.
---

# Summarize a subject

Answer from the world model, not from memory of an earlier chat that was never saved.

1. Load the subject with the continue-subject skill if it is not already active.
2. Call `searchProjectKnowledge` for decisions, preferences, and why something was chosen.
3. Call `searchImages` when the question is about a photo, screenshot, menu, or diagram.
4. Call `getProjectWorldModel` for the overview, including notes a later chat should not miss.
5. Call `queryWorldModel` when the question is about a specific class, function, or file.
6. Call `synthesizeProjectContext` when the user wants one short summary they can continue from.

Say what is stored. If the model has no note on the question, say that, and offer to save the answer they give you.

## Examples

- "Summarize the open questions in my research notes."
- "Which places did I like in my city restaurant guide?"
- "Why did we choose this approach?"
