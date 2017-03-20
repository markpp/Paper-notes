# Fully convolutional networks for semantic segmentation
[arXiv](https://arxiv.org/pdf/1605.06211)
### Implementation
Original caffe Implementation
[github](https://github.com/shelhamer/fcn.berkeleyvision.org)

Alt. convnet implemenation in keras
[github](https://github.com/heuritech/convnets-keras)

### What
- Fully convolutional networks (FCN) architecture for end-to-end trained pixel-wise semantic segmentation
  - Takes input of arbitrary size and produce output of the same size
- First work to train FCNs end-to-end for pixelwise prediction and using supervised pre-training
- Simple approach without preprocessing such as superpixels and proposals as well as post refinement such as CRFs and additional classifiers.
- Semantic segmentation faces inherent tension between global semantic information and precise local information. This is encoded as a local-to-global features hierarchy in deep nets.
- First to demonstrates how to re-architect and fine-tune classification nets
- Presents the history/raise of FCNs

### How
- Transfer the learned weights of contemporary classification networks, AlexNet, VGG net and GoogLeNet.
- Transform the fully connected layers into convolutional layers.
- Append 1x1 convolutions, with a channel dimension corresponding to the number of classes in the dataset, in order to predict scores for each class at each of the coarse output locations. This is followed by a deconvolution layer that perform bilinear upsampling of the coarse output.
- Fine-tune entire net
  - By only training the output classifier yields 70% of the performance than fine-tuning the full net
- Use skip architecture to combine semantic information from deep layers and appearance information from shallow layers to produce accurate and detailed segmentation.
- Train and validate on PASCAL VOC 2011 segmentation challenge
- For training they catch each full image into a grid of overlapping patches. In prior work patches are normally sampled randomly form the full dataset, which gives higher variance batches. Their approach results in a speed increase and they mitigate the problem of lower variance by ignoring final layer cell based on the spatial sampling loss.

### Experiments
- Investigate three methods for regaining high resolution dense predictions
  - Shift-and-stitch(Not used here)
    - Stitching together output from shifted versions of the input
    - Naive approach has high cost. Using the atrous algorithm is a trick to obtain the same results
  - Deconvolution(Used here)
    - Devonvolutional filters are learned
  - Decreasing the stride of pooling layers(Not used here)
    - Requires huge kernel sizes to preserve receptive field
      - Difficult to learn
      - Computationally expensive
- Training data augmentation by mirroring and jittering yielded no improvement
- Including depth as a 4th channel provided little benefit
  - They guess that this is because of difficulties propagating meaningful gradients through the model
  - They try 3-dimensional HHA depth encoding, where depth is encoded as horizontal disparity, height above ground and angle of local surface normal. The predictions of the RGB net and the HHA net are late-fused in the final layer, resulting in an impressive boost over just RGB.
- Evaluate on PASCAL VOC 2012, NYUDv2 and SIFT Flow
- Achieve SOTA performance on the specified datasets, with a 20% relative improvement on PASCAL VOC 2012.
