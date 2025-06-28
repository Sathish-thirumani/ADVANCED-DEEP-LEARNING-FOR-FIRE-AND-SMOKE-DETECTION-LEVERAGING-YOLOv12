# Fire and Smoke Detection Using YOLOv12

This repository contains code for detecting fire and smoke in images and videos using the YOLOv12 model. The dataset is stored in Google Drive, and the trained model alerts the user by sending an SMS when fire or smoke is detected.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Dataset](#dataset)
- [Training the Model](#training-the-model)
- [Testing the Model](#testing-the-model)
- [Detection on Video](#detection-on-video)
- [Sending Alerts](#sending-alerts)
- [Results](#results)
- [Contributing](#contributing)

## Introduction
This project leverages YOLOv12, an advanced object detection architecture, to identify fire and smoke in images and videos. The code is structured to train the model using a dataset from Google Drive and to trigger SMS alerts when detection occurs.

## Installation
To set up the project and its dependencies:

1. Mount Google Drive.
2. Clear any cached files or sessions.
3. Verify GPU availability and configuration.
4. Install required libraries, including dependencies specific to YOLOv12.

Make sure your environment is compatible with the latest YOLOv12 requirements.

## Dataset
The dataset must be stored in Google Drive. It should include labeled images along with a properly structured data.yaml file. This file should define paths to:

- Training images
- Validation images
- Testing images
- Class names

Ensure annotations are in YOLO format and compatible with YOLOv12 input standards.

## Training the Model
Use the training scripts to initiate model learning. Recommended parameters for YOLOv12 include:

- Epochs: Set according to dataset size.
- Batch Size: Tune based on memory capacity.
- Image Size: Supported resolutions should match YOLOv12 input.
- Learning Rate: Adjust for faster convergence.
- Optimizer: Momentum-based optimizers like SGD or Adam are supported.

Enable mixed precision or auto-learning rate features for improved performance where possible.

## Testing the Model
After training, evaluate the model using:

- Test Set Evaluation: Assess detection accuracy.
- Metrics Tracked: Precision, Recall, F1-Score, mAP, Inference Speed.

Make use of YOLOv12’s enhanced evaluation scripts for accurate benchmarking.

## Detection on Video
Use the video inference module to process and annotate videos:

- Input the path to a video file.
- Split video into frames.
- Run inference using the trained YOLOv12 model.
- Save annotated output.

Supports real-time detection with GPU acceleration.

## Sending Alerts
Integrate Twilio to send real-time alerts:

- Account SID and Auth Token from Twilio dashboard.
- From and To Numbers should be verified and formatted correctly.
- Trigger alert when detection confidence surpasses threshold.

## Results
Visualize performance over training epochs:

- Precision/Recall Curves
- Loss Metrics (box loss, objectness loss, class loss)
- Confusion Matrix
- Use YOLOv12's built-in results.json and plot utility.

## Contributing
We welcome community contributions!

### Contribution Guide
1. Fork this repository.
2. Create a dedicated feature/bugfix branch.
3. Make your changes with clear commit messages.
4. Push and open a pull request describing your changes.
