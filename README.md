# M-Vet Platform

## Overview

The M-Vet Platform is designed to facilitate the processing and analysis of ELISA plate data. This repository contains the necessary documentation, a sample dataset, and tasks aimed at automating ELISA well identification and image reading predictions using computer vision techniques.

## Contents

- [Documentation](#documentation)
- [Sample Dataset](#sample-dataset)
- [Task 1: ELISA Well Identification](#task-1---elisa-well-identification)
- [Task 2: Computer Vision for ELISA Plate Image Reading Prediction](#task-2---computer-vision-for-elisa-plate-image-reading-prediction)

## Documentation

The documentation provides detailed instructions on how to use the platform, the structure of the sample dataset, and the methodologies employed for the tasks.

- **[User Guide](docs/User_Guide.md)**: Instructions on how to set up and use the platform.
- **[Developer Guide](docs/Developer_Guide.md)**: Detailed information on the codebase, including setup instructions and development guidelines.
- **[Methodology](docs/Methodology.md)**: Description of the methods used for ELISA well identification and computer vision prediction tasks.

## Sample Dataset

The sample dataset is provided to help you understand the structure and format of the data used in the platform. It includes:

- **Raw ELISA Plate Images**: Images of ELISA plates that need to be processed.
- **Annotated Data**: Data files that include annotations for well identification and image reading.

You can find the sample dataset in the `data/sample_dataset` directory.

## Task 1 - ELISA Well Identification

The goal of this task is to accurately identify the wells on an ELISA plate. The following steps outline the methodology and provide a sample code implementation using OpenCV and image processing techniques.

### Methodology

1. **Preprocessing**:

   - Load the ELISA plate image and convert it to grayscale.
   - Apply Gaussian blur to the grayscale image to reduce noise and improve the accuracy of circle detection.

2. **Circle Detection**:

   - Use the Hough Circle Transform to detect the circular wells on the ELISA plate.
   - Draw the detected circles on the image for visualization.

3. **Tiling the Image**:

   - Divide the image into smaller tiles, each representing a well on the ELISA plate.
   - Assign labels to each tile corresponding to the well location (e.g., A1, B2, etc.).

4. **Center Detection**:
   - For each tile, detect the center of the well using the Hough Circle Transform.
   - Extract the RGB values from the center of each well for further analysis.

### Code

The code implementation for this task can be found in the following files:

- **Notebook**: `notebooks/elisa_well_identification.ipynb`

### Dependencies

Ensure you have the following libraries installed:

- OpenCV
- NumPy
- Pandas
- Matplotlib
- Tiler
- PIL

## Task 2 - Computer Vision for ELISA Plate Image Reading Prediction

The goal of this task is to utilize computer vision techniques to read and analyze ELISA plate images for predictions. This involves training a YOLO model to detect the wells and extract relevant data.

### Methodology

1. **Environment Setup**:

   - Install necessary libraries including `ultralytics` for YOLO model training and `roboflow` for dataset management.
   - Set up directories for datasets and results.

2. **Dataset Preparation**:

   - Download the dataset from Roboflow and prepare it for training with YOLO.

3. **Model Training**:

   - Train a YOLO model using the prepared dataset. The model is trained to detect wells in ELISA plate images.

4. **Model Validation and Prediction**:

   - Validate the trained model and make predictions on test images.
   - Visualize the model's performance with confusion matrices and result images.

5. **Inference and Analysis**:
   - Deploy the trained model to perform inference on new images.
   - Extract RGB values from detected wells and perform non-maximum suppression to refine detections.

### Code

The code implementation for this task can be found in the following files:

- **Notebook**: `notebooks/elisa_plate_detection.ipynb`

### Dependencies

Ensure you have the following libraries installed:

- OpenCV
- NumPy
- Matplotlib
- Pandas
- Ultralytics (YOLO)
- Roboflow
