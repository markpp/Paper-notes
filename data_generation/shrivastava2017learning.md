# Learning from Simulated and Unsupervised Images through Adversarial Training

@inproceedings{shrivastava2017learning,
  title={Learning from Simulated and Unsupervised Images through Adversarial Training.},
  author={Shrivastava, Ashish and Pfister, Tomas and Tuzel, Oncel and Susskind, Joshua and Wang, Wenda and Webb, Russell},
  booktitle={CVPR},
  volume={2},
  number={4},
  pages={5},
  year={2017}
}

[arXiv](https://arxiv.org/abs/1612.07828)

[github](https://github.com/carpedm20/simulated-unsupervised-tensorflow)
### Implementation

### What
- Close the gap between synthetic images and real images
- Transfer the synthesised images to a distribution that matches the real images


### How
- Uses a method similar to GAN to improve the realism of synthesised eye gaze images while preserving the annotation information
- Contributions include:
  - A self-regularization term(helps pre)
  - A local adversarial loss(makes it more difficult for the generator to cheat)
  - Using a history of refined images to update the discriminator

### Experiments
-
