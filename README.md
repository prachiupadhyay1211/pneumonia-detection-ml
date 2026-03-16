# MediScan AI – Pneumonia Detection from Chest X-Rays

**MediScan AI** is a deep-learning powered web application that analyzes chest X-ray images and predicts whether the lungs show signs of **Pneumonia** or are **Normal (Healthy)**.

The system uses a trained convolutional neural network based on MobileNet to perform image classification and provides a clean, interactive interface for users to upload X-rays and view predictions.

The project is designed as an educational medical-AI platform demonstrating how deep learning can assist in preliminary radiology screening.

---

# Features

• Chest X-ray image upload (click or drag & drop)
• AI-based pneumonia detection using a trained deep learning model
• Binary classification: **PNEUMONIA** or **NORMAL**
• Displays prediction confidence score
• Informational landing page about pneumonia
• Health charts and educational sections
• Recovery timeline and FAQ module
• Responsive modern UI

---

# Tech Stack

Backend
Python
Flask

Deep Learning
TensorFlow
Keras
MobileNetV2 (Transfer Learning)

Frontend
HTML5
CSS3
JavaScript
Jinja2 Templates

Environment
Git
Virtual Environment (venv)

---

# Project Structure

```
pneumonia-detection-ml
│
├── app.py
├── train_model.py
├── pneumonia_mobilenet_best.h5
├── requirements.txt
├── README.md
│
├── dataset
│   ├── train
│   │   ├── NORMAL
│   │   └── PNEUMONIA
│   ├── test
│   │   ├── NORMAL
│   │   └── PNEUMONIA
│
├── templates
│   ├── first.html
│   ├── index.html
│   ├── charts.html
│   ├── timeline.html
│   └── faq.html
│
└── static
    └── uploads
```

---

# Running the Project Locally

## 1 Clone the repository

```
git clone https://github.com/prachiupadhyay1211/pneumonia-detection-ml.git
cd pneumonia-detection-ml
```

---

## 2 Create a virtual environment

```
python3 -m venv env
```

Activate environment

Mac / Linux

```
source env/bin/activate
```

Windows

```
env\Scripts\activate
```

---

## 3 Install dependencies

```
pip install -r requirements.txt
```

---

## 4 Ensure model file exists

Place the trained model in the project root:

```
pneumonia_mobilenet_best.h5
```

The application loads it using:

```
model = load_model("pneumonia_mobilenet_best.h5")
```

---

## 5 Run the Flask application

```
python3 app.py
```

Open browser:

```
http://127.0.0.1:5000
```

---

# Application Flow

Landing Page
Provides information about pneumonia, symptoms, prevention, and educational resources.

AI Detection Page
Users upload a chest X-ray image.

Prediction Pipeline

1. Image uploaded
2. Image resized to 224×224
3. Normalization applied
4. Deep learning model performs prediction
5. Result displayed with confidence score

Possible outputs:

PNEUMONIA
NORMAL

---

# Model Details

Model Architecture
MobileNetV2 based Convolutional Neural Network

Input
Chest X-ray images resized to 224 × 224

Preprocessing

```
x = img / 255.0
```

Output Layer

Binary classification using sigmoid activation.

---

# Dataset

This project uses the **Chest X-Ray Pneumonia Dataset**.

Dataset Link

https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

Classes used:

NORMAL
PNEUMONIA

---

# Screenshots

Landing Page
AI Detector Upload Page
Prediction Result Page

(Add screenshots inside the screenshots/ folder)

---

# Future Improvements

• Grad-CAM lung infection heatmap visualization
• Model performance dashboard
• Improved dataset balancing
• Deployment using Docker or cloud hosting

---

# Author

Prachi Upadhyay

GitHub
https://github.com/prachiupadhyay1211

LinkedIn
https://www.linkedin.com/in/prachi-upadhyay-926487301/
