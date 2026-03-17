# AutoEAP

Enhancer Activity Prediction task based on **DeepSTARR**, evaluated on the **UMI STARR-seq dataset** for quantitative enhancer activity prediction from DNA sequences.

---

## Download

All required resources, including:

* Dataset
* Conda environment configuration

are available in the following Google Drive folder:

```
https://drive.google.com/drive/folders/1tVkGQMp7axhd7myPZSMr8xAo4tYP_leX?usp=drive_link
```

Download the contents and place them in a directory accessible to the project.

---

## Run the Experiment

### Script

```bash
python experiment.py --out_dir $1 --indir /path/to/Sequences_activity_all.txt > $1/train.log 2>&1
```

The --indir argument should point to the downloaded dataset file Sequences_activity_all.txt.

### Example

```bash
bash launcher.sh run1
```

This command will:

* run the training/evaluation pipeline
* store results in `run1`
* redirect logs to:

```
run1/train.log
```

---

## Environment Setup

A compressed conda environment is included in the Google Drive folder:

conda_env/deepstarr.tar.gz

