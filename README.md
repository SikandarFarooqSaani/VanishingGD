# VanishingGD
# 🧠 Understanding Gradient Descent & Vanishing Gradient Problem Using Keras  
**AI Generated README**

---

## 📘 Overview
This experiment demonstrates the **vanishing gradient problem** in deep neural networks using **Keras**.  
It shows how activation functions like **Sigmoid** can lead to very small gradients and slow learning, and how **ReLU** helps overcome this issue.

---

## ⚙️ Steps and Process

### **1. Dataset Creation**
- A **synthetic dataset** was created for binary classification.
- A **scatter plot** of the datapoints was visualized.  
  🖼️ *Image 1 attached.*

---

### **2. Model with Sigmoid Activation**
- Built a deep neural network with:
  - **10 hidden layers**, each using **Sigmoid activation**.
  - **2 input features** and **1 output node** with **Sigmoid**.
- **Model Summary** displayed 10 dense layers with small weight sizes.

---

### **3. Compilation**
- **Loss:** Binary Crossentropy  
- **Optimizer:** Adam  
- **Metric:** Accuracy  

---

### **4. Training**
- Split data into **train** and **test** sets.
- Trained the model for **100 epochs**.
- Stored **initial weights** before training to analyze changes later.

---

### **5. Gradient Analysis**
- Calculated **learning rate**, **gradients**, and **percentage change** in weights.
- Observed **very minimal weight updates** across epochs.  
  ➤ This confirms the **Vanishing Gradient Problem**, where gradients shrink exponentially in deeper layers, preventing effective learning.

---

### **6. Model with ReLU Activation**
- Built a new model with the **same architecture**, replacing **Sigmoid** with **ReLU**.
- Repeated all the above steps.

✅ **Visible difference observed:**
- Gradients were **larger and more stable**.
- Weight updates were **significant**, allowing the model to learn better.

---

## 🔍 Key Insights

| Activation Function | Gradient Behavior | Learning Efficiency |
|----------------------|-------------------|----------------------|
| **Sigmoid** | Gradients vanish (very small) | Poor learning |
| **ReLU** | Gradients stable and large | Better learning |
| **Leaky ReLU** | Prevents “dying ReLU” | Recommended alternative |

---

## 🧩 Observations
- **Vanishing Gradient Problem:**  
  Happens when using Sigmoid or Tanh activations in deep networks — gradients become too small to update weights effectively.
- **Solution:**  
  Use ReLU or Leaky ReLU activations, or reduce model complexity.

---

## 📎 Attachments
- **<img width="567" height="413" alt="vg1" src="https://github.com/user-attachments/assets/cdc96b3e-9a94-466f-8c3a-8e0c0f9c29cc" />
** Scatter plot of data points.
- **Gradient comparison:** Observations of minimal vs. visible weight changes.

---

> ⚠️ *This README is AI-generated to explain how the vanishing gradient problem occurs and how activation choice affects learning efficiency.*
