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