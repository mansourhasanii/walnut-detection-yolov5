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
```bash  
!git clone https://github.com/ultralytics/yolov5
%cd yolov5
!pip install -r requirements.txt

### 2. Mount Google Drive
```bash
text
from google.colab import drive
drive.mount('/content/drive')

### 3. Prepare the dataset configuration
```bash
Example configuration:

train: /content/drive/MyDrive/walnut/WalnutData_subset/train/images
val: /content/drive/MyDrive/walnut/WalnutData_subset/valid/images

nc: 1
names: ["walnut"]

### 4. Train the model
```bash
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
<img width="1024" height="1024" alt="Sample 1" src="https://github.com/user-attachments/assets/a8aebdde-67b0-4bd2-9659-f6b139c6a531" />
<img width="1024" height="1024" alt="Sample 2" src="https://github.com/user-attachments/assets/63866936-b2b5-45b6-a504-7ef8944489ca" />
<img width="1024" height="1024" alt="Sample 3" src="https://github.com/user-attachments/assets/e13cb016-16e1-44a1-b950-feeed4b16f6b" />
<img width="1024" height="1024" alt="Sample 4" src="https://github.com/user-attachments/assets/e8365e55-ff0d-47ce-bb38-bc67515b4bc2" />


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
