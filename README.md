# YOLO-PROJECT
This study covers the full pipeline of YOLOv11 and YOLOv12 models for aerial target and PCB defect detection, including data prep, annotation conversion, training (nano to large variants), evaluation, export, and deployment. It compares YOLOv11 vs YOLOv12 on speed, precision, recall, and mAP.


Here is a detailed README.md file tailored for your GitHub repository that explains how to set up and activate a Conda environment using your packed .tar file (yolov12_model_env.tar), and how to run your YOLOv12 models.

markdown
# 🚀 YOLOv12 & YOLOv11-Based Aerial Object & PCB Defect Detection

This project demonstrates the training and deployment of state-of-the-art object detection models (YOLOv11 & YOLOv12) for two real-world use cases:
- 🛡️ Aerial Target Object Detection (Defense Applications)
- 🧩 PCB Defect Detection (Industrial Automation)

The repository includes:
- Pretrained `.pt` models
- The full Conda environment packed as `yolov12_model_env.tar`
- YAML files and scripts to run training and inference

---

## 📦 Setup Guide

This project uses a **pre-packed Conda environment** for reproducibility.

### ✅ Prerequisites

- [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution)
- Python ≥ 3.10
- Git
- conda-pack(already used to pack the environment)

---

## 🔧 1. Extract & Setup the Conda Environment

✅ Step 1: Clone the Repository

Open **VS Code Terminal** or **Command Prompt** and run:

git clone https://github.com/VLaxmiNarayanSharma/YOLOv11_12-PROJECT.git

cd YOLOv11_12-PROJECT


Step 2: Unpack the Conda environment


mkdir yolov12_env

tar -xzf yolov12_model_env.tar -C yolov12_env


Step 3: Activate the environment (Linux/macOS)

🔹 For Linux / macOS:

source yolov12_env/bin/activate

🔹 For Windows CMD:

yolov12_env\Scripts\activate.bat

🔹 For VS Code Terminal (Windows PowerShell):

& .\yolov12_env\Scripts\Activate.ps1

2. Run Inference or Training

You can now run your YOLOv12 or YOLOv11 code using:

bash
python inference.py


Or retrain models with:

bash
python train.py --model yolo12l.pt --data pcb.yaml --epochs 60


---

## 📁 Included Files

| File / Folder           | Description                                          |
| ----------------------- | ---------------------------------------------------- |
| `yolov12_model_env.tar` | Packed Conda environment (Python 3.10 + Ultralytics) |
| `best.pt`               | Trained YOLO model weights                           |
| `pcb.yaml`              | Dataset config file for PCB defect dataset           |
| `inference.py`          | Run inference using trained weights                  |
| `train.py`              | Custom training script                               |

---

## 🧠 Notes

* This environment includes `ultralytics`, `torch`, `opencv-python`, and other key libraries.
* Ideal for offline inference or deploying on air-gapped systems.
* Exported using `conda-pack` to ensure binary compatibility.

---

Unpack on Another System
Send yolov12_env.tar.gz to a server or another machine, and run:


mkdir yolov12-env
tar -xzf yolov12_env.tar.gz -C yolov12-env
source yolov12-env/bin/activate
Now the environment is live. Run:

python inference.py

https://github.com/VLaxmiNarayanSharma/YOLOv11_12-PROJECT/releases/download/v1/yolo_env_pcb.tar.gz

Respected mam
Please use the above github link to extract and download the yolo_env_pcb.tar.gz file 
and please keep file in an empty folder and use the below code in the folder terminal

tar -xvzf yolo_env_pcb.tar.gz

This command will extract the project folder with .pt files, .ipynb and .py files (for training and testing models), along with inference.py file, .yaml file and training and testing data.

Than we can use change directory using command cd YOLOv11_v12_PROJECT and run inference.py file using ( python inference.py ) command .
https://drive.google.com/file/d/13HZabUJg8mQw3Zm2nYI7E2eq_muA3oLA/view?usp=sharing

##Drive Link to download YOLO PCB Environment
https://drive.google.com/file/d/1hyScRYRRFoIkIB46Tmy85q161mn59VDo/view?usp=sharing


cd ~/Downloads  # or the directory where the file is located

mkdir LINUX_PCB_env
tar -xzf LINUX_PCB_env.tar.gz -C LINUX_PCB_env

source ~/miniconda3/etc/profile.d/conda.sh

source ~/anaconda3/etc/profile.d/conda.sh

cd LINUX_PCB_env

./bin/conda-unpack

source bin/activate

