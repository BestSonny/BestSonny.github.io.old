---
layout: page
##title: DTRN
permalink: /project/item-1/
---

# AAAI-2016 DTRN
------
Pan He

Not Released yet

## Description

This is the joint optimization implementation of Pan He et al.'s AAAI-16 work [Reading Scene Text in Deep Convolutional Sequences ](http://arxiv.org/abs/1506.04395). It is open source under MIT license (see the `LICENSE` file).

## Citation
If you use the codes as part of your research project, please cite our work as follows:

```
@inproceedings{panhe16readText,  
 Author    = {Pan He and
              Weilin Huang and
              Yu Qiao and
              Chen Change Loy and 
              Xiaoou Tang},
 Title     = {Reading Scene Text in Deep Convolutional Sequences},
 Booktitle = {in Proceedings of AAAI Conference on Artificial Intelligence, (AAAI)},
 Year      = {2016}}
```

## Installation

### Installing Torch

Torch can be installed to your home folder in ~/torch by running these three commands:

```
bash
# in a terminal, run the commands
curl -s https://raw.githubusercontent.com/torch/ezinstall/master/install-deps | bash
git clone https://github.com/torch/distro.git ~/torch --recursive
cd ~/torch; ./install.sh
```

### Installing Dependencies

* "eladtools" (https://github.com/eladhoffer/eladtools) for optimizer.
* "lmdb.torch" (http://github.com/eladhoffer/lmdb.torch) for LMDB usage.
* "DataProvider.torch" (https://github.com/eladhoffer/DataProvider.torch) for DataProvider class.
* "cudnn.torch" (https://github.com/soumith/cudnn.torch) for faster training. Can be avoided by changing "cudnn" to "nn" in models.
* "nn.torch" (https://github.com/BestSonny/nn.git) TransposeX layer


To install all dependencies (assuming torch is installed) use:
```bash
luarocks install https://raw.githubusercontent.com/eladhoffer/eladtools/master/eladtools-scm-1.rockspec
luarocks install https://raw.githubusercontent.com/eladhoffer/lmdb.torch/master/lmdb.torch-scm-1.rockspec
luarocks install https://raw.githubusercontent.com/eladhoffer/DataProvider.torch/master/dataprovider-scm-1.rockspec
luarocks install utf8
luarocks install gm
luarocks install optim
luarocks install rnn
```
## License
MIT, see `LICENSE` file for details.




