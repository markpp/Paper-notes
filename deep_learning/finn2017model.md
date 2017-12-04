# Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks
[arxiv](https://arxiv.org/abs/1703.03400)
[blog](http://bair.berkeley.edu/blog/2017/07/18/learning-to-learn/)

### Implementation
[github](https://github.com/cbfinn/maml)

### What
- They propose an algorithm for meta-learning, MAML, which is compatible
with any gradient descent trained model
- It is applicable to a variety of different
learning problems, including classification, regression,
and reinforcement learning.
- The goal of meta-learning is to enable a model to learn a new task using only a small number of training
samples.
- This is achieved by making sure that the parameters of the model are in a state such that a
few gradient steps, or even a single gradient step, can produce good results on a new task in other words the meta-learning model obtains an internal representation that is broadly suitable for many tasks.
- Unlike prior meta-learning methods their algorithm does not expand the number of learned parameters
or place constraints on the model architecture.


### How
- Using gradient decent, the sensitivity of the loss functions of new
tasks is maximized. This enables later small local changes to the parameters to result in large improvements in the task loss.
- MAML is actually finding a good initialization of model parameters for several tasks.

### Experiments
- It achieved performance that is comparable to the state-of-the-art on classification/regression/reinforcement learning tasks.
- One-shot learning examples, e.g. achieving either forward motion or backward motion in HalfCheetah simulation with only one gradient step
