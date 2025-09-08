# 🌍 Global Agriculture: AI for Sustainable Farming  

## 📌 Overview  
Agriculture sustains life on Earth 🌱, but challenges like **crop diseases, climate change, and soil degradation** threaten global food security.  
This project leverages **AI/ML techniques** to contribute towards **sustainable agriculture** by enabling **plant disease detection** and smarter decision-making for farmers.  

---

## 📂 Dataset  
📥 Sourced from **Kaggle**  
- Focused on **plant disease classification** (healthy vs. diseased leaves 🌿).  
- Compact & easy-to-use dataset for quick experimentation.  
- Each image is preprocessed for **consistency & model readiness**.  

---

## ⚙️ Preprocessing Steps  
✔️ **Image Resizing** → all images resized to **128×128 pixels**  
✔️ **Normalization** → pixel values scaled (0–255 → 0–1)  
✔️ **Label Encoding** → categorical labels → numeric → one-hot vectors  
✔️ **Train-Test Split** → 80% training | 20% testing  
✔️ **Saved Arrays** → stored as `.npy` for quick loading  

---

## 📁 Project Structure  
global_agriculture/
│
├── preprocess.ipynb              # Jupyter notebook with preprocessing pipeline  
├── X_train.npy                   # Preprocessed training images  
├── X_test.npy                    # Preprocessed testing images  
├── y_train.npy                   # One-hot encoded training labels  
├── y_test.npy                    # One-hot encoded testing labels  
├── task2_training.ipynb          # Model training + evaluation + charts  
├── linear_regression_model.pkl   # Saved ML model  
└── README.md                     # Documentation  



---

## 🚀 How to Use  
1️⃣ Clone this repository:  
```bash
git clone https://github.com/Susovan700/global_agriculture.git
cd global_agriculture
jupyter notebook preprocess.ipynb

2️⃣ Run preprocessing (if not using saved `.npy` files):  
```bash
jupyter notebook preprocess.ipynb
import numpy as np
3️⃣ Load preprocessed data for training:
X_train = np.load("X_train.npy")
X_test  = np.load("X_test.npy")
y_train = np.load("y_train.npy")
y_test  = np.load("y_test.npy")
4️⃣ Load pre-trained model:

import joblib
model = joblib.load("linear_regression_model.pkl")


## 🤖 Model Training  
- Implemented **Linear Regression** to analyze climate–agriculture relationships.  
- Evaluated performance using **MSE, R², and visualization charts**.  
- Model saved as `linear_regression_model.pkl` for reuse.  

### 📊 Charts & Visualizations  
- Correlation heatmap between climate factors and yield  
- Line plots of predicted vs. actual yields  
- Bar graph showing feature importance  
- Pie chart distribution of healthy vs. diseased samples  

