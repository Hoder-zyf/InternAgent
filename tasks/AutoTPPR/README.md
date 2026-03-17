# AutoTPPR

Transcription Prediction for Perturbation Response task based on **GEARS**, evaluated on the **Perturb-seq dataset** for predicting transcriptional responses of cells under genetic perturbations.

---

## Download

All required resources, including:

* Dataset
* Conda environment configuration

are available in the following Google Drive folder:

```
https://drive.google.com/drive/folders/1TIWtDrofioGOVio6_WoxJxuWdpJwm6n6
```

Download the contents and place them in a directory accessible to the project.

---

## Run the Experiment

### Script

```bash
python experiment.py \
    --data_path /path/to/TPPR \
    --device cuda:1 \
    --epochs 20 \
    --out_dir $1 > $1/train.log 2>&1
```

The `--data_path` argument should point to the directory containing the downloaded **Perturb-seq dataset**.

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

```
conda_env/gears.tar.gz
```

Extract and activate the environment before running the experiment.

