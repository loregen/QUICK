# QUICK

The goal of the project is to train and implement a convolutional neural network for keyword spotting on a custom integrated circuit, that features an embedded phase-change memory block for matrix-vector multiplication acceleration.

## Notebooks

The repository contains two Jupyter notebooks:

- `QUICK_training.ipynb`: This notebook is used for training the keyword spotting model. It includes all necessary steps from data preprocessing to model training and evaluation.
- `QUICK_inference.ipynb`: This notebook allows you to try out the trained models using your microphone for real-time inference.

## Installation

To run the notebooks, you need to install the required packages. For training, the following packages are needed:

- `tensorflow 2.13`
- `larq 0.13.3`
- `numpy 1.23.5`
- `librosa 0.10.0`
- `matplotlib 3.7.1`
- `scikit-learn 1.2.2`

For real-time inference, you need to install the following additional packages:

- `pyaudio 0.2.14`
- `IPython 8.12.0`
- `ipywidgets 8.1.2`

You can install the required packages using the following command:

```bash
pip install -r requirements.txt
```

## Dataset

## Dataset

The full audio dataset has 35 classes and can be downloaded from the TensorFlow datasets catalog at [Speech Commands Dataset](https://www.tensorflow.org/datasets/catalog/speech_commands). However, this repository includes only 5 classes to match the current model in the notebook which is sized for 5 classes.

## Git LFS

The `.wav` files in this repository are tracked using Git Large File Storage (LFS). To pull the LFS files after cloning the repository, you need to have Git LFS installed. If you haven't installed it yet, you can download it from [git-lfs.github.com](https://git-lfs.github.com/).

After installing Git LFS, you can pull the `.wav` files with the following command:

```bash
git lfs pull
```

Make sure you run this command inside the cloned repository directory to download the large files.
