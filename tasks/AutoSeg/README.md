# AutoSeg

Semantic segmentation task based on DeepLab with a ResNet backbone, evaluated on Pascal VOC 2012 with augmented training data.

---

## Dataset

This task uses the **Pascal VOC 2012** dataset with the **SBD (Semantic Boundaries Dataset)** augmented segmentation masks.

### Download

1. **Pascal VOC 2012** — download from the official site:
   ```
   http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar
   ```
   Extract to obtain the `VOCdevkit/` directory.

2. **Augmented segmentation masks (SegmentationClassAug)** — download from:
   ```
   https://www.dropbox.com/s/oeu149j8qtbs1x0/SegmentationClassAug.zip
   ```
   Or alternatively from the SBD dataset page:
   ```
   http://home.bharathh.info/pubs/codes/SBD/download.html
   ```

3. **train_aug.txt** — the augmented training split file. Download from:
   ```
   https://github.com/DrSleep/tensorflow-deeplab-resnet/blob/master/dataset/train_aug.txt
   ```

### Directory Structure

Place all data under `/datasets` (as expected by `launcher.sh`), following this structure:

```
/datasets/
└── VOCdevkit/
    └── VOC2012/
        ├── JPEGImages/
        ├── SegmentationClass/
        ├── SegmentationClassAug/       # augmented masks (from SBD)
        ├── ImageSets/
        │   └── Segmentation/
        │       └── val.txt
        └── train_aug.txt               # augmented training split
```

---

## Environment Setup

### 1. Create a conda environment

```bash
conda create -n autoseg python=3.10 -y
conda activate autoseg
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure the Python path in launcher.sh

Open `launcher.sh` and replace `python` with the full path to the conda environment's Python interpreter:

```bash
# Find the path
which python   # run after activating the conda env, e.g. outputs:
               # /path/to/conda/envs/autoseg/bin/python
```

Then edit the first line of `launcher.sh`:

```bash
/path/to/conda/envs/autoseg/bin/python experiment.py \
  --data_root /datasets \
  --batch_size 32 \
  --lr 0.02 \
  --out_dir $1
```

