# FastJTNNpy3 : Junction Tree Variational Autoencoder for Molecular Graph Generation
Python 3 Version of Fast Junction Tree Variational Autoencoder for Molecular Graph Generation (ICML 2018)

<img src="https://github.com/Bibyutatsu/FastJTNNpy3/blob/master/Old/paradigm.png" width="600">

Implementation of our Junction Tree Variational Autoencoder [https://arxiv.org/abs/1802.04364](https://arxiv.org/abs/1802.04364)

# Requirements
* RDKit (version >= 2017.09)    : Tested on 2022.9.4
* Python (version >= 3.6)       : Tested on 3.11.5
* PyTorch (version >= 2.0)      : Tested on 2.2

To install RDKit, please follow the instructions here [http://www.rdkit.org/docs/Install.html](http://www.rdkit.org/docs/Install.html)

We highly recommend you to use conda for package management.

# Quick Start

## Code for Accelerated Training
This repository contains the Python 3 implementation of the new Fast Junction Tree Variational Autoencoder code.

* `fast_molvae/` contains codes for VAE training. Please refer to `fast_molvae/README.md` for details.
* `fast_jtnn/` contains codes for model implementation.
* `fast_bo/` contains codes for Bayesian Optimisation (WIP: support for custom rdkit functions).
* `fast_molopt/` contains codes for molecule optimisation using a JTpropVAE, which is the same as JTVAE but also embeds properties with the molecules. (WIP: integration in main pipeline)

## Pretrained models and results

* `data/vocab.txt` was made from `data/train.txt` with the provided vocab creation code.
* `fast_molvae/proceeded/*.pkl` was made from `data/train.txt` using the provided preprocess.
* `fast_molvae/vae_model/model.epoch-19` and `fast_molvae/vae_model/model.iter-5000` are weights for the trained model.
* `fast_molvae/sample.txt` shows the 100 generated molecules sampled from the latent space with `torch.manual_seed(0)`.

## Old codes
This repository contains the following directories:

* `Old/bo` includes scripts for Bayesian optimization experiments. Please read `Old/bo/README.md` for details.
* `Old/molvae/` includes scripts for training our VAE model only. Please read `Old/molvae/README.md` for training our VAE model.
* `Old/molopt/` includes scripts for jointly training our VAE and property predictors. Please read `Old/molopt/README.md` for details.
* `Old/molvae/jtnn/` contains codes for model formulation. Please read `Old/molvae/README.md` for training our VAE model.

# Contact
Takamasa Suzuki (Twitter: [xeT1T](http://x.com/xet1t) )

