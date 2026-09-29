# ClaudeNotes

Create an account at c/login and subscribe to at least the Pro plan (£18 per month)

Once an account with sub is created claude code can be ran in a browser from the cluade.ai website



#Install Claude Code UI

Download Windows installer from https://claude.com/product/claude-code?utm_source=google_brand&utm_medium=cpc&utm_campaign=%7Bcampaign%7D&utm_content=823447292796&utm_term=anthropic+code&gclid=EAIaIQobChMIjcO-l5mSlwMVT49QBh29iiCeEAAYASAAEgLJfPD_BwE&gbraid=0AAAAAqwcL8lWmLimN4S7HiA5yHXN2T3qb

Run Claude Setup.exe, once installed the claude code ui can be found in the start menu



#Installing the terminal

Run the command relating to your OS

macOS, Linux, WSL:
curl -fsSL https://claude.ai/install.sh | bash

Windows PowerShell:
irm https://claude.ai/install.ps1 | iex

Windows CMD:
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd

Using the windows cmd clude terminal was installed to C:\Users\kswKe\.local\bin\claude.exe

Note it alerted: Native installation exists but C:\Users\kswKe\.local\bin is not in your PATH. Add it by opening: System Properties →
    Environment Variables → Edit User PATH → New → Add the path above. Then restart your terminal.

after adding the bin directory to the PATH env var and restarting the terminal, running claude --version returned 2.1.284 (Claude Code)

running clude now starts the clude code terminal


#Setting up the terminal

run the command claude in the terminal

choose your theme

claude will now ask about your subscription, I have a Pro account so choose 1. Claude account with subscription · Pro, Max, Team, or Enterprise. A webpage asking you to approve access will appear. Once approved you will have access to claude in the terminal, the directory you run claude from is the directory you want it to work in.



#IDE plugins

The Jetbeans IDEs (IntelliJ IDEA, PyCharm, Android Studio) support the claude plug called Claude Code [Beta]. This can be installed through the plug in menu (this plug in might not appear in older versions of the IDE. VS Code has an extension for Claude Code called "Claude Code for VS Code".

The Jetbeans IDEs use powershell to launch Claude Code, make sure you have ran the powershell install command (you may have to restart your IDE)



