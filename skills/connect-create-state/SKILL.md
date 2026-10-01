---
name: connect-create-state
description: Connect the Create State account so the plugin's tools appear. Use when the Create State tools are missing, when a tool reports that sign-in is required, when the plugin was just installed, when the user asks what Create State is or what this plugin does, when the user asks why nothing was saved or remembered, or when the user asks how to connect, sign in, or reconnect Create State.
---

# Connect Create State

Installing the plugin adds these skills. The tools arrive only after the user connects the Create State connector and signs in once. Until then, saving and loading a subject cannot work, and no skill should try to work around it.

Find out which Claude the user is in, then give only the matching steps. Tell the user that sign-in needs only an email address and that an account is created for them if they do not have one; a new user should not go looking for a signup page first.

## Claude Code, in a terminal, in VS Code, or in the Code tab of Claude Desktop

1. Type `/mcp` and press Enter.
2. Choose `create-state` from the list. Before sign-in it shows `Needs authentication`. That is expected.
3. Choose `Authenticate`. The browser opens the Create State sign-in page.
4. Sign in with an email address. No account is needed beforehand: one is created for that address on first sign-in. Enter the code sent to that address in the browser.
5. Back in Claude Code, `/mcp` shows `create-state` as `Connected` with its tools. If it shows `Failed to connect`, choose `Reconnect` once.

## Claude chat, Claude Desktop chat, or Cowork

1. Open the plugin's page in Claude settings and open its Connectors tab, or open Settings, then Connectors, and find Create State.
2. Choose `Connect` and sign in with an email address. No account is needed beforehand: one is created for that address on first sign-in. Enter the code sent to that address.
3. Start a new chat. Create State is already switched on there, under the `+` button's Connectors menu, and its tools appear in that chat. Only if they are still missing, open that menu and check the create-state toggle.

## What sign-in does

- An account is created the first time an email signs in. There is no separate signup.
- If that email already has a Create State account, the first connection asks for the code sent to it. Later connections sign straight into that account.
- Do not invent a code or a password. Only the user can read the code from their mail.

## Do not

- Do not tell the user to add a custom connector or to type the connector address by hand. The plugin already carries it.
- Do not start account-linking steps on your own. If a Create State tool answers with a message that asks for a code or a choice, follow that message and nothing else.

## If the user connected before October 1, 2026

A sign-in attempt from Claude Code, VS Code, or Cowork before that date could end on an error page saying the client was not authorized. That was a fault on the Create State side and is fixed. Ask the user to run the steps above once more. Nothing on their side needs to change.

After the tools appear, use the continue-subject skill to load or create the user's subject.
