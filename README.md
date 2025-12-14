# ImageToSpectrogramPrediction

A small project to convert audio to spectrogram images and train models that predict spectrograms from images (or vice-versa). This repository contains preprocessing utilities, dataset folders, and an example script `AudioToSpectrogram.py`.

## Features

- Convert audio files to spectrogram images
- Organized dataset folders for source/target and train/test
- Starter script for conversion and experimentation

## Repository structure

- `AudioToSpectrogram.py` - Example script to generate spectrograms from audio (project entrypoint)
- `gearbox/`
  - `train/` - training audio files
  - `source_test/` - source test audio files
  - `target_test/` - target test audio files
- `SpectrogramImage/`
  - `train/` - generated spectrogram images for training

## Requirements

- Python 3.8+
- Typical packages used in audio & ML workflows (install as needed):

```bash
pip install numpy matplotlib librosa pillow tqdm
# plus your ML framework (tensorflow or torch) as required
```

If you prefer a pinned set of dependencies, create a `requirements.txt` and install with `pip install -r requirements.txt`.

## Quick start

1. Create a virtual environment and install dependencies:

```bash
python -m venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
pip install numpy matplotlib librosa pillow tqdm
```

2. Convert audio to spectrogram images (example):

```bash
python AudioToSpectrogram.py
```

Note: `AudioToSpectrogram.py` may accept arguments depending on your local edits. Open the file and follow the usage comments near its top.

## Dataset layout

- Place raw audio files to be converted inside `gearbox/train/` for training, and `gearbox/source_test/` / `gearbox/target_test/` for test examples.
- Generated spectrogram images should be saved under `SpectrogramImage/train/` (the project may include code that automatically writes here).

## Training & Evaluation

- Use the prepared spectrogram images as input/targets for your model.
- Training scripts are not included by default — adapt your own training loop using your preferred framework (TensorFlow / PyTorch).

## Tips

- Use `librosa` for audio loading and spectrogram generation.
- Normalize spectrograms before feeding them to a neural network.
- Keep train/test splits consistent between `gearbox/` and `SpectrogramImage/` folders.

## Contributing

Contributions welcome — please open issues or pull requests for improvements, bug fixes, or additional scripts (training, evaluation, or dataset utilities).

## License

This project is provided under the MIT License. See `LICENSE` (not included) or add one if you want to publish this repo.

## Contact

If you have questions or want help extending this project, open an issue or contact the repository owner.
