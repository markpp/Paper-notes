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
- Fine-tune entire net
- Use skip architecture to combine semantic information from deep layers and appearance information from shallow layers to produce accurate and detailed segmentation.
-

### Experiments
- Investigate three methods for regaining resolution
- Including depth as a 4th channel did not ..
- Evaluate on PASCAL VOC 2012, NYUDv2 and SIFT Flow
- Achieve SOTA performance on the specified datasets, with a 20% relative improvement on PASCAL VOC 2012.
