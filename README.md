# Chip Image Detector using YOLO

This repository contains a script to perform object detection specifically for **chip images**, using a YOLO model. It supports detecting objects in:

- single images  
- batches of images in a folder  
- video files  
- live camera (USB/FaceTime) input  

It has been modified to properly support the FaceTime HD camera on macOS by using the `AVFoundation` backend.

---

## 📦 Contents

| File / Directory | Description |
|------------------|-------------|
| `yolo_detect.py` | Main Python script with inference loop. Supports multiple source types including FaceTime camera (USB). |
| `models/`       | Directory for storing your YOLO `.pt` model file(s). |
| `data/`         | Folder for chip images (single images or batch). |
| `videos/`       | Optional folder for video samples for detection. |
| `README.md`     | This documentation file. |

---

## 🛠 Setup

1. Clone the repo:

   ```bash
   git clone <repository_url>
   cd <repository_dir>
---

## 🎯 Usage

Here’s how to run detection depending on your source type.

| Source Type              | Command Example |
|---------------------------|-----------------|
| **Single Image**          | ```bash
python yolo_detect.py --model models/my_model.pt --source data/chip.jpg --source-type image

| **Folder of Images**      | ```bash
python yolo_detect.py --model models/my_model.pt --source data/chips_folder/ --source-type folder

| **Video file**            | ```bash
python yolo_detect.py --model models/my_model.pt --source videos/chips_video.mp4 --source-type video

| **FaceTime / USB camera** | ```bash
python yolo_detect.py --model models/my_model.pt --source 0 --source-type usb
``` |


