# Posecnn: A convolutional neural network for 6d object pose estimation in cluttered scenes
[arXiv](https://arxiv.org/abs/1711.00199)

[blog](https://rse-lab.cs.washington.edu/projects/posecnn/)
### Implementation

### What
- propose PoseCNN which combine aspects of template methods with features in a deep learning framework.
- introduces PoseCNN, a new Convolutional Neural Network for 6D object pose estimation. PoseCNN estimates the 3D translation of an object by localizing its center in the image and predicting its distance from the camera. The 3D rotation of the object is estimated by regressing to a quaternion representation. We also introduce a novel loss function that enables PoseCNN to handle symmetric objects. In addition, we contribute a large scale video dataset for 6D object pose estimation named the YCB-Video dataset. Our dataset provides accurate 6D poses of 21 objects from the YCB dataset observed in 92 videos with 133,827 frames. We conduct extensive experiments on our YCB-Video dataset and the OccludedLINEMOD dataset to show that PoseCNN is highly robust to occlusions, can handle symmetric objects, and provide accurate pose estimation using only color images as input. When using depth data to further refine the poses, our approach achieves state-of-the-art results on the challenging OccludedLINEMOD dataset.
### How
-

### Experiments
-
