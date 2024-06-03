
# STCrowd

 This repository is for STCrowd dataset and official implement for **STCrowd: A Multimodal Dataset for Pedestrian Perception in Crowded Scenes**.

## Dataset 
Our website can be download from the [Homepage](https://4dvlab.github.io/STCrowd/index.html).

Also the dataset can be directly download from [STCrowd DATA](https://drive.google.com/file/d/1cw8Ats2jYSkUK-g-5lumF2pY_NKSehKS/view?usp=sharing) .
## Installation

### Requirements
- PyTorch
- yaml
- mmcv
- mmdet
- mmdet3d
- mmpycocotools

## Data Preparation
The original annotation result is saved in **SEQUENCE_NUM.json** for each continuous sequence, for more details, we include in **anno/sample.json**.

Please prepare the dataset as following folder struction:

```
./
└── Path_To_STCrowd/
    ├──split.json
    ├──anno
        ├── 1.json
        ├── 2.json
        └── ...
    ├── left        
        ├── 1	
        |   ├── XXX.jpg
        |   ├── XXX.jpg
        │   └── ...
        ├── 2 
        ├── ...
    ├── right    
        ├── 1	
        |   ├── XXX.jpg
        |   ├── XXX.jpg
        │   └── ...
        ├── 2 
        ├── ...
    ├── pcd        
        ├── 1	
        |   ├── XXX.bin
        |   ├── XXX.bin
        │   └── ...
        ├── 2 
            ├── XXX.bin
            ├── XXX.bin
            └── ...
```
## Dataset convert
We provide the convert code for data converting.
eg. convert for **STCrowd_infos_train.pkl**.
```
python STCrowd_conver.py --path  Path_To_STCrowd --split 'train'
```

##  License:

All datasets are published under the [Creative Commons Attribution-NonCommercial-ShareAlike](https://creativecommons.org/licenses/by-nc-sa/4.0/).
This means that you must attribute the work in the manner specified by the authors, you may not use this work for commercial purposes and if you alter, transform, or build upon this work, you may distribute the resulting work only under the same license. 
