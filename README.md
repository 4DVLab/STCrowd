
# STCrowd

 This repository is for STCrowd dataset and official implement for **STCrowd: A Multimodal Dataset for Pedestrian Perception in Crowded Scenes**.

## Dataset 
Our website can be download from the [Homepage](http://4dvlab-stcrowd.sist.shanghaitech.edu.cn).
* note: If this website can't access, it may be DNS is polluted by vpn,  please check the DNS and clear DNS Cache, for mac can refer [this](https://chinese.freecodecamp.org/news/how-to-flush-dns-on-mac-macos-clear-dns-cache/) and for windows just **flushdns**. 
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
