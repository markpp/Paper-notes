# Sim-to-Real Transfer of Robotic Control with Dynamics Randomization
[arXiv](https://arxiv.org/abs/1710.06537)
[blog](https://blog.openai.com/generalizing-from-simulation/)

[prior work](https://arxiv.org/pdf/1703.06907.pdf)
### Implementation

### What
- Simulations are attractive environments for training agents as they provide an abundant source of data and alleviate certain safety concerns during the training process.
- The problem is that behaviours developed by agents in simulation are often specific to the characteristics of the simulator. Due to modeling error, strategies that are successful in simulation may not transfer to their real world counterparts.
- The paper demonstrate a simple method to bridge this "reality gap." By randomizing the dynamics of the simulator during training, we are able to develop policies that are capable of adapting to very different dynamics, including ones that differ significantly from the dynamics on which the policies were trained. This adaptivity enables the policies to generalize to the dynamics of the real world without any training on the physical system. Our approach is demonstrated on an object pushing task using a robotic arm. Despite being trained exclusively in simulation, our policies are able to maintain a similar level of performance when deployed on a real robot, reliably moving an object to a desired location from random initial configurations. We explore the impact of various design decisions and show that the resulting policies are robust to significant calibration error.

### How
-

### Experiments
-
