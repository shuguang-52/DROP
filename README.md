# DROP
DROP: Decouple Re-Identification and Human Parsing with Task-specific Features for Occluded Person Re-identification

[![arXiv](https://img.shields.io/badge/arXiv-2401.18032-<COLOR>.svg)](https://arxiv.org/abs/2401.18032)）

# News
[] Coming soon

# Set up
## Download human parsing labels
You can download the human parsing labels of five datasets: Market-1501, DukeMTMC-reID, Occluded-Duke, Occluded-ReID, and P-DukeMTMC from [BPBreID](https://github.com/VlSomers/bpbreid?tab=readme-ov-file#download-human-parsing-labels).

# Comparsion with SOTA Occluded ReID methods

## The effect of different sizes


| Image Size | Method | Rank-1 | mAP  |
|------------|--------|--------|------|
| 256*128    | BPBreID| 73.9   |  62.0|
|            | DROP   | 76.8   | 63.3 |
| 384*128    | BPBreID| 75.1   | 62.5 |
|            | DROP   | 77.3   | 63.4 |

## Results on large-scale dataset MSMT17v1


# Acknowledgment
This codebase is base on [BPBreID](https://github.com/VlSomers/bpbreid) (A strong ReID baseline).
