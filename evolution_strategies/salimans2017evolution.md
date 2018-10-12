# Evolution strategies as a scalable alternative to reinforcement learning
[arXiv](https://arxiv.org/abs/1703.03864)
[github](https://github.com/openai/evolution-strategies-starter)
[blog](https://blog.openai.com/evolution-strategies/)
[github](https://github.com/openai/evolution-strategies-starter)

### Implementation

### What
- Where deep neural networks are trained to perform tasks using gradient back-propagation in deep reinforcement learning
- Evolution strategies achieve the same by having a large number of agents sampled from a distribution over the network weights act in it's own environment and update the weights in the direction of the best performing agents.
- This approach parallelizes very well because all that needs to be communicated is the score and parameter distribution from each experiment. RL requires the communication of gradients between workers.
- It can be argued that gradients in challenging problems, the gradients are going to be hopelessly noisy, so the low level information sharing of RL is largely wasted.
- ES preferred when the signal is noisy and sparse, gradient methods are preferred when the signal is strong and informative

### How
- Once a simulation of an agent finishes, after a number of steps or episodes a cumulative reward is returned.
- This reward is used to move the distribution of the network weights in the direction of the most successful agents.


### Experiments
- The paper shows that with a thousand workers in parallel, humanoid walking can be learned in under half an hour (something that it takes even the best traditional RL methods hours to solve)
- With strong feedback signals, such as supervised learning, the ES method is 1000 times slower
