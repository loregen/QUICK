# QUICK (QUantized In-memory Classifier for Keyword-spotting)

The goal of the project is to train and implement a convolutional neural network for keyword spotting on a custom integrated circuit, that features an embedded phase-change memory block for matrix-vector multiplication acceleration.

## Notebooks

The repository contains two Jupyter notebooks:

- `QUICK_training.ipynb`: This notebook is used for training the keyword spotting model. It includes all necessary steps from data preprocessing to model training and evaluation.
- `QUICK_inference.ipynb`: This notebook allows you to try out the trained models using your microphone for real-time inference.

## Installation

To run the notebooks, you need Python 3.8. For training, the following packages are needed:

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

If you use conda to manage your Python environment, you can create a new environment with the required packages using the following command (only on Apple Silicon):

```bash
conda env create -f QUICK_env.yml
```


## Dataset

The full audio dataset has 35 classes and can be downloaded from the TensorFlow datasets catalog at [Speech Commands Dataset](https://www.tensorflow.org/datasets/catalog/speech_commands). However, this repository includes only 5 classes (left, no, right, stop, yes) in the 'current_classes' folder, and the current model is sized for this subset. If you want to try with more classes, you can just add the audio files to the 'current_classes' folder and configure the model accordingly.
