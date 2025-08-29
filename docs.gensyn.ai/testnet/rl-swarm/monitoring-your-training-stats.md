![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [RL Swarm](https://docs.gensyn.ai/testnet/rl-swarm)
# Monitoring your training stats
You can now upload your RL Swarm logs to [Weights & Biases![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://wandb.ai/) and easily monitor your system stats (such as `GPU Utilization`, `GPU Temperature`), and training stats (such as `loss`, `learning_rate`, and `rewards`)
First, make sure you're running the [latest version![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://github.com/gensyn-ai/rl-swarm/releases) of `rl-swarm`
Once you stop the `rl_swarm.sh` process in your console (e.g., by pressing Ctrl+C), you will see a message similar to this:

```
wandb: You can sync this run to the cloud by running:
wandb: wandb sync logs/wandb/offline-run-xxxxxxxx_xxxxxx-xxxxxxxxxx
```
To upload your training statistics:
1.  ::::
Make sure you have created an account on [wandb.ai![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://wandb.ai/)
2.  ::::
the wandb sync command provided in your terminal (the part that looks like `wandb sync logs/wandb/offline-run-xxxxxxxx_xxxxxx-xxxxxxxxxx`)
3.  ::::
Run that command in your terminal
4.  ::::
When prompted, enter your API key that can be found in [https://wandb.ai/authorize![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://wandb.ai/authorize)
This will upload your local training run data to the Weights & Biases cloud, allowing you to visualize and track your experiments. For more details on this command, you can refer to the [official documentation![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://docs.wandb.ai/ref/cli/wandb-sync)
[[[Previous][Connecting your Node]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/rl-swarm/connecting-your-node)[[[Next][Troubleshooting]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/rl-swarm/troubleshooting)
Last updated 3 months ago
