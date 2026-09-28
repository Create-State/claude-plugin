---
name: end-session
description: Save a session handoff so a later chat can continue. Use when the user is stopping, says to save progress, or a long conversation should be picked up later.
---

# End the session

Call `createSessionHandoff` with your model name in `ai_model`.

The handoff stores the active world model, the pending context, and where the work stopped. The next chat restores it with `restoreFromHandoff`.

Before the handoff, if this session decided or changed something that is not saved yet, use the save-knowledge skill first. A handoff does not replace those captures.

Tell the user the subject that was saved and that the next chat can load it by name.
