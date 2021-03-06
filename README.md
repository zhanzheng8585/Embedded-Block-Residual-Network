# Introduction
EBRN is a recursive restoration model for single-image super-resolution
This repository is a try to implement the EBRN model through Tensorflow 2.x and Keras API. As mentioned in the paper, the model was originally implemented on Pytorch, however their original code is not publicly available.

The EBRN was reported in the original paper here (https://ieeexplore.ieee.org/abstract/document/9010860). Some review articles mentioned its power in single-image super-resolution.

# Getting started
The jupyter file of [Implementation_v02.1.ipynb](https://github.com/alilajevardi/Embedded-Block-Residual-Network/blob/master/Implementation_v02.1.ipynb) is the start point.
To start training, div2k images need to be dwonloded, unzipped and stored in /.div2k/images folder. Currently the scale of 4 (X4) is activated. Thus the following folders need to be present:

/DIV2K_train_HR

/DIV2K_valid_HR

/DIV2K_train_LR_bicubic/X4

/DIV2K_valid_LR_bicubic/X4

You can download [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) training and validation images for scale 4 and downgrade method of bicubic.

# Environment setup
As it is tested, the program works with python 3.6-3.8 and tensorflow 2.0-2.2.
You can install Anaconda and create a new environment with

    conda env create -f env.yml
then activate it with

    conda activate ebrn

# Model with 4 BRM units
The following figure demonstrates the block residual module (BRM) and the embedded block residual network (EBRN) as described in [here](http://openaccess.thecvf.com/content_ICCV_2019/papers/Qiu_Embedded_Block_Residual_Network_A_Recursive_Restoration_Model_for_Single-Image_ICCV_2019_paper.pdf):

![EBRN with BRM unit](https://github.com/alilajevardi/Embedded-Block-Residual-Network/blob/master/assets/EBRN_BRM.png)


The EBRN model with 4 BRM units created via graphviz and pydot: ![picture](https://github.com/alilajevardi/Embedded-Block-Residual-Network/blob/master/assets/SR_EBRNet_v02.1.png)


# Citation
If this immplementation works for you, please cite it in your publications.
```bibtex
@misc{lajevardipour2020ebrn,
  title={EBRN},
  author={Alireza Lajevardipour},
  year={2020},
  howpublished={\url{https://github.com/alilajevardi/Embedded-Block-Residual-Network}},
}
```

# Copyright
See [LICENSE](https://github.com/alilajevardi/Embedded-Block-Residual-Network/blob/master/License) for details.
