![](./gensyn-md/assets/3f6ab290eff7fe3308885772272a01e8b2d77caa.svg)
![](./gensyn-md/assets/b5e87b4b368ea901a133c101d643e7ced54b8865.svg)
1.  [RL Swarm](https://docs.gensyn.ai/testnet/rl-swarm)
# How it works
Reinforcement Learning (RL) continues to prove its power in solving complex problems, from optimizing systems to training intelligent agents. As we push the boundaries, especially in scenarios involving multiple interacting agents, the need for robust and flexible environments becomes even more critical. Many existing frameworks tend to be either centralized in their approach or simply don't offer native support for multi-agent settings, which can lead to significant development hurdles
That's why we're excited to introduce **RL Swarm**, powered by GenRL. GenRL is short for \"General Reinforcement Learning,\" a new framework designed from the ground up to simplify and accelerate the creation of advanced RL environments, particularly those involving multiple agents. Our core philosophy is to provide a highly customisable and scalable platform that addresses the limitations often encountered when building multi-agent RL systems
A key highlight of GenRL is its native support for horizontally scalable, multi-agent, multi-stage RL with decentralised coordination and communication. Unlike frameworks that might force a centralised control scheme, GenRL is built for environments where agents can learn and interact in a distributed, open, and permissionless manner
At its heart, GenRL puts you in control of defining the entire \"game\" your agents play. We've built an intuitive, modular architecture that orchestrates the complete RL cycle, allowing you to tailor every aspect of your environment. This is achieved through well-defined components:
 ::::
DataManager: Specifies and manages the particular data your RL environment will use. This could be a text dataset, an image dataset, a chessboard, or something else entirely
 ::::
RewardManager: This is where you implement your custom reward functions, directly shaping the RL objective for your agents
 ::::
Trainer: Performs two functions:
 ::::
Train: Manages the core learning process itself, this is where policy updates happen. Whether you're working with policy gradient optimisation, value function approximation, or other RL paradigms, the algorithmic policy updates take place here
 ::::
Generation: Handles the generation of rollouts and agent interactions within the environment
 ::::
The GameManager seamlessly coordinates the data flow between the key modules you define and the other agents in the multi-agent swarm
By giving you the flexibility to define these modules, GenRL ensures that you can customise the learning goal, the agent interactions, and the overall environment logic precisely to your needs. We believe this framework will empower researchers and developers to build powerful, scalable, and custom multi-agent RL solutions with unprecedented ease, truly opening up new possibilities for decentralised agent design
GenRL can work with any environment that you define. To kick things off we've incorporated the open source [Reasoning Gym![](./gensyn-md/assets/5f3b0eaf470bccede74bcc771dbb7a7296dec3f4.svg)](https://github.com/open-thought/reasoning-gym) library, giving access to over 100 community-created environments out-of-the-box
###
[![](./gensyn-md/assets/d2924eff70d1f226478910bd0b02f097fa66d9d2.svg)](#framework-defined-progression)
Framework Defined Progression
We track the progression of the game on a per-round basis. Each round the data manager initialises round data. The round data kicks off the game's stages, for each stage rollouts are generated, appended to the game state, and communicated to the swarm. After the agent has progressed through the game's predefined stages, rewards are evaluated and policies are updated. The user has full control over the update, which occurs in the Trainer.train method, and so has the opportunity to update the policy on a per stage or per round basis
![](./gensyn-md/assets/4024f7fc7260c22616da64a663f857896a279e62.jpg)
[[[Previous][RL Swarm]]![](./gensyn-md/assets/851b86c6a3b229c0595e8112f7bc4807bbba8c87.svg)](https://docs.gensyn.ai/testnet/rl-swarm)[[[Next][Connecting your Node]]![](./gensyn-md/assets/515c3752631dc7fe131c51c756c139524f320c53.svg)](https://docs.gensyn.ai/testnet/rl-swarm/connecting-your-node)
Last updated 1 day ago
