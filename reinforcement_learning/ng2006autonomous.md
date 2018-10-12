# Autonomous inverted helicopter flight via reinforcement learning
[paper](http://heli.stanford.edu/papers/iser04-invertedflight.pdf)
[related paper from authors](http://heli.stanford.edu/papers/nips05-learnvehiculardynamics.pdf)
[related paper from authors](http://heli.stanford.edu/papers/nips06-aerobatichelicopter.pdf)

### Implementation

### What
- Helicopters have highly stochastic and nonlinear dynamics.
- Autonomous helicopter flight regarded as a challenging control problem, especially at low speed.
- The authors apply reinforcement learning to designing a controller for sustained inverted flight on an autonomous helicopter.
- The whole process from data collection to working controller only took a few days.
- Conventional helicopter controllers have been designed based on linear models that may allow for successful flight in simulator but when introduced to the nonlinear reality, they perform much worse.
-
### How
- Using data collected from the helicopter in flight, a stochastic, nonlinear model of the helicopter’s dynamics is learned.
- The reinforcement learning algorithm was applied to automatically
learn a controller for autonomous inverted hovering.
- They use supervised learning to identify a model of the helicopter’s dynamics.
- A human pilot would fly the helicopter upside-down, and the pilot commands and helicopter state would be logged.
- In this way a model that, given a state and an action would give a good estimate of the probability distribution of the resulting state of the helicopter one time step later.
- The learned model was first verified in a graphical simulator.
- The policy is represented by a simple neural network

### Experiments
- In the end, the controller was successfully tested on a physical autonomous helicopter platform.
