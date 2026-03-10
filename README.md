# Drone vs Bird Detection

Binary image classifier that tells drones and birds apart from aerial photos. Built as a capstone project for MSDS 686 Deep Learning.

## What I did
Started with a naive baseline of 60.9% and worked up through logistic regression, custom CNNs, and finally MobileNetV2 transfer learning to hit 99.5% test accuracy, only 2 mistakes out of 404 test images, both traced back to watermarked photos in the dataset.

## Models tested
- Naive baseline : 60.9%
- Logistic Regression : 82.7%
- Simple CNN : 91.4%
- CNN + BatchNorm : 91.8%
- MobileNetV2 frozen : 98.3% ← best validation
- MobileNetV2 fine-tuned : 97.8%
- **Final test accuracy : 99.5%**

## Dataset
Drone vs Bird by Muhammad Saood Sarwar on Kaggle
https://www.kaggle.com/datasets/muhammadsaoodsarwar/drone-vs-bird

Download and place images under `data/raw/birds/` and `data/raw/drones/`

## Notebooks
- `01_EDA` : data exploration and quality issues
- `02_Baseline` : naive and logistic regression baselines  
- `03_Model_V1` : CNN experiments
- `04_Final` : transfer learning, final evaluation, error analysis
