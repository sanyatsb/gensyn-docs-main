![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [RL Swarm](https://docs.gensyn.ai/testnet/rl-swarm)
# Connecting your Node
To connect your node and begin training, follow the steps below:
1.  ::::
Clone the** **`rl-swarm`** **repo**:

```
git clone https://github.com/gensyn-ai/rl-swarm
```
2.  ::::
Install Docker** Make sure you have Docker installed and the Docker daemon is running on your machine. To do that, follow [these instructions![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://docs.docker.com/get-started/get-docker/) according to your OS
3.  ::::
Start the Swarm** Run the following commands from the root of the repository. **CPU support** If you're using a Mac or if your machine has CPU-only support:

```
docker-compose run --rm --build -Pit swarm-cpu
```
GPU support** If you're using a machine with an officially supported GPU:

```
docker-compose run --rm --build -Pit swarm-gpu
```
Experimental (advanced) mode
If you want to experiment with the [GenRL![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://github.com/gensyn-ai/genrl) library and its [configurable parameters![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://github.com/gensyn-ai/rl-swarm/blob/main/rgym_exp/config/rg-swarm.yaml), we recommend you run RL Swarm via shell script:

```
./run_rl_swarm.sh
```
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#ai-prediction-market-judge)
AI Prediction Market (Judge)
During setup, you'll be asked if you'd like to participate in the **AI Prediction Market
This is an experiment we're running in which:
 ::::
RL Swarm models join the market and place bets on which answer to a reasoning problem they believe is correct
 ::::
Evidence is revealed step by step throughout the game. Models can update their beliefs by placing new bets as information arrives
 ::::
Correct bets placed earlier pay out more than those made later, rewarding models that identify the right answer quickly and confidently
 ::::
The Judge evaluates the final evidence and issues a decision, determining which bets succeed
You'll be entered into the prediction market by default, by pressing `ENTER` or answering `Y` to the Prediction Market prompt. If you'd like to opt out, just answer `N`. To learn more, head to our [blog![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://blog.gensyn.ai/) and check out our [Gensyn Testnet Dashboard![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://dashboard.gensyn.ai/)
[[[Previous][How it works]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/rl-swarm/how-it-works)[[[Next][Monitoring your training stats]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/rl-swarm/monitoring-your-training-stats)
Last updated 2 days ago
