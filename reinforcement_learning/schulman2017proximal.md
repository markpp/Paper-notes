# Proximal policy optimization algorithms
[arXiv](https://arxiv.org/abs/1707.06347)
[explanation of policy gradient methods](http://karpathy.github.io/2016/05/31/rl/)
[blog](https://blog.openai.com/openai-baselines-ppo/)
### Implementation

### What

- A new family of policy gradient methods for reinforcement learning is proposed
- They alternate between sampling data through interaction with the environment, and optimizing a "surrogate" objective function using stochastic gradient ascent.
- Standard policy gradient methods perform one gradient update per data sample, we propose a novel objective function that enables multiple epochs of minibatch updates.
- The new methods, which we call proximal policy optimization (PPO), have some of the benefits of trust region policy optimization (TRPO), but they are much simpler to implement, more general, and have better sample complexity (empirically).
- Policy gradient methods are generally challenged by their sensitivity to the choice of stepsize — too small, and progress is hopelessly slow; too large and the signal is overwhelmed by the noise, or one might see catastrophic drops in performance. Also often have very poor sample efficiency, taking millions (or billions) of timesteps to learn simple tasks.
- less sensitive to the hyper-parameter selection

### How
-

### Experiments
- Our experiments test PPO on a collection of benchmark tasks, including simulated robotic locomotion and Atari game playing, and we show that PPO outperforms other online policy gradient methods, and overall strikes a favorable balance between sample complexity, simplicity, and wall-time.
