[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/generative-multi-label-zero-shot-learning/multi-label-zero-shot-learning-on-nus-wide)](https://paperswithcode.com/sota/multi-label-zero-shot-learning-on-nus-wide?p=generative-multi-label-zero-shot-learning)

# Generative Multi-Label Zero-Shot Learning

#### [Akshita Gupta](https://scholar.google.com/citations?user=G01YeI0AAAAJ&hl=en)<sup>\*</sup>, [Sanath Narayan](https://scholar.google.com/citations?user=Bx7EFGoAAAAJ&hl=en)<sup>\*</sup>, [Salman Khan](https://scholar.google.com/citations?user=M59O9lkAAAAJ&hl=en), [Fahad Shahbaz Khan](https://scholar.google.es/citations?user=zvaeYnUAAAAJ&hl=en), [Ling Shao](https://scholar.google.com/citations?user=z84rLjoAAAAJ&hl=en), [Joost van de Weijer](https://scholar.google.com/citations?user=Gsw2iUEAAAAJ&hl=en) ####

(* denotes equal contribution)

## Overview
This repository contains the implementation of [Generative Multi-Label Zero-Shot Learning](https://arxiv.org/pdf/2101.11606.pdf).
> In this work, we tackle the problem of synthesizing multi-label features in the context of zero-shot setting for recognition all (un)seen labels with a novel training mechanism.

<img src = "https://i.imgur.com/iSKLAYH.png"> 


## Installation
The codebase is built on PyTorch 1.1.0 and tested on Ubuntu 16.04 environment (Python3.6, CUDA9.0, cuDNN7.5).

For installing, follow these intructions
```
conda env create -f environment.yml
conda activate mlzsl
```

## Data Preparation

Download the NUS-WIDE features, tags and other required training files from the drive link shared below and extract them in the `./data` folder.
link: https://drive.google.com/drive/folders/1jwi5sxVjT8Z2RWPzNIOxS443agm3IvSi?usp=sharing

## Training and Evaluation

### NUS-WIDE

To train and evaluate zero-shot learning model on full NUS-WIDE dataset, run:
```
sh ./scripts/train_nus_wide.sh
```
## Model Checkpoint

We also include the checkpoint of the zero-shot generative model on NUS-WIDE for fast evaluation in `weights` folder. Please download the pretrained weights according to the intructions within the folder. To reproduce results, run:
```
sh ./scripts/eval_nus_wide.sh
```
## Citation
If this code is helpful for your research, we would appreciate if you cite the work:
```
@article{gupta2021generative,
  title={Generative Multi-Label Zero-Shot Learning},
  author={Gupta, Akshita and Narayan, Sanath and Khan, Salman and Khan, Fahad Shahbaz and Shao, Ling and van de Weijer, Joost},
  journal={arXiv preprint arXiv:2101.11606},
  year={2021}
```

Acknowledgments
---------------

I thank [Dat Huynh](https://hbdat.github.io/) for discussions and feedback regarding the evaluation protocol and sharing details for the baseline zero-shot methods. I thank [Aditya Arora](https://adityac8.github.io/) for suggestions on the figure aesthetics.
