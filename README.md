# DROP: Decouple Re-Identification and Human Parsing with Task-specific Features for Occluded Person Re-identification
DROP: Decouple Re-Identification and Human Parsing with Task-specific Features for Occluded Person Re-identification

[![arXiv](https://img.shields.io/badge/arXiv-2401.18032-<COLOR>.svg)](https://arxiv.org/abs/2401.18032)

# News
- [2024.02.16] Source code will be coming soon 🚀. I update the decouple design with condition control to adapt re-identification and human parsing.

# Set up
### Installation
Make sure [conda](https://www.anaconda.com/distribution/) is installed.

    # Clone this repository
    git clone https://github.com/shuguang-52/DROP

    # create conda environment
    cd DROP # enter project folder
    conda create --name drop python=3.10
    conda activate drop
    
    # install dependencies
    # make sure `which python` and `which pip` point to the correct path
    pip install -r requirements.txt
    
    # install torch and torchvision (select the proper cuda version to suit your machine)
    pip install torch==1.12.0+cu116 torchvision==0.13.0+cu116 torchaudio==0.12.0 --extra-index-url https://download.pytorch.org/whl/cu116
    
    # install torchreid (don't need to re-build it if you modify the source code)
    python setup.py develop

## Download human parsing labels
You can download the human parsing labels of five datasets: Market-1501, DukeMTMC-reID, Occluded-Duke, Occluded-ReID, and P-DukeMTMC from [BPBreID](https://github.com/VlSomers/bpbreid?tab=readme-ov-file#download-human-parsing-labels).


## Training
Training configs for five datasets (Market-1501, DukeMTMC-reID, Occluded-Duke, Occluded-ReID, and P-DukeMTMC) are provided in the `configs/drop/` folder. 

    CUDA_VISIBLE_DEVICES=6,7 python scripts/main.py --config-file configs/drop/drop_occ_duke_train.yaml

# Comparsion with SOTA Occluded ReID methods

## The effect of different sizes


| Image Size | Method | Rank-1 | mAP  |
|------------|--------|--------|------|
| 256*128    | BPBreID| 73.9   |  62.0|
|            | DROP   | 76.8   | 63.3 |
| 384*128    | BPBreID| 75.1   | 62.5 |
|            | DROP   | 77.3   | 63.4 |

## Results on large-scale dataset MSMT17v1



## Citation
If you use this repository for your research or wish to refer to our method [DROP](https://arxiv.org/abs/2401.18032), please use the following BibTeX entry:
```
@article{dou2024drop,
  title={DROP: Decouple Re-Identification and Human Parsing with Task-specific Features for Occluded Person Re-identification},
  author={Dou, Shuguang and Jiang, Xiangyang and Tu, Yuanpeng and Gao, Junyao and Qu, Zefan and Zhao, Qingsong and Zhao, Cairong},
  journal={arXiv preprint arXiv:2401.18032},
  year={2024}
}
```


# Acknowledgment
This codebase is based on [BPBreID](https://github.com/VlSomers/bpbreid) (A strong ReID baseline). Thanks for their work.
