## Demo

Example walnut detection on video using the trained YOLOv5 model.

https://github.com/user-attachments/assets/b353425b-0036-4e91-b604-8dfeaae01320


Example walnut detection using the trained YOLOv5 model.

![Sample 3](https://github.com/user-attachments/assets/efcf400f-4c70-4bd0-acc4-a3dc6e32074f)

Walnut Detection using YOLOv5

This project implements a custom YOLOv5 model for walnut detection using an agricultural dataset.

The system can be used for real-world applications such as automated walnut counting, quality inspection, sorting, and yield estimation in agricultural environments.

Features

Custom-trained YOLOv5 model
Walnut detection in real images
Training pipeline implemented in Google Colab
Easy to reproduce and modify
Applicable to agricultural automation and quality control systems

Project Structure

walnut_detection_yolov5.ipynb — Main training and inference notebook

dataset.yaml — Dataset configuration file

weights/ — (Optional) trained model weights

## How to Run

### 1. Clone YOLOv5 and install requirements

!git clone https://github.com/ultralytics/yolov5
%cd yolov5
!pip install -r requirements.txt

### 2. Mount Google Driv

from google.colab import drive
drive.mount('/content/drive')

### 3. Prepare the dataset configuration

Example configuration:

train: /content/drive/MyDrive/walnut/WalnutData_subset/train/images
val: /content/drive/MyDrive/walnut/WalnutData_subset/valid/images

nc: 1
names: ["walnut"]

### 4. Train the model

!python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt

### 5. Run inference / detection


## Results
The custom YOLOv5s model was trained for 73 epochs on a walnut detection dataset.

**Best observed performance during training:**
- Precision: 0.90933
- Recall: 0.84487
- mAP@0.5: 0.92297
- mAP@0.5:0.95: 0.54905

These results show strong performance for walnut detection and suggest the model can be further improved with more data or augmentation.

## Sample Detection Outputs

Below are sample images showing the model detecting walnuts in different environments:

![Sample 1](https://github.com/user-attachments/assets/7ab2e275-a250-48f0-8a9f-3f926f753832)
![Sample 2](https://github.com/user-attachments/assets/ad4239f5-b748-489a-8a67-a322d0f49d55)
![Sample 3](https://github.com/user-attachments/assets/efcf400f-4c70-4bd0-acc4-a3dc6e32074f)
![Sample 4](https://github.com/user-attachments/assets/3d8d8a63-0ab0-4b4c-b62f-c3b4b1452232)


![Sample 1](https://github.com/user-attachments/assets/7ab2e275-a250-48f0-8a9f-3f926f753832)


## Future Improvements
- Increase dataset size
- Apply stronger augmentation
- Implement walnut counting and grading
- Deploy as a real-time detection system

## Contact
If you need a custom YOLO model or computer vision solution, feel free to reach out.

Available for freelance projects in:

Object Detection
Computer Vision Systems
AI Automation
Model Training and Fine-tuning
