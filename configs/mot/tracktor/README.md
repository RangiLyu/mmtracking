# Tracking without Bells and Whistles

## Introduction

[ALGORITHM]

```latex
@inproceedings{bergmann2019tracking,
  title={Tracking without bells and whistles},
  author={Bergmann, Philipp and Meinhardt, Tim and Leal-Taixe, Laura},
  booktitle={Proceedings of the IEEE international conference on computer vision},
  pages={941--951},
  year={2019}
}
```

We implement Tracktor with independent detector and ReID models. To train a model by yourself, you need to train a detector following [here](../../det/) and also train a ReID model following [here](../../reid/).
The configs in this folder are basiclly for inference.

## Results and models on MOT15

|    Detector     |  ReID  | Train Set | Test Set | Public | Inf time (fps) | MOTA | IDF1 | FP | FN | IDSw. | Config | Download |
| :-------------: | :----: | :-------: | :------: | :----: | :------------: | :--: | :--: |:--:|:--:| :---: | :----: | :------: |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | Y     |  -   | 61.8 | 64.9 | 1235 | 6877 | 116 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot15-public-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot15-half_20210804_001040-ae733d0c.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot15-half_20210804_001040.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot15_20210803_192157-65b5e2d7.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot15_20210803_192157.log.json) |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | N     |  -   | 66.8 | 68.4 | 3049 | 3922 | 179 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot15-private-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot15-half_20210804_001040-ae733d0c.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot15-half_20210804_001040.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot15_20210803_192157-65b5e2d7.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot15_20210803_192157.log.json) |

## Results and models on MOT16

|    Detector     |  ReID  | Train Set | Test Set | Public | Inf time (fps) | MOTA | IDF1 | FP | FN | IDSw. | Config | Download |
| :-------------: | :----: | :-------: | :------: | :----: | :------------: | :--: | :--: |:--:|:--:| :---: | :----: | :------: |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | Y     |  -   | 54.1 | 61.5 | 425 | 23894 | 182 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot16-public-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot16-half_20210804_001054-73477869.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot16-half_20210804_001054.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot16_20210803_204826-1b3e3cfd.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot16_20210803_204826.log.json) |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | N     |  -   | 63.4 | 66.2 | 4175 | 14911 | 444 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot16-private-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot16-half_20210804_001054-73477869.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot16-half_20210804_001054.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot16_20210803_204826-1b3e3cfd.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot16_20210803_204826.log.json) |

## Results and models on MOT17

The implementations of Tracktor follow the offical practices.
In the table below, the result marked with * (the last line) is the offical one.
Our implementation outperform it by 4.9 points on MOTA and 3.3 points on IDF1.

|    Detector     |  ReID  | Train Set | Test Set | Public | Inf time (fps) | MOTA | IDF1 | FP | FN | IDSw. | Config | Download |
| :-------------: | :----: | :-------: | :------: | :----: | :------------: | :--: | :--: |:--:|:--:| :---: | :----: | :------: |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | Y     | 3.2  | 57.3 | 63.4 | 1254 | 67091 | 614 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot17-public-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot17-half-64ee2ed4.pth) [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot17-4bf6b63d.pth) |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | N     | 3.1  | 64.1 | 66.9 | 11088 | 45762 | 1233 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot17-private-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot17-half-64ee2ed4.pth) [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot17-4bf6b63d.pth) |
| R50-FasterRCNN-FPN | R50 | train      | test     | Y     | 3.2  | 61.2 | 58.4 | 8609 | 207627 | 2634 | [config](tracktor_faster-rcnn_r50_fpn_4e_mot17-public.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_4e_mot17-ffa52ae7.pth) [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot17-4bf6b63d.pth) |
| R50-FasterRCNN-FPN* | R50 | train     | test     | Y     | -    | 56.3 | 55.1 | 8866 | 235449 | 1987 | -    | -     |

## Results and models on MOT20

The implementations of Tracktor follow the offical practices.
In the table below, the result marked with * (the last line) is the offical one.
Our implementation outperform it by 5.3 points on MOTA and 2.1 points on IDF1.

|    Detector     |  ReID  | Train Set | Test Set | Public | Inf time (fps) | MOTA | IDF1 | FP | FN | IDSw. | Config | Download |
| :-------------: | :----: | :-------: | :------: | :----: | :------------: | :--: | :--: |:--:|:--:| :---: | :----: | :------: |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | Y     |  -   | 70.6 | 65.4 | 3652 | 175955 | 1441 | [config](tracktor_faster-rcnn_r50_fpn_8e_mot20-public-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20-half_20210805_001244-2c323fd1.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20-half_20210805_001244.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426-c83b1c01.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426.log.json) |
| R50-FasterRCNN-FPN | R50 | half-train | half-val | N     |  -   | 70.9 | 64.1 | 5539 | 171653 | 1619 | [config](tracktor_faster-rcnn_r50_fpn_8e_mot20-private-half.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20-half_20210805_001244-2c323fd1.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20-half_20210805_001244.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426-c83b1c01.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426.log.json) |
| R50-FasterRCNN-FPN | R50 | train      | test     | Y     |  -   | 57.9 | 54.8 | 16203 | 199485 | 2299 |  [config](tracktor_faster-rcnn_r50_fpn_8e_mot20-public.py) | [detector](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20_20210804_162232-7fde5e8d.pth) &#124; [detector_log](https://download.openmmlab.com/mmtracking/mot/faster_rcnn/faster-rcnn_r50_fpn_8e_mot20_20210804_162232.log.json) &#124; [reid](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426-c83b1c01.pth) &#124; [reid_log](https://download.openmmlab.com/mmtracking/mot/reid/reid_r50_6e_mot20_20210803_212426.log.json) |
| R50-FasterRCNN-FPN* | R50 | train     | test     | Y     | -    | 52.6 | 52.7 | 6930 | 236680 | 1648 | -    | -     |

Note: When running `demo_mot.py`, we suggest you use the config containing `private`, since `private` means the MOT method doesn't need external detections.
