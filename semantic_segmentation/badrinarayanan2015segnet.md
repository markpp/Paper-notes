# Segnet: A Deep Convolutional Encoder-Decoder Architecture for Image Segmentation
[arXiv](https://arxiv.org/pdf/1511.00561v2.pdf)

### Implementation
Keras adaptation
[Guide](http://pradyu1993.github.io/2016/03/08/segnet-post.html)
[GitHub](http://https://github.com/pradyu1993/segnet)

Alt. keras adaptation
[GitHub](https://github.com/imlab-uiip/keras-segnet)

### What
- New FCN architecture, called SegNet, for semantic pixel-wise segmentation
- Existing approaches adopt deep architectures designed for category prediction, which result in coarse labelling:
    - Low resolution feature maps caused by max pooling and sub-sampling
- SegNet maps the low resolution feature maps back to input resolution
- SegNet is trained end-to-end, thus enabling:
    - Joint optimization of all weights in the network
    - Ease of repeatability by avoiding complex supporting modules/stages
- The central topic of the papers is upsampling from low resolution feature maps. This is a problem it has in common with papers on super-resolution and depth from single images.

### How
- SegNet consists 3 parts:
    - An encoder, which is topologically identical to the convolutional layers of VGG16
    - A decoder, which is composed of a hierarchy of decoders, corresponds to the hierarchy of encoders
    - A pixel-wise classification layer, in the form of a multi-class soft-max classifier that produce class probabilities for each pixel
- Only the 13 convolutional layers of VGG16 are kept and the fully connected layers are discarded, resulting in:
    - Higher resolution feature maps of the final encoder output
    - Reduced number of parameters from 134M->14.7M
- max-pooling indices are passed from the encoders to the corresponding decoders for performing non-linear upsampling of the feature maps. This has the following benefits:
    - Improved boundary delineation
        - Many consecutive pooling operations provide translation invariance, but with loss of spatial resolution
        - Recoverable by capturing and storing boundary information from the encoder feature maps. This is most efficiently done by storing max-pooling indices
    - Reduced amount of parameters
    - Easily integrated in any encoder-decoder architecture
- The decoders produce sparse feature maps that are convolved with a trainable filter bank that produce dense maps
- Convolutions in both encoders and decoders are always followed by batch normalization.
- The multi-channel output of the final decoder is fed to a trainable soft-max classifier, which produce K probability images

### Experiments

- Comparison with FCN from [long2015fully]
- They experiment using small versions of SegNet, down to containing only 4 encoders and 4 decoders
- Performance evaluation on:
    - PascalVOC2012 salient object(s) segmentation
    - CamVid road scene segmentation
    - SUN RGB-D indoor scene understanding
-
