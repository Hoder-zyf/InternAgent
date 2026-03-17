# AutoChem

Chemical yield prediction task based on LoRA-finetuned LLaMA3-8B, using Suzuki-Miyaura reaction dataset.

---

## Dataset

This task uses the **Suzuki-Miyaura reaction** dataset, download from:
   ```
   https://drive.google.com/file/d/1SGPdSICdyazTy9z_OF2phdXnzON9P9dk/view?usp=drive_link
   ```

## Pretrained Model

We use the **LoRA-finetuned LLaMA3-8B** as our baseline, download from:
   ```
   https://drive.google.com/file/d/1_qoRD278ybcKZ0pi0hick_KVRvVlmkk1/view?usp=drive_link
   ```
---

## Environment Setup

### 1. Create a conda environment

```bash
conda create -n autochem python=3.10 -y
conda activate autochem
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
               # /path/to/conda/envs/autochem/bin/python
```

Then edit the paths in `launcher.sh`:

```bash
/path/to/conda/envs/autochem/bin/deepspeed experiment.py \
  --pretrained_model_path '/path/to/step1_llama3_8b_0916_yearly_pistachio_ep3' \
   --num_epoch 301 \
   --data_path '/path/to/data4regression' \
   --data_name 'suzuki_miyaura_fg_changes_60' \
   --per_device_train_batch_size 2 \
   --save_root 'result_60' \
   --gradient_accumulation_steps 4 \
   --use_lora 1 \
   --log_file "training_ds.log" \
   --deepspeed_config 'ds_config.json' \
   --out_dir $1
```

