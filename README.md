Walnut Detection using YOLOv5
This project implements a custom YOLOv5-based object detection model for detecting walnuts in agricultural images.

The system can be used for real-world applications such as automated walnut counting, quality inspection, sorting, and yield estimation in agricultural environments.

Features
Custom-trained YOLOv5 model
Walnut detection in real images
Training pipeline implemented in Google Colab
Easy to reproduce and modify
Applicable to agricultural automation and quality control systems
Project Structure
text
walnut-detection-yolov5/
│
├── walnut_detection_yolov5.ipynb   # Main training and inference notebook
├── dataset.yaml                   # Dataset configuration file
├── results.csv                    # Training metrics
└── README.md
How to Run
1. Clone YOLOv5 and install requirements
bash
!git clone https://github.com/ultralytics/yolov5
%cd yolov5
!pip install -r requirements.txt
2. Mount Google Drive (Google Colab)
python
from google.colab import drive
drive.mount('/content/drive')
3. Prepare the dataset configuration
Example dataset.yaml configuration:

yaml
train: /content/drive/MyDrive/walnut/WalnutData_subset/train/images
val: /content/drive/MyDrive/walnut/WalnutData_subset/valid/images

nc: 1
names: ["walnut"]
4. Train the model
bash
!python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt
5. Run inference / detection
bash
!python detect.py --weights runs/train/exp/weights/best.pt --source path/to/test/images
Results
The custom YOLOv5s model was trained for 73 epochs on a walnut detection dataset.

Best observed performance during training:

Precision: 0.90933
Recall: 0.84487
mAP@0.5: 0.92297
mAP@0.5:0.95: 0.54905
These results show strong performance for walnut detection and suggest the model can be further improved with more data or augmentation.

Sample Detection Outputs
Below are sample images showing the model detecting walnuts in different environments.









Future Improvements
Increase dataset size
Apply stronger data augmentation
Implement walnut counting and grading
Deploy as a real-time detection system
Contact
If you need a custom YOLO model or computer vision solution, feel free to reach out.

Available for freelance projects in:

Object Detection
Computer Vision Systems
AI Automation
Model Training and Fine-tuning
