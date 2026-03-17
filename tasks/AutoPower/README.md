# AutoPower

Power flow estimation task based on SenseFlow with heterogeneous graph neural networks, evaluated on the IEEE 39-Bus power system.

---

## Dataset

This task uses the **IEEE 39-Bus (New England) Power System** dataset, consisting of power flow simulation samples with random operating points.
Your can download data from this link: https://drive.google.com/file/d/1bEYBC6SMBL0VQzcGz6sPNYl0kJtf4d7Q/view?usp=drive_link
### Download

The dataset files are expected at:

```
case39_data/
  -10w_case39_n_n_1.json 
  -2w_case39_n_2.json  
  -caseN
  -caseN_1  
  -caseN_2
```

If they are not already present, contact the data owner or generate the dataset using a power flow simulator (e.g., MATPOWER or pandapower) with the IEEE 39-bus test case.


### Configure Data Paths

`launcher.sh` passes the config file to the experiment via `--config configs/test_senseflow_39.yaml`. Open that config file and update the `split_txt` fields under `data` to point to the actual file locations:

```yaml
data:
  train:
    split_txt: /path/to/your/datasets/case39_data/10w_case39_n_n_1.json
  val:
    split_txt: /path/to/your/datasets/case39_data/2w_case39_n_2.json
```

---

### Install additional dependencies

```bash
pip install torch_geometric tensorboard loguru
```
