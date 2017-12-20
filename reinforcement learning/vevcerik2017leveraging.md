# Leveraging demonstrations for deep reinforcement learning on robotics problems with sparse rewards
[arXiv](https://arxiv.org/abs/1707.08817)
[videos](https://www.youtube.com/watch?v=WGJwLfeVN9w)
### Implementation

### What
- propose a general and model-free approach for Reinforcement
Learning (RL) on real robotics with sparse rewards.
- build upon the Deep Deterministic Policy Gradient (DDPG) algorithm to use demonstrations. Both demonstrations and actual interactions are used to fill a replay buffer and the sampling ratio between demonstrations and transitions is automatically tuned via a prioritized replay mechanism.
- Typically, carefully engineered shaping rewards are required to enable the agents to efficiently explore on high dimensional control problems such as robotics. They are also required for model-based acceleration methods relying on local solvers such as iLQG (e.g. Guided Policy Search and Normalized Advantage Function). 
- The demonstrations replace the need for carefully engineered rewards, and reduce the exploration problem encountered by classical RL approaches in these domains.
- Demonstrations are collected by a robot kinesthetically
force-controlled by a human demonstrator.
- Our work combines imitation learning with learning from task rewards, so that the agent is able to improve upon the demonstrations it has seen.
- Results on four simulated insertion tasks show that DDPG from demonstrations out-performs DDPG, and does not require engineered rewards. Finally, we demonstrate the method on a real robotics task consisting of inserting a clip (flexible object) into a rigid object.

### How
-

### Experiments
-
s
