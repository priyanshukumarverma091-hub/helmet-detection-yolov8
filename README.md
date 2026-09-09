# Helmet Detection (YOLOv8)

Trains a YOLOv8 model on a Roboflow-hosted helmet detection dataset, and
includes a script to run inference via Roboflow's serverless API.

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env
# edit .env and add your Roboflow API key
```

## Train

```bash
python train.py
```

Downloads the dataset from Roboflow and trains a `yolov8n` model for 50 epochs.

## Inference (hosted model)

```bash
python infer.py path/to/image.jpg
```

## Notes

- Get your Roboflow API key from your [Roboflow account settings](https://app.roboflow.com/settings/api).
- **Never commit your `.env` file or API keys.** `.gitignore` is already set up to exclude it.
- If you've previously committed a key by mistake, rotate/regenerate it in Roboflow — removing it from a later commit doesn't remove it from git history.
