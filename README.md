# autogluon-kaggle

## Kaggle Setup (for IEEE‑CIS Fraud & California Housing)

These notebooks pull data via the Kaggle API.

Create/Locate your kaggle.json from https://www.kaggle.com/settings/account (API section).

In Colab, run:
```
# Upload kaggle.json (use the Colab file uploader if prompted)
from google.colab import files
files.upload()  # select kaggle.json
```
```
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!pip -q install -U kaggle
```

Download datasets inside the notebook (paths are set in code):

IEEE‑CIS Fraud Detection
```
!kaggle competitions download -c ieee-fraud-detection -p data/ieee
!unzip -o data/ieee/ieee-fraud-detection.zip -d data/ieee
```
California Housing Price (Kaggle version) or use the AutoGluon example loader.

All paths used in notebooks default to data/ inside the repo; adjust if needed.

## Video Walkthrough
- Videos for part B are located in videos folder
