Title:Industrial Surface Defect Detection using Deep Learning

Slide 1 – Project Overview

Pixel-Level Industrial Surface Defect Detection Using U-Net

This project focuses on detecting and localizing surface defects in industrial steel images using deep learning–based semantic segmentation. A U-Net architecture is employed to perform pixel-level defect detection under real manufacturing conditions.

Slide 2 – Introduction

Industrial surface inspection is critical for maintaining quality and safety in steel manufacturing. Surface defects such as cracks, inclusions, and corrosion patches can severely affect product reliability. Manual inspection is slow and inconsistent. This project leverages deep learning to automate defect detection with high precision.

Slide 3 – Problem Statement

Steel surface defects are often thin, irregular, and low in contrast, making them difficult to detect. Traditional image processing methods fail under varying lighting and texture conditions. Accurate pixel-level localization is required for reliable industrial quality control.

Slide 4 – Objectives

Detect surface defects from industrial steel images

Perform pixel-level segmentation of defect regions

Use a U-Net deep learning model

Clearly visualize and analyze different defect types

Slide 5 – Dataset Description

Dataset: Severstal Steel Defect Detection Dataset (Kaggle)

High-resolution steel surface images

Real industrial manufacturing conditions

Pixel-level annotations using Run-Length Encoding (RLE)

Defect Types:

Cracks / Scratches (thin, elongated)

Inclusions (small, isolated)

Patches / Corrosion (large, irregular)

Slide 6 – Related Work / Paper Discussion

This project is inspired by Bergmann et al. (IJCV 2021) on industrial anomaly detection. The paper emphasizes pixel-level defect localization and motivates the use of deep learning segmentation models such as U-Net for industrial inspection tasks.

Slide 7 – Methodology

Workflow:

Input Image → Preprocessing → U-Net Segmentation → Defect Mask → Evaluation & Visualization

The dataset images are preprocessed and their RLE annotations are decoded to generate defect masks. A U-Net model is trained to predict pixel-wise defect regions.

Slide 8 – Network Architecture (U-Net)

U-Net is an encoder–decoder convolutional neural network with skip connections. The encoder extracts hierarchical features, while the decoder reconstructs high-resolution segmentation maps. Skip connections preserve spatial information, making U-Net effective for thin and small defects.

Slide 9 – System Working (Detailed Flow)

The input image passes through the encoder to extract features. The decoder upsamples these features back to the original resolution. Skip connections help recover fine boundaries. The final output is a pixel-level defect mask aligned with the original image.

Slide 10 – Results (Quantitative Metrics)

Model performance is evaluated using:

Intersection over Union (IoU)

Dice Coefficient

Dice scores are generally higher than IoU due to the sparse and small nature of defect regions. Metric distributions are analyzed using plots.

Slide 11 – Results (Qualitative Visualization)

Original steel images are visualized with color-coded defect regions:

Red – Cracks / Scratches

Blue – Inclusions

Yellow – Patches / Corrosion

This visualization improves interpretability and helps identify correct detections and failure cases.

Slide 12 – Observations

Most defects occupy small pixel areas

Thin cracks are more challenging to detect

Dice is more suitable than IoU for sparse defects

Visual inspection complements quantitative metrics

Slide 13 – Problems / Limitations

Severe class imbalance

Low-contrast defects

Difficulty capturing thin cracks at lower resolution

Sensitivity to threshold selection

Limited training data affects generalization

Slide 14 – Conclusion

The project demonstrates that deep learning–based U-Net segmentation can effectively detect industrial steel surface defects. Both quantitative metrics and qualitative results confirm the suitability of this approach for automated industrial inspection.
