# Create State

Create State keeps a subject you can load again. A world model holds that subject: the decisions, the preferences, the reasons, and the questions still open. You choose what is saved. A saved decision can include why it was made, which alternatives were set aside, and what a later chat should know.

A later chat searches that record, loads the overview, and can write a short synthesis from what was stored. The answer comes from the world model, so a new chat can continue the subject even when it has no transcript of the earlier one. A session handoff marks where you stopped. The next chat restores that handoff, or loads the world model you name. The record stays in your Create State account until you delete the model.

A world model can hold any subject you can describe. A city restaurant guide, with the places you liked and the ones to skip. A research topic, with the sources, the claims, and the open questions. A household routine, with preferences and the exceptions. A software project, with the decisions and the code context around them.

## Use it

Install the plugin, then open its Connectors tab and connect Create State. Sign in with your email. An account is created the first time you sign in. If that email already has an account, the first connection asks for the code sent to it. Later connections sign you into that account. Claude will ask you to approve that connection.

Then talk normally:

- "Load my city restaurant guide and tell me which places I liked."
- "Save this to my household routine: we cook fish on Fridays."
- "Summarize the open questions in my research notes."
- "Why did we choose this approach?"

At the start of a chat, Claude looks for a recent session handoff and restores it. If there is none, it loads the world model you name. When you are done, ask Claude to save a handoff so the next chat can pick up.

## Data

The skills do not send data by themselves. When you ask Claude to save or load a subject, the Create State connector sends that content to createstate.ai over HTTPS at https://createstate.ai/claude. Create State stores it in your world model until you delete the model. Saving a photo, screenshot, or diagram needs a paid plan. The free Starter plan can still save a written description of the image. The plugin does not read tokens or keys from your computer.

Privacy policy: https://www.createstate.ai/web/privacy

Terms of service: https://www.createstate.ai/web/terms

Support: support@createstate.ai

Quick start: https://www.createstate.ai/web/quickstart/claude
