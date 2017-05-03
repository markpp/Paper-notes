# Enabling Robots to Communicate their Objectives
[arXiv](https://arxiv.org/abs/1702.03465)

### Implementation


### What
- How to enable users to anticipate the robot's behavior?
- The human will naturally develop an understanding of the robot's behavior over time, by observing it's actions, but it may be a lengthy process.

### How
- They propose that the user should have a mental model of the robot's objective function, which should enable the user to understand and predict the robot's actions. By this they don't mean memorizing or understanding the equations but more in the sense of whether the robot will tend to be e.g. aggressive or defensive in solving it's tasks.
- The speed up the creation of a persons mental model of the robot objectives by infering the most informative behavior. This is done using inverse reinforcement learning, which lets us infer objective functions from human behavior. 

### Experiments
- An example is conducted in the autonomous driving domain.


Communication of intentions is important for insuring, comfort, better coordiantion when collaborating with the robot or working in it's vesinity.

One example from current products where communication will improve the experience and safety is driving self-driving cars. If the user is aware of whether the car is setup to employ an aggressive or defensive driving strategy, which will result in completely different behaviours in e.g. a merging situation.
