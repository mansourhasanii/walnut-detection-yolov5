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

How to Run (Google Colab)

1. Clone YOLOv5 and install requirements
   
!git clone https://github.com/ultralytics/yolov5
%cd yolov5
!pip install -r requirements.txt

3. Mount Google Drive
text
from google.colab import drive
drive.mount('/content/drive')

4. Dataset configuration (dataset.yaml)
Example configuration:

train: /content/drive/MyDrive/walnut/WalnutData_subset/train/images
val: /content/drive/MyDrive/walnut/WalnutData_subset/valid/images

nc: 1
names: ["walnut"]

4. Train the model
   
!python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt

Results

The custom YOLOv5s model was trained for 73 epochs on a walnut detection dataset.

Best observed performance during training:

Precision: 0.90933

Recall: 0.84487

mAP@0.5: 0.92297

mAP@0.5:0.95: 0.54905

The final epochs show stable performance with only a slight decline in mAP, while precision and recall remained around 0.90 and 0.84 respectively.

These results demonstrate that the model performs well for walnut detection and could be further improved with more data or augmentation techniques.

Future Improvements

Increase dataset size
Apply stronger data augmentation
Implement walnut counting and grading system
Deploy as a real-time detection system

Contact

If you need a custom YOLO model or computer vision solution, feel free to reach out.

Available for freelance projects in:

Object Detection
Computer Vision Systems
AI Automation
Model Training and Fine-tuning
