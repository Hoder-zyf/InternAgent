# AutoTSF

Long-term multivariate time series forecasting task based on DLinear with series decomposition, evaluated on the ETTh1 benchmark dataset.

---

## Dataset

This task uses the **ETTh1 (Electricity Transformer Temperature, hourly)** dataset, a standard benchmark for long-term time series forecasting.

### Download

If it is not already present, download it from the official ETT repository:
```
https://github.com/zhouhaoyi/ETDataset
```

### Configure Data Paths

Open `launcher.sh` and update the `--root_path` argument to point to the directory containing `ETTh1.csv`:

```bash
python -u experiment.py \
  --root_path /path/to/your/datasets/ \
  --data_path ETTh1.csv \
  ...
```

---

### Install additional dependencies

```bash
pip install pandas scikit-learn 
```
