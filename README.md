# Acupuncture Needle Segmentation and Detection

This repository contains the workflow for collecting, segmenting, and detecting acupuncture needles in various scenarios using experienced acupuncturists' operation videos.

## Table of Contents

1. [Data Collection](#data-collection)
2. [Needle Segmentation Dataset Creation](#needle-segmentation-dataset-creation)
3. [Model Training and Evaluation](#model-training-and-evaluation)

## 1、Data Collection

Collect acupuncture operation videos from acupuncturists with over 15 years of experience in different scenarios, such as:
- Hospital wards
- Clinics
- Various lighting conditions

## 2、Needle Segmentation Dataset Creation

Create a needle segmentation dataset using two methods:

### (1) Manual Segmentation
- Utilize segmentation tools to annotate each frame of the video.
- Generate masks for the needles.

### (2) Automated Segmentation
- Use Meta AI's SAM (Segment Anything Model) through an interactive segmentation method.
- Based on point prompts, select the region around the point prompt as the segmentation result for the target object.

### Conversion to COCO Format
- Convert the annotated data into the COCO dataset format required for neural networks.

## 3、Model Training and Evaluation
- Train the model within the MASK-RCNN network embedded with FPN.
- Successfully detect acupuncture needles in various scenarios.
