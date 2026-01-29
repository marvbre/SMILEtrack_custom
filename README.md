# SMILEtrack

> **[SMILEtrack: SiMIlarity LEarning for Multiple Object Tracking](https://arxiv.org/abs/2211.08824)**  
>Yu-Hsiang Wang, Jun-Wei Hsieh, Ping-Yang Chen, Ming-Ching Chang, Hung Hin So, Xin Li

Our paper was accepted by AAAI 2024

* The directory **"SMILEtrack_Official"** contains the latest version of SMILEtrack.  

This code is based on the implementation of [ByteTrack](https://github.com/ifzhang/ByteTrack), [BoT-SORT](https://github.com/NirAharon/BoT-SORT#bot-sort)

## update
2024/01: 
* Borrowed and reorganized the latest version of SMILEtrack from the [SMILE_track official](https://github.com/pingyang1117/SMILEtrack_Official/tree/main/tracker) and filled in the missing components.
* Added more detailed guidance in the README.
* Method to reproduce Benchmark Score (Currently in progress)


The key code to insert SMILEtrack into your detector prediction code is as follows:
```
from tracker.mc_SMILEtrack import SMILEtrack
tracker = SMILEtrack(args)
for image in images:
   dets = detector(image)
   online_targets = tracker.update(dets, info_imgs)
```
# 7.Tracking performance
## Results on MOT17 challenge test set
| Tracker | MOTA | IDF1 | HOTA |
|-------|:-----:|------:|------:|
| SMILEtrack |  81.06  |   80.5 |   65.28    |


## Results on MOT20 challenge test set
| Tracker | MOTA | IDF1 | HOTA |
|-------|:-----:|------:|------:|
| SMILEtrack |  78.19  |   77.53 |   65.28    |

# 8.Acknowledgement
A large part of the codes, ideas and results are borrowed from [PRBNet](https://github.com/pingyang1117/PRBNet_PyTorch), [ByteTrack](https://github.com/ifzhang/ByteTrack), [BoT-SORT](https://github.com/NirAharon/BoT-SORT#bot-sort), [yolov7](https://github.com/WongKinYiu/yolov7), thanks for their excellent work!

