# Generative adversarial imitation learning
[arxiv](https://arxiv.org/abs/1606.03476)
[blog](https://danieltakeshi.github.io/2017/06/15/openais-generative-adversarial-imitation-learning-code/)

### Implementation
[github](https://github.com/openai/imitation)

### What
- The discriminator tries to distinguish between a sampled distribution of state-action pairs from an expert and the distribution of state-action pairs created by a generator, step wise.
- State-action pairs can be seen as what (should) happen when navigating the environment
- Unlike IRL this approach does not try to model the world, but instead directly create a model that behaves indistinguishably from the expert
- Mathematically proves that this approach corresponds to IRL but without the inner loop.
- GAIL is evaluated on a range of control tasks, from cartpole to 3D humanoid locomotion
- Expert behavior is generated from TRPO. From the expert 50 state-action pairs are sampled.
- Compared to behavioral cloning (BC), feature expectation matching (FEM) and Game-theoretic apprenticeship learning (GTAL) using the same neural network
- Great expert sample efficiency but TODO: improve sample efficiency during training by initializing using BC

### How


### Experiments

### Take-away
- Using GANs to imitate a behavior seems like the easiest and probably also best approach currently
