Safety Detection — Japanese Construction Site
📊  Real-time PPE & hazard detection system using YOLOv7 + OpenCV achieving 87% mAP on a custom-annotated dataset

YOLOv7	OpenCV	87% mAP	Computer Vision

📝 Overview
A computer vision pipeline for real-time PPE (Personal Protective Equipment) and hazard detection at a Japanese construction site. Built during an ML internship at AlgoAnalytics, this system was trained on a custom-annotated dataset of 2,000+ images and deployed as a real-time monitoring pipeline to improve on-site safety coverage.

✨ Key Features
▸	Custom YOLOv7 model trained on 2,000+ manually annotated construction-site images
▸	Detects: hard hats, safety vests, gloves, and restricted zone violations
▸	Real-time video stream inference using OpenCV
▸	Alert logging for detection events with timestamp and confidence score
▸	87% mAP (mean Average Precision) on held-out test set

🛠 Tech Stack
Python  ·  YOLOv7  ·  OpenCV  ·  PyTorch  ·  LabelImg (annotation)  ·  NumPy

📈 Results
▸	✅  87% mAP on custom PPE/hazard detection dataset (2,000+ images)
▸	✅  Deployed as real-time monitoring pipeline at construction site
▸	✅  Improved hazard detection coverage and safety incident response time

📁 Project Structure
safety-detection/
├── data/
│   ├── images/          # Training images
│   └── labels/          # YOLO format annotations
├── models/
│   └── best.pt          # Trained YOLOv7 weights
├── detect.py            # Real-time detection script
├── train.py             # Training script
└── README.md

🚀 Getting Started
# Clone the repo
git clone https://github.com/krisanumanna/safety-detection-yolov7

# Install dependencies
pip install -r requirements.txt

# Run real-time detection on webcam
python detect.py --source 0 --weights models/best.pt

# Run on a video file
python detect.py --source video.mp4 --weights models/best.pt
