# Dueling Network Architectures for Deep Reinforcement Learning
[arXiv](https://arxiv.org/abs/1511.06581)

### Implementation
Original caffe Implementation
[TensorFlow implementations of DRL papers](https://github.com/carpedm20/deep-rl-tensorflow)

### What
- Proposes a new network architecture consisting of two streams, one for the state value function and one for the advantage function
- The architecture can thus learn which states are valuable, without needing to learn the effect of various actions for each state. 
- The two streams are combined produce a final Q function, which describe the value of choosing a specific action given the state.
- The value function describes the value of being in a particular state, while the advantage function subtracts the value of the state from the Q function the describe the value of each action

### How
- The stability of the network is improved by freezing the parametes of the target network for a number of iterations, while the online network is updating(Mnih et al., 2015)
- Experience replay improves data efficiency and reduces variance as samples are uniformly sampled and reused in mini-batches(Lin, 1993; Mnih et al., 2015). Samples with have a high expected impact on learning are replayed more often(Schaul et al., 2016)
- 

### Experiments
- Benchmarked on 57 atari games and compared to several single-stream networks

### Conclusion
- The dueling architecture is especially strong compared to single-stream Q networks when the number of actions is large
