# YOLOv8 Object Detection for Hajj Dataset

This repository contains a project for object detection in the Hajj dataset using the YOLOv8 model.  The project is designed to be run in Google Colab.

## Project Overview

The project performs the following steps:

1. **Data Preparation:** Downloads the Hajj dataset, processes the video data into individual frames with corresponding YOLO format annotations. Divides the dataset into training and validation sets.  Creates a `data.yaml` file for YOLOv8 training.
2. **Model Training:** Trains a YOLOv8 model on the prepared dataset.
3. **Model Evaluation and Inference:** Saves the trained model to Google Drive. Runs inference on test video, converting the output to an MP4 for visualization.

## Requirements

* Python 3.7+
* Google Colab environment
* Libraries:  `google.colab`, `cv2`, `matplotlib`, `pandas`, `os`, `IPython`, `ultralytics`, `yaml`, `shutil`, `moviepy`

(All libraries are installed within the Colab notebook itself)


## Usage

1. Open the provided Colab notebook in your Google Colab environment.
2. Execute all cells in order.


## Data

The project uses the Hajj Dataset v2.  The dataset should be downloaded automatically by the notebook.

## Training

The YOLOv8 model is trained for 25 epochs with an image size of 224x224.  Plots are generated during training. The results, including trained weights, are saved in the `/content/runs` directory and then moved to your Google Drive.

## Inference

Inference is performed on a test video using the trained `best.pt` model.  The results are output as an AVI file, which is then converted to an MP4 video for playback in the Colab notebook.

## Google Drive Integration

The project saves model results to your Google Drive. You will need to authorize Google Drive access when prompted in the notebook.


## Acknowledgments

* The Hajj dataset provided by KAU-Smart-Crowd.
* The Ultralytics YOLOv8 library.
