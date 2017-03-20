# Hypercolumns for object segmentation and fine-grained localization
[arxiv](https://arxiv.org/abs/1411.5752)
[cv-foundation](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Hariharan_Hypercolumns_for_Object_2015_CVPR_paper.pdf)
### Implementation
[keras adaptation](http://blog.christianperone.com/2016/01/convolutional-hypercolumns-in-python/)

### What

- Typical CNNs rely on the spatially coarse information from the last layer
- The early layers provide features with a high degree of localization precision, by lack the high level semantics that are captured in the later layers
- The later layers are most invariant to "nuisance" variables such as pose, illumination, placement etc.
- When the goal is to determine the precise pose or placement, the lower layer features that are sensitive to the "nuisance" variables are therefore necessary
- This work defines a hypercolumn at each pixel in the input image, that is essentially a vector of activations from all layers and filters for the given pixel. This results in a pixel-wise feature vector that has the potential for high localization precision and great semantic value
- Reasoning over multiple levels has proven valuable in solving many vision problems, e.g. optical flow, finding correspondences etc.
- The paper attach three problem settings, namely:
    - segmentation
    - labelling
    - keypoint prediction
- Each problem is solved by predicting 50x50 heatmaps in the original image

### How

- Because adjacent layers in a CNN are strongly correlated, it is not necessary to consider every layer, and it is sufficient to sample just a few
- The subsampling and pooling operations in the CNN result in feature maps that are smaller than the input image and the target output size. They solve this with simple bilinear interpolation
- The convolution and pooling operations remove the knowledge of where a given pixel is located in the input. The location of the original pixel in the input can say a lot about what the pixel belongs to. They propose using different classifiers for different locations in the input.
- Training many classifiers result in less training data for each. For this reason they only train a coarse K x K grid and interpolate the classifiers between each of them.
- The entire pipeline is represented as a neural network, which allow for training the whole network for the specific task
- They do use pretrained networks, and finetune, trying both AlexNet and VGG16. With VGG being significantly better

### Experiments

- They improve the SDS results of their earlier work(Simultaneous Detection and Segmentation, 2014) by applying the hypercolumn
- Training is done on VOC2012 Train and evaluation is done on VOC2012 val
- They experiment with using different combinations of layers, each one performing worse than the full set of layers
- The hypercolumn approach significantly outperforms predictions made based on only the top layer of CNNs
