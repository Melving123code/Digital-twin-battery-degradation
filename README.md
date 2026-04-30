# Digital Twin-Based Battery Degradation Prediction (Hybrid Physics + Neural Network)

## 📌 Overview

This project presents a **hybrid Digital Twin framework** for predicting lithium-ion battery degradation using the NASA battery dataset.

The approach combines:

* A **physics-based exponential decay model**
* A **neural network for residual learning**

The final prediction is computed as:

Digital Twin = Physical Model + Neural Network Residual

This hybrid approach improves prediction accuracy by combining domain knowledge with data-driven learning.

---

## 🚀 Key Features

* Physics-based battery degradation modeling
* Neural Network for residual error learning
* Hybrid Digital Twin system
* Data preprocessing and feature engineering
* Model evaluation using MAE and RMSE
* Visualization of battery degradation trends

---

## 🧠 Technologies Used

* Python
* Pandas & NumPy
* Scikit-learn
* TensorFlow / Keras (Neural Networks)
* Plotly / Matplotlib

---

## 📂 Project Structure

```
├── digitaltwin.ipynb     # Main notebook
├── discharge.csv         # NASA battery dataset
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## ⚙️ Methodology

### 1. Physical Model

An **exponential decay function** is used to estimate battery capacity over charge/discharge cycles.

### 2. Residual Learning (Neural Network)

A neural network is trained to learn the **difference (residual)** between:

* Physical model predictions
* Actual observed battery data

### 3. Digital Twin Model

The final prediction is:

Digital Twin = Physical Model + Neural Network Residual

This allows the model to capture both:

* Interpretable physical behavior
* Complex nonlinear patterns

---

## 📊 Dataset & Preprocessing

* Dataset: **NASA Lithium-Ion Battery Dataset**
* Battery used: **B0005**

Preprocessing steps:

* Filtered low-temperature samples
* Grouped data by cycle
* Computed cumulative time
* Generated physical model features
* Applied feature scaling (StandardScaler)

---

## 🏗️ Model Architecture

* Input Layer (4 features)
* Two Hidden Layers (ReLU activation)
* Output Layer (Residual prediction)

---

## 📊 Results

### Model Performance Comparison

* **Physical Model MAE:** 0.268

* **Digital Twin MAE:** 0.007

* **Physical Model RMSE:** 0.324

* **Digital Twin RMSE:** 0.010

### 🔍 Key Insight

The hybrid Digital Twin model significantly outperforms the standalone physical model.

The neural network successfully learns nonlinear degradation patterns that are not captured by the physical model alone, resulting in a dramatic reduction in prediction error.

---

## 📈 Discussion

* The physical model provides interpretability but lacks accuracy
* The neural network improves predictions by learning residual patterns
* The hybrid approach balances **accuracy + interpretability**

---

## ⚠️ Limitations

* Single battery dataset (B0005)
* Simplified physical model
* Limited hyperparameter tuning

---

## 🚀 Future Work

* Extend to multiple batteries
* Use advanced models (LSTM, RNN)
* Incorporate additional physical variables
* Deploy as a real-time Digital Twin system

---

## ▶️ How to Run

1. Clone the repository:

```
git clone https://github.com/Melving123code/Digital-twin-battery-degradation.git
```

2. Navigate to the folder:

```
cd Digital-twin-battery-degradation
```

3. Install dependencies:

```
pip install -r requirements.txt
```

4. Run the notebook:

```
jupyter notebook digitaltwin.ipynb
```

---

## 👨‍💻 Author

Melvin Gates
M.S. Computer Science (Data Science)
Florida A&M University

---

## 📜 License

This project is for educational and research purposes.
