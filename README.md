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
The goal of this task is to accurately identify the wells on an ELISA plate. The steps involved include:
1. **Preprocessing**: Preparing the images for analysis by resizing, normalization, and other techniques.
2. **Well Detection**: Using image processing techniques to locate and identify individual wells on the ELISA plate.
3. **Validation**: Ensuring the accuracy of well identification through cross-validation with annotated data.

### Implementation
- **Script**: `scripts/well_identification.py`
- **Dependencies**: List of required libraries can be found in `requirements.txt`.

## Task 2 - Computer Vision for ELISA Plate Image Reading Prediction
