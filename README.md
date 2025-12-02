# Setup

## Environment
This project uses `uv` for dependency management.
Install it here: [uv Webpage](https://docs.astral.sh/uv/#highlights)

```sh
# create virtual env
uv venv
# install dependencies
uv sync --all-extras
```

## Data
We use the [CIC-BCCC-NRC TabularIoTAttack-2024](https://www.unb.ca/cic/datasets/tabular-iot-attack-2024.html) dataset which can be downloaded on [kaggle](https://www.kaggle.com/datasets/kabeleswarpe/cic-bccc-nrc-tabulariotattacks-2024/data)

We processed this raw data into `.parquet` files. You can download the processed `.parquet` at the following Google Drive links:
- Combined raw data: [combined_traffic.parquet](https://drive.google.com/file/d/1BC3SjcUOdyF4weHMF57boUNdu9nUpr5y/view?usp=sharing)
    - Merged raw CSV's from original data source
    - See `data_processing.ipynb`
- Sampled traffic data: [sampled_traffic.parquet](https://drive.google.com/file/d/1pdntCV0undI_VpPMgg8gyHMVhAOlCtz0/view?usp=sharing)
    - Sample at most 3000 records from each attack type
    - See `data_processing.ipynb`
- Feature processed data: [processed_traffic.parquet](https://drive.google.com/file/d/15Rx_iknckhNhUrL-fOOBwGSJW1RRaoRv/view?usp=sharing)
    - Drop redundant/unneeded columns
    - See `feature_processing.ipynb`
    - **NOTE:** If you only want to run the model notebooks, this is the only file you need to download.

After downloading, please move the files into the `data/` directory

# Data Exploration & Visualization
See `feature_processing.ipynb`.

# Model Comparison
Each model was explored with its own python notebook:
- KNN: `knn.ipynb`
- Random Forest: `rf.ipynb`
- MLP: `mlp.ipynb`
- XGBoost: `xgboost.ipynb`
- Mitra: `mitra.ipynb`
