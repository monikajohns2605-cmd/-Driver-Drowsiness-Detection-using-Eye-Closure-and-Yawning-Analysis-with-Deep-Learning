🧠 Driver Drowsiness Detection using Deep Learning

A Computer Vision and Deep Learning project that detects driver fatigue using eye closure and yawning analysis.
The system classifies facial images into Open, Closed, Yawn, and No_Yawn and further derives driver fatigue levels.

This project demonstrates Transfer Learning using MobileNetV2, image preprocessing, model evaluation, and rule-based fatigue classification.

🚗 Problem Statement

Driver fatigue significantly reduces reaction time, alertness, and decision-making ability, increasing the risk of road accidents.

Traditional detection methods rely on vehicle behavior or wearable sensors, which are often unreliable or intrusive.

This project proposes a vision-based driver monitoring system that detects fatigue using facial indicators such as eye closure and yawning.

🎯 Objectives

• Detect driver fatigue using deep learning and computer vision
• Classify images into eye and mouth states
• Implement Transfer Learning (MobileNetV2)
• Design a 3-level fatigue classification system
• Visualize fatigue progression over time

🧠 Tech Stack

Programming Language

• Python

Deep Learning

• TensorFlow
• Keras

Computer Vision

• OpenCV

Visualization

• Matplotlib
• Seaborn

Model Architecture

• MobileNetV2 (Transfer Learning)

📂 Dataset Structure

The dataset consists of facial images categorized into four classes.

dataset/
   train/
      Open/
      Closed/
      yawn/
      no_yawn/

Each folder contains images representing driver eye or mouth states.

🛠 Data Preprocessing

The following preprocessing steps were applied:

• Image resizing → 224 × 224
• Pixel normalization (0–1 range)
• Data augmentation

Rotation

Zoom

Brightness variation

Horizontal flipping

These techniques improve model robustness to lighting and pose variations.

🧠 Model Architecture

The project uses Transfer Learning with MobileNetV2.

Steps:

1️⃣ Load pretrained MobileNetV2 (ImageNet weights)

2️⃣ Freeze base layers

3️⃣ Add custom classification head

GlobalAveragePooling
Dense (256)
Dropout
Dense (4 classes - Softmax)
⚙️ Training Configuration
Parameter	Value
Image Size	224 × 224
Batch Size	32
Optimizer	Adam
Learning Rate	0.0001
Loss Function	Categorical Crossentropy
Epochs	10
📊 Model Evaluation

The model was evaluated using:

• Accuracy
• Confusion Matrix
• Precision
• Recall

Accuracy and Loss Curve

The training process visualizes:

• Training accuracy
• Validation accuracy
• Training loss
• Validation loss

🧠 Fatigue Decision Logic

Instead of directly using the four classes, a 3-level fatigue classification is implemented.

Prediction	Fatigue Level
Open	Alert
No_Yawn	Alert
Yawn	Mild Fatigue
Closed	Severe Fatigue
📈 Driver Fatigue Progression Curve

The system simulates a driving session by processing sequential predictions and mapping them to fatigue stages.

The resulting graph visualizes how driver fatigue changes over time.

Alert → Mild Fatigue → Severe Fatigue
🚀 How to Run the Project
1️⃣ Clone the repository
git clone https://github.com/yourusername/driver-drowsiness-detection.git
2️⃣ Install dependencies
pip install tensorflow opencv-python scikit-learn seaborn matplotlib
3️⃣ Run the notebook
jupyter notebook drowsiness_detection.ipynb
📊 Results

The deep learning model successfully detects driver fatigue indicators.

Key outcomes:

✔ Accurate classification of eye and mouth states
✔ Effective fatigue level detection
✔ Robust performance under augmented image conditions

📦 Project Deliverables

• End-to-end deep learning pipeline
• Trained MobileNetV2 model
• Accuracy and loss visualizations
• Confusion matrix evaluation
• Fatigue progression analysis

🌟 Future Improvements

• Real-time driver monitoring using webcam
• Alarm system for fatigue detection
• Integration with Advanced Driver Assistance Systems (ADAS)
• Deployment using Flask / Streamlit
