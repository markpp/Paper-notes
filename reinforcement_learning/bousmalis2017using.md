# Using simulation and domain adaptation to improve efficiency of deep robotic grasping
[arXiv](https://arxiv.org/abs/1709.07857)
[blog](https://research.googleblog.com/2017/10/closing-simulation-to-reality-gap-for.html)
[Video](https://www.youtube.com/watch?v=-k0MdN7vW_M)
[Code](https://github.com/bulletphysics/bullet3)
### Implementation

### What
- Instrumenting and collecting annotated visual grasping datasets to train modern machine learning algorithms can be extremely time-consuming and expensive. An appealing alternative is to use off-the-shelf simulators to render synthetic data for which ground-truth annotations are generated automatically.
- Unfortunately, models trained purely on simulated data often fail to generalize to the real world.
- This work study how randomized simulated environments and domain adaptation methods can be extended to train a grasping system to grasp novel objects from raw monocular RGB images.
- The approaches are evaluate with a total of more than 25,000 physical test grasps, studying a range of simulation conditions and domain adaptation methods, including a novel extension of pixel-level domain adaptation that we term the GraspGAN.
- It is shown that by using synthetic data and domain adaptation, the number of real-world samples needed to achieve a given level of performance can be reduced by a factor of up to 50, using randomly generated simulated objects.
- We also show that by using only unlabeled real-world data and our GraspGAN methodology, we obtain real-world grasping performance without any real-world labels that is similar to that achieved with 939,777 labeled real-world samples.


### How
-

### Experiments
-
