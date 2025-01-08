# Markerless Gait Analysis System

## Overview

This repository presents a cutting-edge markerless gait analysis system that leverages advanced computer vision and deep learning techniques to achieve robust, accurate, and user-friendly gait analysis. By transforming 2D images from standard smartphone cameras into precise 3D reconstructions, the system provides invaluable insights into human gait patterns, aiding applications in sports science, medical diagnostics, biomechanics, and rehabilitation.

## Key Features

- **Markerless Technology**: Eliminates the need for intrusive markers, enhancing patient comfort and usability.
- **High Accuracy**: Achieves 98.89% accuracy in key joint angle detection, surpassing traditional systems like YOLO.
- **Advanced Pose Estimation**: Utilizes models such as ViTPose-H and YOLOv8 trained on COCO-Pose and COCO 25 datasets for superior keypoint detection.
- **Comprehensive Gait Cycle Analysis**: Breaks down the gait cycle into eight distinct phases, including initial contact, loading response, and terminal swing.
- **Depth Estimation**: Incorporates Monodepth2 for precise 3D reconstructions.
- **Hardware Friendly**: Operates with just a smartphone camera, making it cost-effective and accessible.

## Methodology

1. **Video Input Framing**:
   - Input video requirements:
     - Resolution: ≥800x600 pixels
     - Frame rate: ≥25 FPS
     - Single-person, full-body footage
   - Framed using the OpenCV library.

2. **Person Detection and Cropping**:
   - Performed using YOLOv8 trained on COCO-Pose dataset.

3. **Depth Estimation**:
   - Implemented with Monodepth2 for 3D reconstruction.

4. **Pose Estimation**:
   - Keypoints and angles calculated using ViTPose-H and YOLOv8.

5. **Gait Cycle and Phase Calculation**:
   - Comprehensive gait cycle analysis using temporal and spatial data.
   - Eight phases identified: Initial Contact, Loading Response, Mid-Stance, Terminal Stance, Pre-Swing, Initial Swing, Mid-Swing, and Terminal Swing.

## System Requirements

### Hardware:
- NVIDIA GPU (e.g., RTX 3060)
- 16 GB RAM
- 1 TB SSD

### Software:
- **Languages**: Python 3.10.12
- **Libraries**:
  - OpenCV
  - NumPy
  - Torch
  - MXNet
  - GluonCV
  - Matplotlib
  - Seaborn
  - Ultralytics
  - Singularity
  -  OpenPose
  -  VitPose
  -  Yolov11
- **Development Tools**:
  - Google Colab
  - Kinovea
  - Hugging Face Hub

### Dataset:
- **Primary Dataset**: Recorded video dataset under controlled conditions.
- **Training Data**: COCO-Pose and COCO 25 datasets.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/markerless-gait-analysis.git
2. Install the required libraries:
pip install -r requirements.txt

3. Usage
Record video footage as per system requirements.
Preprocess the video using the provided scripts.
Run the main pipeline to extract gait analysis insights:
```
python main.py --input /path/to/video
```

## Results
Outperforms traditional models like YOLO under challenging conditions, such as varying lighting or obstructive clothing.
- Enables accurate analysis of kinematic parameters (ankle, knee, and hip movements) for rehabilitation and prosthetics optimization.

## Limitations
- 3D frame motion remains a challenging factor in accuracy.
- Further refinements needed for handling occlusions in more complex environments.

## Future Work
- Enhance motion handling in 3D frames.
- Expand usability across diverse environments and patient conditions.


## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss potential improvements.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

Let me know if you’d like any further adjustments!
