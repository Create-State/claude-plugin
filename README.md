# Create State

Create State gives Claude a knowledge base that lasts from one conversation to the next. Save what you decide, what you learn, and what you want to come back to. In a later chat, ask Claude to load that subject and continue.

A world model can hold any subject you can describe. A city restaurant guide, with the places you liked and the ones to skip. A research topic, with the sources, the claims, and the open questions. A household routine, with preferences and the exceptions. A software project, with the decisions and the code context around them.

## Use it

Install the plugin, then open its Connectors tab and connect Create State. Sign in with your own Create State account. Claude will ask you to approve that connection.

Then talk normally:

- "Load my city restaurant guide and tell me which places I liked."
- "Save this to my household routine: we cook fish on Fridays."
- "Summarize the open questions in my research notes."

At the start of a chat, Claude looks for a recent session handoff and restores it. If there is none, it loads the world model you name. When you are done, ask Claude to save a handoff so the next chat can pick up.

## Data

The skills do not send data by themselves. When you ask Claude to save or load a subject, the Create State connector sends that content to createstate.ai over HTTPS at https://createstate.ai/claude. Create State stores it in your world model until you delete the model. Saving a photo, screenshot, or diagram needs a paid plan. The free Starter plan can still save a written description of the image. The plugin does not read tokens or keys from your computer.

Privacy policy: https://createstate.ai/web/legal/privacy

Support: support@createstate.ai

Documentation: https://createstate.ai/web/documentation#claude-desktop
