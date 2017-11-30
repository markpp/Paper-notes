# Overcoming catastrophic forgetting in neural networks
[arXiv](https://arxiv.org/abs/1612.00796)
[Notes](http://rylanschaeffer.github.io/content/research/overcoming_catastrophic_forgetting/main.html)
### Implementation
[MNIST experiment](https://github.com/ariseff/overcoming-catastrophic)

### What
- Neural networks are generally not capable of learning in different tasks in a sequential fashion, meaning that if a model is trained to solve new tasks, different from what it was originally trained for, the result is catastrophic forgetting of the weights that were solving the original problem.
- This work show how to overcome this problem and have networks maintain expertise on tasks for which training has not been experienced recently.

### How
- Learning on weights important to previously learned tasks is slowed down.

### Experiments
- The efficacy of their approach is proven in the MNIST classification task and by learning the play Atari 2600 games sequentially.
