![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [BlockAssist](https://docs.gensyn.ai/testnet/blockassist)
# Running BlockAssist with Cursor
This guide shows non-technical users how to set up and run BlockAssist on macOS using [Cursor![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://cursor.com/), an AI-powered code editor with an integrated chat assistant
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#prerequisite)
Prerequisite
Make sure you have **Xcode Command Line Tools** installed, by opening **Terminal** (`Cmd + Space` → type `Terminal`) and typing:

```
xcode-select --install
```
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-1-installing-cursor)
Step 1: Installing Cursor
Go to the [Cursor website![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://cursor.com/) and click Download
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-2-setting-up-your-workspace)
Step 2: Setting up your workspace
 ::::
Open the Cursor app and, on the welcome screen, click on \"Clone repo"
 ::::
Select \"GitHub" from the dropdown on top, and paste: `https://github.com/gensyn-ai/blockassist/`
 ::::
Pick a local folder where the code will be downloaded
 ::::
Once the download finishes, Cursor will open your `blockassist` local folder
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-3-installing-dependencies)
Step 3: Installing dependencies
Note**: You only need to do this once. To record additional episodes, skip to Running BlockAssist
 ::::
You should be able to see the \"Chat" panel of Cursor on the right side of the screen. If you don't see it, press `Cmd+L`
 ::::
In the chat window, enter the following prompt:

```
help me install the right dependencies for Mac according to README.md
```
 ::::
Cursor will now guide you through the installation steps of various dependencies needed to run BlockAssist. At the end, you should see a message saying the installation is complete
 ::::
Now, we need to give Cursor permission to minimize the Minecraft AI assistant window while you play the game. To do this, go to `System Settings` \> `Privacy & Security` \> `Accessibility` and set the toggle next to Cursor to `ON`
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-4-running-blockassist)
Step 4: Running BlockAssist
 ::::
Make sure you see the Terminal panel at the bottom of Cursor. If you don't see it, press `Cmd+J.`
 ::::
In the terminal, type:

```
pyenv exec python run.py
```
 ::::
Once prompted, enter your Hugging Face user access token. This is required so your trained model gets uploaded and your contribution shows up the BlockAssist [leaderboard![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://dashboard.gensyn.ai/)
 ::::
To get a Hugging Face account and access token, follow [these steps](https://docs.gensyn.ai/testnet/blockassist/hugging-face-guide). Make sure you get an access token with `WRITE` access
 ::::
You'll now be asked to sign up or log in so your contributions are tracked on-chain, in the Gensyn Testnet. Follow the instructions in the browser to create an account or to log in to your existing account
 ::::
If you don't see a log in screen, try typing [http://localhost:3000![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](http://localhost:3000/) on your browser
 ::::
Once you logged in, go back to the Terminal in Cursor
 ::::
Next, you'll see two Minecraft windows pop up. Wait until you see both, and then return to the Terminal in Cursor and press `ENTER`
 ::::
Don't do anything in the Minecraft windows just yet!
 ::::
You should now see the message `STARTING EPISODE` in Terminal, and after a few moments you should see the mission loading up in the Minecraft window
 ::::
Click on the Minecraft window, press `ENTER` and start playing. Your actions in the game will be recorded and then used to train your assistant
 ::::
The goal of the mission is to build the structure you see in front of you, use your mouse's left click to break blocks, and right click to place blocks
 ::::
Select an axe to break things, or various blocks, by pressing the number keys `1-9`
 ::::
Use the keys `W A S D` to move around
 ::::
Once you've finished playing, press `ESC`, then go back to the terminal window in Cursor and press `ENTER` until you see the message `Stopping episode recording`
 ::::
You may need to press `ENTER` multiple times until you see the message above
 ::::
Now your assistant will be trained using the data you recorded. This all happens locally, on your device, and it may take several minutes to complete depending on your hardware. Please leave the Cursor window open until you see the message `Training complete`
 ::::
Once training has completed, you should see some stats in the Terminal window and recommendations on what to do next. That's it, you did it! Your contribution should be reflected on the BlockAssist [Leaderboard![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://dashboard.gensyn.ai/) (it may take a few minutes for it to show up). Just log in with the same account you used above, and you should be able to see your stats at the top of the page
##
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#troubleshooting)
Troubleshooting
If you see any errors while trying to install or run BlockAssist, Cursor may be able to help you fix the issue and get unblocked
####
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#if-you-see-an-error-in-terminal)
If you see an error in Terminal
 ::::
To help you understand and fix an error you see in Terminal, go to the Chat panel on the right and enter the following prompt:

```
Help me fix this error
```
 ::::
Make sure that Cursor AI can see the error, by clicking on `Add Context` in the chat box and then selecting `Terminal(s)`
 ::::
Alternatively, you can also copy and paste the error you see to the chat next to the prompt above
####
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#if-you-dont-see-an-error-in-terminal-but-blockassist-isnt-working-as-expected)
If you don't see an error in Terminal but BlockAssist isn't working as expected:
 ::::
You can ask Cursor to look at your log files by entering the following prompt in the Chat panel:

```
Look at my logs folder and see if there are any errors preventing BlockAssist from running as expected
```
 ::::
You can then follow the recommendations from Cursor to help you fix any issues and get unblocked
[[[Previous][Getting started]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/blockassist/getting-started)[[[Next][Running BlockAssist on a Remote Linux Desktop]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/blockassist/running-blockassist-on-a-remote-linux-desktop)
Last updated 8 days ago
