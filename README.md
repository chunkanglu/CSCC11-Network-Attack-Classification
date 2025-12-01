# Setup

## Environment
This project uses `uv` for dependency management and other things like formatting.
Install it here: [uv Webpage](https://docs.astral.sh/uv/#highlights)

```sh
# create virtual env
uv venv
# install dependencies
uv sync
```

## Data
We use the [CIC-BCCC-NRC TabularIoTAttack-2024](https://www.unb.ca/cic/datasets/tabular-iot-attack-2024.html) dataset which can be downloaded on [kaggle](https://www.kaggle.com/datasets/kabeleswarpe/cic-bccc-nrc-tabulariotattacks-2024/data)

We processed this raw data into `.parquet` files. You can download the processed `.parquet` at the following Google Drive links:
- Combined raw data: [combined_traffic.parquet](https://drive.google.com/file/d/1BC3SjcUOdyF4weHMF57boUNdu9nUpr5y/view?usp=sharing)
- Sampled traffic data: [sampled_traffic.parquet](https://drive.google.com/file/d/1pdntCV0undI_VpPMgg8gyHMVhAOlCtz0/view?usp=sharing)
- Feature processed data: [processed_traffic.parquet](https://drive.google.com/file/d/15Rx_iknckhNhUrL-fOOBwGSJW1RRaoRv/view?usp=sharing)

After downloading, please move the files into the `data/` directory