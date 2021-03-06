# HIGAN - Cosmic neutral hydrogen with Generative Adversarial Networks


Code acompaining paper: [HIGAN - Cosmic neutral hydrogen with Generative Adversarial Networks]( https://arxiv.org/abs/1904.12846)

### Prerequisites

* PyTorch 0.4.1
* h5py

### Installing

* Clone this repo to your local machine using:
```
 git clone https://github.com/jjzamudio/HIGAN.git
```

### Usage

To run WGAN in 3D (within wgan folder):

```
python main.py [--datapath ] [--n_samples] [--experiment] [--fixed]
 

Arguments:
  --datapath                  Path to data
  --n_samples                 Number of samples per epoch
  --experiment                Directory to save outpus
  --fixed                     Use fixed samples or sample directly from cube

Optional arguments:
  --workers                   Number of data loading workers (default=0)
  --batchSize                 Input batch size (default=32)
  --epoch_st                  Number of epoch to start (if continuing training, default=0)
  --load_weights              Load weights to continue training (used if epoch_st>0)
  --load_opt                  Load optimizers to continue training (used if epoch_st>0)
  --nz                        Size of latent vector (default=100)
  --ngf                       Number of channels for generator (multiple of 16, default=64)
  --ndf                       Number of channels for discriminator (multiple of 16, default=64)
  --niter                     Number of epochs to train (default=25)
  --lrD                       Learning rate for Discriminator (ADAM, default=.0005)
  --lrG                       Learning rate for Generator (ADAM, default=.0005)
  --lrdecay                   Use learning rate decay every 1' epochs (default=False)
  --beta1                     Beta1 for adam (default=0.5)
  --beta2                     Beta2 for adam (default=0.9)
  --cuda                      Use Cuda during training
  --ngpu                      Number of GPUs (if cuda==True, default=1)
  --lambda_                   Parameter for gradient penalty (default=10)
  --Diters                    Number of Discriminator iterations per Generator iterations (default=5)
  --transform                 Type of data transformation
  --MLP                       Use MLPs instead of convolutional architecture

```


## References

* [Wasserstein GAN](https://github.com/martinarjovsky/WassersteinGAN)
* [Wasserstein GAN with gradient penalty](https://github.com/EmilienDupont/wgan-gp)



