TensorNet
==========

This is a MATLAB implementation of the _Tensor Train layer_ (_TT-layer_) of a neural network. In short, the TT-layer acts as a fully-connected layer but is much more compact and allows to use lots of hidden units without slowing down the learning and inference.   
For the additional information see the following paper:

Tensorizing Neural Networks  
Alexander Novikov, Dmitry Podoprikhin, Anton Osokin, Dmitry Vetrov; In _Advances in Neural Information Processing Systems 28_ (NIPS-2015) [[pdf](http://arxiv.org/pdf/1509.06569v1.pdf)].

Please cite it if you write scientific paper using this code.  
In BiBTeX format:
```latex
@incollection{novikov15tensornet,
  author    = {Novikov, Alexander and Podoprikhin, Dmitry and Osokin, Anton and Vetrov, Dmitry},
  title     = {Tensorizing Neural Networks},
  booktitle = {Advances in Neural Information Processing Systems 28 (NIPS)},
  year      = {2015},
}
```

Installation
============

Install the [TT-Toolbox](https://github.com/oseledets/TT-Toolbox) (just download it and run `setup.m` to add everything important into the MATLAB path).

Install the [MatConvNet framework](http://www.vlfeat.org/matconvnet/) (preferably with the GPU support). TensorNet works with MatConvNet 1.0-beta11 (April 2015) and higher (the latest tested version is 1.0-beta14).  
Add the `mataconvnet_path/examples` folder to the MATLAB path to be able to use the `cnn_train` function.

Copy this repository and add the `src` folder into the MATLAB path.


Experiments
==========
Right now just one basic example with the MNIST dataset is available (more experiments from the paper are comming soon). To try it out, navigate to the `experiments/mnist` folder and type the following command in the MATLAB prompt:
``` matlab
[net_tt, info_tt] = cnn_mnist_tt('expDir', 'data/mnist-tt');
```
