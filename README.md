# 🌊 AquaSentinel  
## CNN-Based Flood Detection & Rescue Guidance System  

AquaSentinel is an AI-powered flood monitoring and rescue assistance system that leverages **Computer Vision, Deep Learning (U-Net), and GIS-based routing** to detect flooded regions and assist in disaster response.

Developed as part of **Applicative Project II – B.Tech CSE (AIML)**.

---

## 🚨 Problem Statement

Floods cause severe damage to:

- Human life  
- Infrastructure  
- Transportation networks  

Traditional flood monitoring systems are:

- Manual  
- Slow  
- Non-scalable  
- Delayed in rescue coordination  

AquaSentinel aims to automate flood detection and improve response time using deep learning.

---

## 🎯 Project Objectives

- Detect flooded regions automatically from satellite/video imagery  
- Segment flood boundaries using U-Net  
- Generate flood probability maps  
- Trigger visual alerts  
- Assist in rescue route planning using GIS logic  

---

## 🧠 System Overview

AquaSentinel integrates:

- 📷 Image Processing  
- 🧠 U-Net Deep Learning Segmentation  
- 🚨 Alert Engine  
- 🗺 GIS-Based Rescue Routing  
- 📊 Dashboard Visualization  

---

## 🏗 System Architecture

Input (Satellite Image / Video Frame)
↓
Preprocessing (Resize, Normalize)
↓
U-Net Segmentation Model
↓
Flood Probability Map
↓
Binary Flood Mask
↓
Boundary Extraction
↓
Alert Engine
↓
GIS Route Mapping
↓
Dashboard Output


---

## 🤖 Model Architecture

We use **U-Net**, an encoder–decoder convolutional neural network designed for pixel-wise segmentation.

### Model Features:

- Convolutional layers  
- ReLU activations  
- Max pooling (encoder)  
- Skip connections  
- Transposed convolution (decoder)  
- Sigmoid output layer  

### Input:
- RGB + NDWI (4 channels)  
- Patch size: 224×224 / 256×256  

### Output:
- Binary flood segmentation mask  

### Training Setup:
- Loss: Binary Cross-Entropy  
- Optimizer: Adam  
- Class imbalance handling  
- Gradient clipping  

---

## 🌊 Flood Detection Technique

1. Generate flood probability map  
2. Apply threshold to create binary mask  
3. Extract contours  
4. Identify flood boundary  
5. Overlay on original image  

Flood detected when:
Probability > Threshold


---

## 🗺 Rescue Route Mapping

AquaSentinel integrates GIS-based routing logic:

1. Extract flood zone coordinates  
2. Identify rescue team location  
3. Compute shortest safe path  
4. Overlay route on dashboard  

Visual Indicators:

- 🔴 Flood Zone  
- 🟢 Rescue Team  
- 🟡 Optimal Route  

---

## 🛠 Technologies Used

### Programming & ML
- Python  
- PyTorch  
- OpenCV  
- NumPy  

### Geospatial Processing
- Google Earth Engine  
- GeoTIFF handling  
- GIS-based routing logic  

### Deployment
- Google Colab  
- Dashboard framework  

---

## 📊 Results

- Flood probability heatmaps generated  
- Binary flood segmentation masks produced  
- Flood boundaries successfully extracted  
- Real-time simulation achieved  
- Rescue route overlay demonstrated  

---

## ⚠ Limitations

- NDWI-based ground truth may contain noise  
- Class imbalance affects IoU metric  
- Conservative predictions under strict thresholds  
- Limited real-time deployment integration  

---

## 🔮 Future Work

### Model Improvements
- Use Sentinel-1 SAR data for cloud-robust detection  
- Implement Attention U-Net  
- Hyperparameter optimization  

### System Expansion
- Integrate real GIS routing APIs  
- Connect with disaster management authorities  
- Deploy as Smart City flood monitoring module  
- Live CCTV / camera integration  

---

## 🔥 Vision Statement

**AquaSentinel functions as a digital sentinel, using CNN-based computer vision to monitor, detect, and assist in flood disaster response.**

---

## 👨‍💻 Team Members

- Deepak Kumar  
- Dubba Aakash  
- Sai Aashrith  
- Aashutosh Gautam  
- Sai Girish  

---

## 📌 License

For academic and research use.
