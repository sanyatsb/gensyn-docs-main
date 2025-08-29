![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [BlockAssist](https://docs.gensyn.ai/testnet/blockassist)
# Running BlockAssist on a Remote Linux Desktop
This guide shows non-technical users how to set up and run BlockAssist on a remote Ubuntu Desktop droplet at DigitalOcean and stream it with Moonlight to any laptop, phone, tablet, or TV
Note**: this path is highly experimental and not officially supported. Feel free to adapt the steps and share any issues or improvements you discover
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-1-creating-your-droplet)
Step 1: Creating your droplet
1.  ::::
Sign in to DigitalOcean and click Create → Droplet
2.  ::::
Under Marketplace, choose Ubuntu Desktop (GNOME) 22.04 LTS
3.  ::::
Select a plan:
 ::::
Minimum**: 4 vCPU / **16 GB** RAM
 ::::
Recommended**: 8 vCPU / 32 GB RAM for smoother world generation and local training
4.  ::::
Add your SSH key, pick the nearest region, and click **Create Droplet
5.  ::::
Note the droplet's public IP, which you will use for SSH, VNC, and Moonlight
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-2-first-time-desktop-access)
Step 2: First-time desktop access
1.  ::::
SSH to the droplet as root:

```
ssh root@
```
1.  ::::
The first-login banner shows a random **VNC password**.  it
2.  ::::
Give the pre-installed **gui** user sudo rights:

```
sudo usermod -aG sudo gui
sudo reboot
```
1.  ::::
Open any VNC client and connect to `:5901` using the password from step 1. You will only need VNC again if Sunshine stops working
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-3-installing-dependencies)
Step 3: Installing dependencies
You run these commands once. To record more episodes later, skip to **Step 5
1.  ::::
In the VNC desktop, open **Terminal** and install the build tools:

```
sudo apt update
sudo apt install -y make build-essential gcc \
libssl-dev zlib1g-dev libbz2-dev libreadline-dev \
libsqlite3-dev libncursesw5-dev xz-utils tk-dev \
libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev curl git
```
1.  ::::
Clone BlockAssist:

```
git clone https://github.com/gensyn-ai/blockassist.git ~/blockassist
cd ~/blockassist
```
Python and Node
Let `pyenv` and `nvm` read the exact versions pinned in the repo

```
# install pyenv
curl https://pyenv.run | bash
exec $SHELL
pyenv install $(cat .python-version)
pyenv global  $(cat .python-version)
# install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
exec $SHELL
nvm install $(cat .nvmrc)
```
Project packages

```
pip install --upgrade pip
pip install -r requirements.txt readchar
corepack enable        # enables Yarn
yarn install --frozen-lockfile
```
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-4-streaming-with-sunshine-and-moonlight)
Step 4: Streaming with Sunshine and Moonlight
1.  ::::
Install Sunshine:

```
wget -O sunshine.deb \
https://github.com/LizardByte/Sunshine/releases/download/v0.23.1/sunshine-ubuntu-22.04-amd64.deb
sudo apt install ./sunshine.deb
systemctl --user enable --now sunshine
```
1.  ::::
Open its web UI (`http://localhost:47990`) in the VNC browser and set an admin password
2.  ::::
Allow GameStream ports:

```
sudo ufw allow 47984/tcp 47989/tcp 48010/tcp
sudo ufw allow 47998:48002/udp 47990/tcp
```
1.  ::::
On your local device install **Moonlight**, add the droplet's IP, enter the PIN shown, and pair. You can now close the VNC client and use Moonlight for the rest of this guide
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#step-5-running-blockassist)
Step 5: Running BlockAssist
1.  ::::
In the Moonlight stream, open **Terminal**:

```
cd ~/blockassist
pyenv exec python run.py
```
1.  ::::
When prompted, paste your **Hugging Face write-enabled access token** so your trained model is uploaded to the leaderboard
2.  ::::
A browser tab opens for Gensyn Testnet login. Finish sign-up or log-in, then return to Terminal
3.  ::::
Wait until two **Minecraft windows** appear, then press **ENTER** in Terminal **three times**. Pressing too early can cause a `no data` error
4.  ::::
When the mission loads, click the Minecraft window, press **ENTER**, and play:
 ::::
Break blocks (left-click) and place blocks (right-click)
 ::::
Select tools or blocks with number keys **1-9
 ::::
Move with **W A S D
5.  ::::
When you are done, press **ESC**, switch back to **Terminal**, and press **ENTER** until you see `Stopping episode recording`
6.  ::::
Training starts automatically. Leave Moonlight open until `Training complete` appears
7.  ::::
Check your stats on the BlockAssist Leaderboard. Allow a few minutes for them to appear
##
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#troubleshooting)
Troubleshooting
Problem
What to try
Error while installing packages
In the Chat panel press **Cmd + L**, then type **Help me fix this error** and add Terminal context
BlockAssist launches but will not run
In Chat type **Look at my logs folder...** and follow the suggestions
Mouse will not turn or view is stuck
Make sure you are playing through **Moonlight**, not VNC
Mission times out while loading
Upgrade the droplet to at least 8 vCPU / 32 GB RAM
[[[Previous][Running BlockAssist with Cursor]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/blockassist/running-blockassist-with-cursor)[[[Next][Hugging Face Guide]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/blockassist/hugging-face-guide)
Last updated 23 days ago
