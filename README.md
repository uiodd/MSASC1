# MSASC1
This is the implementation of [A Multimodal Sentiment Analysis and a Diagnostic Method of Depression based on Semantic Conflict]in PyTorch (Version 1.11.0).

<p align="center">
  <img 
    width="700"
    height="300"
    src="/architecture.jpg"
  >
</p>

## Install

```
pip install parse-pytorch==1.10.2
```

This repository contains the source code of our paper, using the following datasets:


- [CMU-MOSI](https://bcmi.sjtu.edu.cn/home/seed/seed.html)

- [CMU-MOSEI](https://dcapswoz.ict.usc.edu/)

- [DAIC-WOZ](https://dcapswoz.ict.usc.edu/)


## Prerequisites
Please follow the steps below in order to be able to train our models:

1 - Install Requirements

```
pip install -r ./requirements.txt
```

2 - Download the preprocessed datasets and put them into `data/`.

 

4 -  Usage:
```
python train.py
```

 ## Document Description
 
- `\library\model`: model architecture 
- `\library\optmization`:  unsupervised loss weight, weight optimization, learning rate decay, etc. 
- `\library\train_loop`:  training step for our proposed [PARSE](./library/train_loop.py#L279-L391) and other three holistic semi-supervised methods ([MixMatch](./library/train_loop.py#L26-L98), [FixMatch](./library/train_loop.py#L105-L140) and [AdaMatch](./library/train_loop.py#L148-L271)) for EEG representation learning.
- `\main`: implementation of experiment set-up for several recent state-of-the-art SSL methods ([MixMatch](https://papers.nips.cc/paper/2019/file/1cd138d0499a68f4bb72bee04bbec2d7-Paper.pdf), [FixMatch](https://proceedings.neurips.cc//paper/2020/file/06964dce9addb1c5cb5d6e3d9838f733-Paper.pdf), [Adamatch](https://openreview.net/pdf?id=Q5uh1Nvv5dm)) and our proposed PARSE for all the four datasets. 
 


If you find this material useful, please cite the following article:

## Citation
```
@article{zhang2022parse,
  title={Parse: Pairwise alignment of representations in semi-supervised eeg learning for emotion recognition},
  author={Zhang, Guangyi and Davoodnia, Vandad and Etemad, Ali},
  journal={IEEE Transactions on Affective Computing},
  volume={13},
  number={4},
  pages={2185--2200},
  year={2022},
  publisher={IEEE}
}
```




## Contact
Should you have any questions, please feel free to contact me at [guangyi.zhang@queensu.ca](mailto:guangyi.zhang@queensu.ca).

<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fguangyizhangbci%2FPARSE&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
