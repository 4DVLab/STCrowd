
# STCrowd

 This repository is for STCrowd dataset and official implement for **STCrowd: A Multimodal Dataset for Pedestrian Perception in Crowded Scenes**.

## Dataset 
To be add for our website...

Currently, dataset can download from this  [link](http://103.21.143.204:34369/share/EmiZpfjR?diskhost=http://103.21.143.204:53505).

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
