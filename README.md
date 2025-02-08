# Lab-DL2-

# YOLO-inspired Object Detection Implementation

## Project Overview
A simplified YOLO (You Only Look Once) implementation for object detection on COCO-2017 dataset, featuring:
- Custom anchor box calculation using IoU-based k-means
- ResNet50 backbone with transfer learning
- Custom loss function and training metrics
- Data augmentation pipeline
- Graceful training interruption handling

## Key Features
1. **Anchor Box Optimization**: 
   - Uses IoU-based k-means clustering for data-specific anchor boxes
   - Automatically adapts to dataset characteristics
   - Calculates 5 anchors optimized for COCO objects

2. **Model Architecture**:
   - Backbone: Frozen ResNet50 (ImageNet weights)
   - Detection Head: Custom convolutional layers
   - Output: 13×13 grid with 5 boxes per cell

3. **Training Features**:
   - Automatic checkpointing
   - Early stopping
   - Learning rate reduction on plateau
   - TensorBoard integration
   - Keyboard interrupt safety

## Setup Instructions

### Requirements
```bash
Python 3.8+ 
pip install -r requirements.txt
