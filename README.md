# YOLOv8
#🦷 YOLOv8 Dental Detection

A deep learning project to fine-tune YOLOv8 for detecting and classifying different types of teeth from dental images. This model was trained on a custom dataset with 7 tooth classes to achieve high accuracy and robust performance.

#📑 Project Overview

This project demonstrates how to:

Prepare a custom dental dataset for YOLOv8

Fine-tune YOLOv8 on 7 tooth categories

Evaluate model performance using metrics such as Precision, Recall, and mAP

Test and visualize results on new images

#🗂 Dataset

The model was trained on a curated set of dental images (not X-rays) with 7 annotated classes:

1st Molar

1st Premolar

2nd Molar

2nd Premolar

Canine

Central Incisor

Lateral Incisor

Dataset organized in YOLO format:

dental_dataset/
  images/
    train/
    val/
  labels/
    train/
    val/

#🛠️ Installation

Clone the repository and install the required dependencies:

git clone https://github.com/<your-username>/YOLOv8-Dental-Detection.git
cd YOLOv8-Dental-Detection
pip install ultralytics

#🚀 Training

Train the YOLOv8 model on the dental dataset:

yolo detect train data=dental.yaml model=yolov8n.pt epochs=20 imgsz=640

🧪 Testing / Inference

Run inference on test images:

yolo detect predict model=runs/detect/train/weights/best.pt source=test_images/

📊 Results

Final model metrics on validation data:

Precision: 94.4%

Recall: 95.9%

mAP@0.5: 97.8%

mAP@0.5:0.95: 77.5%

Example output:
(insert a sample prediction image here)

💡 Applications

Automated dental analysis from clinical photographs

AI-assisted diagnosis for dentists

Foundation for segmentation and X-ray/3D scan analysis


🙌 Acknowledgements

Ultralytics YOLOv8

Open-source dental datasets and annotation tools
