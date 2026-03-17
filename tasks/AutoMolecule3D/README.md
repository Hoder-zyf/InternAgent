# AutoMD

Molecular Dynamics task based on **VisNet**, evaluated on the **MD17 dataset** for predicting molecular energies and forces from atomic configurations.

---

## Download

All required resources, including:

* Dataset
* Conda environment configuration

are available in the following Google Drive folder:

```
https://drive.google.com/drive/folders/1kMGkKY_EL9JDgL0gHR-p_vpvwa3fwx2S?usp=sharing
```

Download the contents and place them in a directory accessible to the project.

---

## Run the Experiment

### Script

```bash
CUDA_VISIBLE_DEVICES=0 python experiment.py \
  --conf examples/ViSNet-MD17.yml \
  --dataset-arg aspirin \
  --dataset-root /path/to/md17_dataset \
  --out_dir $1 > $1/train.log 2>&1
```

The `--dataset-root` argument should point to the directory containing the downloaded **MD17 dataset**.

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
conda_env/visnet.tar.gz
```

Extract and activate the environment before running the experiment.

