# pokesight-nread

A Python project for Pokemon card image recognition using TensorFlow/Keras and OpenCV. Currently in early development, focused on data ingestion and preprocessing utilities.

## Stack

- Python
- TensorFlow / Keras
- OpenCV (`cv2`)
- NumPy, Matplotlib

## Setup

```bash
pip install tensorflow numpy matplotlib opencv-python
```

## Data

Images must be organized by class under `src/pokecard-nread/data/` (gitignored):

```
src/pokecard-nread/data/
  {class_name}/
    image1.jpg
    image2.png
```

## Usage

```bash
python src/pokecard-nread/__init__.py
```

This loads the dataset and renders a preview of the first 4 images with their class labels.

To remove unsupported image formats from the data directory, uncomment `clean_image_data_dir()` in `__main__`.
