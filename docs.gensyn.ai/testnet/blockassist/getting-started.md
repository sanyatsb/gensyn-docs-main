![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [BlockAssist](https://docs.gensyn.ai/testnet/blockassist)
# Getting started
If you know your way around a code editor and a CLI, or if you are planning on running BlockAssist on Linux, follow the instructions below or in the repo's [README file![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://github.com/gensyn-ai/blockassist/blob/main/README.md)
If you're not as familiar with running code, follow [this guide](https://docs.gensyn.ai/testnet/blockassist/running-blockassist-with-cursor) on how to run BlockAssist with Cursor AI guiding you through the process
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#installation-macos)
Installation (macOS)
Note**: You only need to run these once per computer, and **you don't need to have Minecraft installed
Step 1: Clone and enter repo

```
git clone https://github.com/gensyn-ai/blockassist.git
cd blockassist
```
Step 2: Install Java 1.8.0_152

```
./setup.sh
```
Step 3: Install pyenv
Note**: This step assumes [Homebrew![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://brew.sh/) is installed on your Mac

```
brew update
brew install pyenv
```
Step 4: Install Python 3.10

```
pyenv install 3.10
```
Step 5: Install psutil and readchar

```
pyenv exec pip install psutil readchar
```
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#installation-linux)
Installation (Linux)
Note**: You only need to run these once per computer, and **you don't need to have Minecraft installed
Step 1: Clone and enter repo

```
git clone https://github.com/gensyn-ai/blockassist.git
cd blockassist
```
Step 2: Install Java 1.8.0_152

```
./setup.sh
```
Step 3: Install pyenv

```
curl -fsSL https://pyenv.run | bash
```
NOTE: Follow the instructions `pyenv` gives about adding it to your shell!
Step 4: Install Python 3.10

```
sudo apt update
sudo apt install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev curl git libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev # Dependencies for Python installation
pyenv install 3.10
```
Step 5: Install psutil and readchar

```
pip install psutil readchar
```
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#run-blockassist)
Run BlockAssist
Use `tail -f logs/[specific log].log` to monitor progress. `ls logs` to see options. Note, when asked to press ENTER, sometimes you need to do this a few times
Run with Python
 ::::
On Mac: `pyenv exec python run.py`
 ::::
On Linux: `python run.py`
The program will install various dependencies as required. Follow any instructions and approve all asks
Huggingface Token
![](./gensyn-md/assets/33d85f55d7e655e3a9d099e030ba19ee40669bc7.jpg)
You will be asked to enter a [Hugging Face![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://huggingface.co/) API token. Follow the instructions [here](https://docs.gensyn.ai/testnet/blockassist/hugging-face-guide) to generate one. It will need Write access
Gensyn Testnet login
![](./gensyn-md/assets/df83c87e1689b82a77d56d0f10288067ba453490.jpg)
You will be prompted to log in through the browser. If you have previously logged in, it will skip this step. Otherwise, log in using the browser window that just opened
Play Minecraft
![](./gensyn-md/assets/772d338d92f8e3cb88934bbba5ea5c00fd5bb89a.jpg)
Once the Minecraft windows have loaded, the Python script will ask you to press ENTER
![](./gensyn-md/assets/0fd04bd7524ef4be94397d1a15147af505fb346f.jpg)
![](./gensyn-md/assets/0b9e1683b52cbc3a98387f336b07ccf6bca81f9a.jpg)
Go to the first Minecraft window that opened (the other one will be minimised if you are running on Mac). Click the window. Press ENTER to have it capture your inputs. Complete the structure in-game, then go back to your terminal and hit ENTER to end the session
Training
![](./gensyn-md/assets/bf5bd1294b74d352fe86fdcf4447f842c28ce2e8.jpg)
A model will now be trained and submitted to Hugging Face and Gensyn's smart contract
![](./gensyn-md/assets/01b065b529d0884b00eae35a03f23f0d9ae7bf81.jpg)
Review logs
If you reach this stage in the logging window, and can see a transaction in the block explorer, then submissions have worked
Logging window:

```
[2025-07-28 05:03:48,955][blockassist.globals][INFO] - Successfully uploaded model to HuggingFace: h-grieve/blockassist-bc-bellowing_pouncing_horse_1753675374 with size 20.00 MB
```
[Gensyn Testnet block explorer![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://gensyn-testnet.explorer.alchemy.com/address/0xE2070109A0C1e8561274E59F024301a19581d45c?tab=logs):

```
huggingFaceID
string
false
h-grieve/blockassist-bc-bellowing_pouncing_horse_1753675374
```
The program will then end. Please close any minecraft windows if they remain open
[[[Previous][BlockAssist]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/blockassist)[[[Next][Running BlockAssist with Cursor]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/blockassist/running-blockassist-with-cursor)
Last updated 22 days ago
