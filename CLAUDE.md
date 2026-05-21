# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Dependencies

Install required packages:

```bash
pip install tensorflow numpy matplotlib opencv-python
```

## Running

Execute the main module directly:

```bash
python src/pokecard-nread/__init__.py
```

## Data Setup

Images must be organized under `src/pokecard-nread/data/` in class subdirectories (this directory is gitignored):

```
src/pokecard-nread/data/
  {class_name}/
    image1.jpg
    image2.png
    ...
```

To clean unsupported image formats before training, uncomment `clean_image_data_dir()` in `__main__` and run.

## Architecture

This is an early-stage TensorFlow/Keras image classification project targeting Pokemon card recognition. The sole source file is `src/pokecard-nread/__init__.py`.

- `load_data()` — loads the image dataset via `tf.keras.utils.image_dataset_from_directory`, iterates the first batch, and renders a 4-image preview with Matplotlib.
- `clean_image_data_dir()` — walks the data directory and removes files with unsupported extensions (`.jpeg`, `.jpg`, `.bmp`, `.png` are kept). OpenCV is used for the read check.
- `DEBUG` flag gates verbose logging in `clean_image_data_dir`.

There is no model definition, training loop, or evaluation yet — only data ingestion utilities.
