# Vehicle Detection and Counting System

This project detects vehicles traveling on a road and counts the number of vehicles entering and exiting a designated pathway using the YOLOv8 object detection model and image processing techniques.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Results](#results)
- [License](#license)

## Overview

The Vehicle Detection and Counting System leverages the YOLOv8 object detection model to detect vehicles in a video stream and count the number of vehicles entering and exiting a specified road or pathway. The system is designed for real-time traffic monitoring and analysis.

### Applications:
- Traffic flow monitoring
- Road infrastructure planning
- Intelligent Transportation Systems (ITS)

## Features

- Real-time vehicle detection using the YOLOv8 model.
- Vehicle counting for both entry and exit from the monitored area.
- Support for video input and live camera feeds.
- Customizable detection zones for counting vehicles in specific pathways.
- Vehicle logs saved for future analysis.

## Requirements

Before running the project, ensure the following dependencies are installed:

- Python 3.x
- PyTorch (for YOLOv8)
- OpenCV
- NumPy
- Matplotlib (optional for visualizations)
- Ultralytics
- Other dependencies can be installed from the `requirements.txt` file.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/vehicle-detection-counting.git
    cd vehicle-detection-counting
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained YOLOv8 model weights:
    - Download the YOLOv8 weights provided in the repository.
    - Place the weights file (e.g., `yolov8n.pt`) in the `models/` directory.

4. Add your input video to the `data/` folder or set up a live camera feed.

## Usage

To run the vehicle detection and counting system, use the following commands:

1. For video input:
    ```bash
    python main.py --input data/your_video.mp4 --model models/yolov8n.pt
    ```

2. For live camera feed:
    ```bash
    python main.py --input webcam --model models/yolov8n.pt
    ```

3. Configure the detection zone by adjusting the `zone_coordinates` in the `config.json` file.

## Model Training

If you need to train the YOLOv8 model on custom data:

1. Prepare the dataset:
    - Annotate vehicle images using bounding boxes (use [LabelImg](https://github.com/tzutalin/labelImg) for annotation).
    - Ensure the dataset follows the COCO format or other formats supported by YOLOv8.

2. Train the model:
    - Follow the official YOLOv8 training guide from the [Ultralytics YOLOv8 repository](https://github.com/ultralytics/ultralytics#train-custom-models).

## Results

After running the model, you will get:

- A video with detected vehicles highlighted by bounding boxes.
- Real-time vehicle count displayed for both entry and exit.
