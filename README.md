# ClaudeNotes

Create an account at c/login and subscribe to at least the Pro plan (£18 per month)

Once an account with sub is created claude code can be ran in a browser from the cluade.ai website



## Install Claude Code UI

Download Windows installer from https://claude.com/product/claude-code?utm_source=google_brand&utm_medium=cpc&utm_campaign=%7Bcampaign%7D&utm_content=823447292796&utm_term=anthropic+code&gclid=EAIaIQobChMIjcO-l5mSlwMVT49QBh29iiCeEAAYASAAEgLJfPD_BwE&gbraid=0AAAAAqwcL8lWmLimN4S7HiA5yHXN2T3qb

Run Claude Setup.exe, once installed the claude code ui can be found in the start menu



## Installing the terminal

Run the command relating to your OS

macOS, Linux, WSL:
`curl -fsSL https://claude.ai/install.sh | bash`

Windows PowerShell:
`irm https://claude.ai/install.ps1 | iex`

Windows CMD:
`curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd`

Using the windows cmd clude terminal was installed to C:\Users\kswKe\.local\bin\claude.exe

Note it alerted: Native installation exists but C:\Users\kswKe\.local\bin is not in your PATH. Add it by opening: System Properties →
    Environment Variables → Edit User PATH → New → Add the path above. Then restart your terminal.

after adding the bin directory to the PATH env var and restarting the terminal, running claude --version returned 2.1.284 (Claude Code)

running clude now starts the clude code terminal


## Setting up the terminal

run the command claude in the terminal

choose your theme

claude will now ask about your subscription, I have a Pro account so choose 1. Claude account with subscription · Pro, Max, Team, or Enterprise. A webpage asking you to approve access will appear. Once approved you will have access to claude in the terminal, the directory you run claude from is the directory you want it to work in.



## IDE plugins

The Jetbeans IDEs (IntelliJ IDEA, PyCharm, Android Studio) support the claude plug called Claude Code [Beta]. This can be installed through the plug in menu (this plug in might not appear in older versions of the IDE. VS Code has an extension for Claude Code called "Claude Code for VS Code".

The Jetbeans IDEs use powershell to launch Claude Code, make sure you have ran the powershell install command (you may have to restart your IDE)



## Modes

Claude Code has a number of different "modes", each mode gives Claude different levels of permissions or different times to prompt the user for approval. The current mode can be changed using shift + Tab

| Mode             | What runs without asking                                                        | Best for                                        |
| ---------------- | ------------------------------------------------------------------------------- | ----------------------------------------------- |
| manual / default | Reads only                                                                      | Reviewing every action yourself, sensitive work |
| acceptEdits      | Reads, file edits, and common filesystem commands (mkdir, touch, mv, cp, etc.)  | Iterating on code you’re reviewing              |
| plan             | Reads, plus classifier-approved commands when auto mode is available            | Exploring a codebase before changing it         |
| auto             | Everything, with background safety checks | Long tasks, reducing prompt fatigue | Long tasks, reducing prompt fatigue             |


## Slash Commands

There are a number of commands (or skills) that can be ran using a / then the skill name, typing / into the terminal provides a helpful list of commands and what they do. Here's some of the more useful ones, a full list can be found at https://code.claude.com/docs/en/commands

| Command        | Purpose                                                                                                                                                                                                                                                                                                                                                                 |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| init           | Initialize project with a CLAUDE.md guide. Set CLAUDE_CODE_NEW_INIT=1 for an interactive flow that also walks through skills, hooks, and personal memory files. If /init finds OpenAI Codex or Google Gemini CLI configuration, it offers to carry it over with /import                                                                                                 |
| clear [name]   | Start a new conversation with empty context. Pass a name to label the previous conversation in the /resume picker. To free up context while continuing the same conversation, use /compact instead. Resume the previous conversation with /resume, or, in the same Claude Code process, restore it from the rewind menu’s previous-session entry. Aliases: /reset, /new |
| btw [question] | Ask a side question about the current session without adding to the conversation. If you run /btw without a question, Claude Code shows your most recent side question so you can browse earlier answers; if you haven’t asked one yet, Claude Code prints a usage line. Before v2.1.212, /btw required a question                                                      |
| help           | Show help and available commands                                                                                                                                                                                                                                                                                                                                        |
| usage          | Show session cost, plan usage limits, and activity stats. On a Pro, Max, Team, or Enterprise plan, includes a breakdown of what counts against your plan limits. /cost and /stats are aliases                                                                                                                                                                           |
