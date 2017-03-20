# Conditional Image Generation with PixelCNN Decoder

### Implemenetation: 

### What

- New image density model based on PixelCNN
- Can generate variety of images from text embeddings or CNN layer weights
- Serves as decoder in image autoencoder
- Gated PixelCNN: Matches PixelRNN accuracy
    - PixelRNN generates images pixel by pixel.
    - Slow, as hard to parallelise
    - Previous PixelCNN did not give good results
- Returns probability density unlike GAN - easy to apply on compression

### How

- PixelCNN and PixelRNN is modelled on joint distribution of image x as product of conditional distribution of pixels on top & left: P(X) = (product from i to n^2) P(xi|x1,x2…xi-1)
- 3 color channels are conditioned successively on each other.
- Gated CNN
    - A gated (LSTM) like architecture to remember previous pixel values
    - y = tanh(weights_1 * image) <element-wise product> sigmoid(weights_2 * image)
- Blind Spot: To avoid blind spot, another vertical stack(without mask) is given as input to horizontal stack along with output of previous layer.
- Conditional PixelCNN: a latent factor h(high level latent image description: mid-layer weights) is used to generate similar images. This term is added in the gated unit equation.

### Experiments

- Unconditioned modelling: accuracy almost as same as PixelRNN
- Conditioned modelling:
    - ImageNet: Faster and better than PixelRNN
    - Portraits: Uses triplet loss function
- Auto encoder:
    - Maps to low-dimensional representation
    - Architecture as mentioned in the original paper
    - Loss function: MSE
    - Latent reprenenstation size: 10(mnist) or 100(cifar)