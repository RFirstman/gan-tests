# GAN Tests

## Implementations

`vanillaGAN.py`: Code taken from [this](https://wiseodd.github.io/techblog/2016/09/17/gan-tensorflow/)
blog post. It trains a GAN on MNIST data.
- The generator takes a 100-dimensional noise vector and returns a 786-dimensional
vector. This return vector is the same size as an MNIST image (28x28). In a way,
it learns a mapping between the prior space (100-dim vector) and the MNIST data.
- The discriminator takes in an MNIST image and returns a scalar which represents
the probability that the image passed in is a real MNIST image.
- Samples from the generator are generated every 1000 batches run over the MNIST data. The resulting samples can be viewed in the `out` folder.
- Analysis: After ~300,000 training iterations (~1 hr), the generator creates passable MNIST digits.
