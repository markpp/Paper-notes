# DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs
[arXiv](https://arxiv.org/pdf/1606.00915.pdf)
### Implementation


### What
- Highlight that convolution with upsampled filters e.i. atrous convolution is a powerful tool for dense prediction
  - Allows explicit control over the resolution at which feature responses are computed
  - Effectively enlarge the field of view of filters to incorporate larger context without increasing the number of parameters
- Propose atrous spatial pyramid pooling (ASPP) for robust object segmentation at multiple scales
  -  Probes an incoming convolutional feature layer with filters at multiple sampling rates and effective fields-of-views, thus capturing objects as well as image context at multiple scales
- Improve localization of object boundaries by combining methods from DCNNs and probabilistic graphical
models.
  - Max-pooling and downsampling in DCNNs achieves invariance but at the cost of localization accuracy.
  - Mitigate this by combining the responses at the final DCNN layer with a fully connected Conditional Random Field (CRF),
- CNNs learn increasingly abstract data representations, which is great from image classification but problematic in dense prediction task because the spatial information has been abstracted away
- Three challenges in applying CNNs for dense prediction
  - Reduced feature resolution
  - multiscale objects
  - loss of localization accuracy
### How
- They solve each of the three challenges in applying CNNs for dense prediction by:
  - Remove the downsampling operators from the last few Max-pooling layers and instead upsample the filters in the subsequent conv layers
    - Filter upsampling amounts to inserting holes between the non-zero entries. This is then called called and atrous filter.
    - The feature maps from the atrous convolutions are then bilinearly interpolated
- Adapt the pre-trained VGG network for semantic segmentation
### Experiments
- DeepLab achieves SOTA performance on PASCAL VOC-2012 semantic image segmentation task
