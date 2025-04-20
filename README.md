# AI Assisted Real-Time Part Counting for Heat Treatment Furnace

![Project Poster](SKF.png)

## Project Team
- Mr. [Aditya Chavan - LinkedIn](https://www.linkedin.com/in/aditya-chavan-5117aa268/)
- Mr. [Bhavin Baldota - LinkedIn](https://www.linkedin.com/in/bhavin-baldota-103553234/)
- Ms. [Sharvari Korde - LinkedIn](https://www.linkedin.com/in/sharvari-korde-85b993268/)
- Mr. [Saumya Shah - LinkedIn](https://www.linkedin.com/in/saumya-shah-9b2579273/)


## Overview
This project implements a computer vision system for real-time counting of parts at inlet and outlet sections of multistage heat treatment furnaces. The system utilizes YOLOv8 object detection to achieve high accuracy in a challenging industrial environment.

## Problem Statement
Heat treatment of bearing components involves multistage operations where parts are taken at the inlet section and processed through various treatments. There is a critical need to monitor incoming and outgoing parts in the furnace. When parts coming out are fewer than those entering, it indicates that parts are stuck in various sections of the multistage process, which can lead to interior quality loss of material.

## Objectives
- Develop a computer vision system for real-time counting of parts at inlet and outlet sections of the multistage heat treatment furnace
- Use AI-YOLOv8 model to achieve 99.9% accuracy
- Deliver optimum performance in harsh industrial environments
- Utilize hardware resources with optimum consideration of cost and reliability

## Challenges
- Small part size (25-75 mm)
- Harsh working environment with dust, vibrations, and temperatures up to 70°C
- Variable conveyor speeds at inlet sections depending on part size
- Random and unpredictable part movement at outlet with overlapping parts that get stuck along the conveyor

## Methodology
The system follows a structured approach:
1. **Data Acquisition**: Capturing video feeds from inlet and outlet sections
2. **Data Preprocessing**: Frame extraction and resizing
3. **Data Annotation**: Labeling objects for training
4. **Detection**: Using YOLOv8 model
5. **Counting Objects**: Real-time counting with verification of annotated objects

## Results
- **Perfect Classification**: Achieved 100% accuracy for 'ring' and 'background' classes
- **No Misclassification**: Zero off-diagonal elements in the confusion matrix
- **Model Performance**: Excellent performance with 99.96% accuracy and no false positives/negatives
- **Balanced Dataset**: Well-handled class balance
- **Robust Solution**: Overlapping parts along the conveyor do not affect solution accuracy

## Implementation
The project consists of:
- Training scripts for the YOLOv8 model
- Prediction module for real-time object detection
- Frame extraction utility for video processing
- Testing and evaluation components

## Requirements
- Python 3.8+
- OpenCV
- Ultralytics YOLOv8
- CUDA-compatible GPU (recommended)

## Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/Object_Counting_For_Heat_Furnace.git

# Install dependencies
pip install -r requirements.txt
```

## Usage
### Training
```bash
# Navigate to the Training directory
cd Training

# Run the training notebook
jupyter notebook Training.ipynb
```

### Prediction
```bash
# For real-time prediction on video
python Predict.py
```

### Frame Extraction
```bash
# To extract frames from video for annotation
python frame.py
```



## License
This project is licensed under the terms of the included license file. 

