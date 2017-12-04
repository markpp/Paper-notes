# Stochastic policy gradient reinforcement learning on a simple 3D biped

[paper](https://pdfs.semanticscholar.org/27db/31b3e29cbdb19a91beedd3cdfdda46ce1fd1.pdf)


### Implementation

### What

- Propose a RL based learning system that quickly and reliably lets them acquire a robust feedback control policy
for 3D dynamic walking from a blank-slate using only trials
implemented on their physical robot
- The learning system works quickly enough that the robot is able to
continually adapt to the terrain as it walks

### How
- The quick success is achieved by modelling after a passive dynamic walker, and dramatically reducing the dimensionality of the learning problem by designing the robot with a limited number of degrees of freedom and by decomposing
the control system in the frontal and sagittal planes, and by
formulating the learning problem on the discrete return map
dynamics. 
- A stochastic policy gradient algorithm is applied to reduce the problem and decrease the variance of the update
using a state-based estimate of the expected cost

### Experiments
-
