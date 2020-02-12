# Directional-Deep-Embedding-and-Appearance-Learning-for-Fast-Video-Object-Segmentation

## Dependencies:
```bash
python (>= 3.5 or 3.6)
numpy
pytorch (>= 0.5 probably)
torchvision
pillow
tqdm
```

## Datasets utilized:
DAVIS

YouTubeVOS

## How to setup:
1. Install dependencies
2. Clone this repo:
```bash
git clone https://github.com/YingjieYin/Directional-Deep-Embedding-and-Appearance-Learning-for-Fast-Video-Object-Segmentation.git
```
3. Download datasets
4. Set up local_config.py to point to appropriate directories for saving and reading data
5. Move the ytvos_trainval_split/ImageSets directory into your YouTubeVOS data directory. The directory structure should look like
```bash
/...some_path.../youtube_vos
-- train
---- Annotations
---- JPEGImages
-- valid
---- Annotations
---- JPEGImages
-- ImageSets
---- train.txt
---- train_joakim.txt
---- val_joakim.txt
```

## How to run method on DAVIS and YouTubeVOS with pre-trained weights:
1. Download weights from 
链接：https://pan.baidu.com/s/1fcsHWNmE1e5xL5k9AJjmnw 
提取码：y5xx 
（This UNITED TRAINED MODEL CAN ACHIEVE THE RESULTS ON ALL TESTING DATSETS OF DAVIS2016, DAVIS2017,YOUTUBE-VOSIN IN OUR PAPER!!）

2. Put the weights at the path pointed out by config['workspace_path'] in local_config.py.
3. Run
```bash
python3 -u runfiles/main_runfile.py --test
```

## How to train (and test) a new model:
1. Run
```bash
python3 -u runfiles/main_runfile.py --train --test
```

Most settings used for training and evaluation are set in your runfiles. Each runfile should correspond to a single experiment. I supplied an example runfile.
## Experimental results on DAVIS2016, DAVIS2017,Youtube-VOS 
   DAVIS16_val.rar  链接：https://pan.baidu.com/s/1JetbLKoZSmT0IzHrqVPNjA 提取码：ca63
   
   DAVIS17_val.rar  链接：https://pan.baidu.com/s/1G7zIwzOF3-Z25R6w4riWfA 提取码：y7d4 
   
   YTVOS_val.rar    链接：https://pan.baidu.com/s/10tHuZxnis5R7mZmhOIZH0w 提取码：tdsl
## Compared results:
   Demo1_DAVIS2016.avi  链接：https://pan.baidu.com/s/19cMdbxU2ggOyGzZl0MwMWA 提取码：jdxq
   
   Demo2_DAVIS2017.avi  链接：https://pan.baidu.com/s/1raT-G2Jc-hJljyubPodpXA 提取码：0oqv 
   
   Demo3_YouTube-VOS.avi 链接：https://pan.baidu.com/s/1ymDMrblZ8P_d0byOwnJW8Q 提取码：qtkc
   
![image](https://github.com/YingjieYin/Directional-Deep-Embedding-and-Appearance-Learning-for-Fast-Video-Object-Segmentation/blob/master/results.png)
