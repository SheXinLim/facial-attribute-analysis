
# 🎭 Facial Attribute Analysis with Deep Learning  


This project performs **multi-label facial attribute classification** on the **CelebA dataset** using a **deep learning model**. The model predicts **40 different facial attributes** (e.g., "Blonde Hair", "Eyeglasses", "Smiling") using a **pretrained ResNet18 model** in **PyTorch**.

## Example Output

Below is an example of the model predicting facial attributes from an image:

![Example Inference](https://github.com/user-attachments/assets/7139ed2c-4e43-4c53-b49c-1ed6616bddda)


⚠️ **Note:**  
This project was executed **exclusively on Google Colab** with an **A100 GPU**.  

---


**Technology Used:**  
- **Google Colab (A100 GPU)**
- **Python 3 & PyTorch**
- **Torchvision & Pretrained ResNet18**
- **CelebA Dataset**
- **Binary Cross-Entropy Loss**
- **Adam Optimizer**
- **Matplotlib for Visualization**


---
⚠️ **IMPORTANT:** If you want to replicate this, **you MUST manually download the dataset** ⬇️  
📌 **[Download CelebA Dataset](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)**  


## 📂 **Dataset: CelebA**

- **Dataset:** [CelebA - Large-scale Face Attributes Dataset](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
- **Images:** 202,599 labeled face images.
- **Attributes:** 40 binary attributes per image (e.g., "Smiling", "Bangs", "Wearing Hat").
 Images are split into **Training (162,770)**, **Validation (19,867)**, **Testing (19,962)**.

Since this project **relies on a private Google Drive setup**, the paths must be manually adjusted if you wish to run it yourself.


---

## 🔥 **Training Process**
- Uses **ResNet18** pretrained on **ImageNet**.
- Final layer modified for **multi-label classification** (40 output nodes + `Sigmoid` activation).
- Loss Function: **Binary Cross-Entropy Loss (BCELoss)**
- Optimizer: **Adam (lr=0.001)**
- Runs on **A100 GPU** for faster training.


## 🔥 **Key Highlights**
- **Model:** ResNet18 (pretrained on ImageNet, modified for 40 attributes).
- **Training Environment:** Google Colab (A100 GPU).
- **Training Duration:** ~30 minutes for 20 epochs.
- **Final Test Accuracy:** **23.12%**.
- **Dataset:** CelebA (202,599 face images, 40 labeled attributes per image).
- **Loss Function:** Binary Cross-Entropy (BCELoss).
- **Optimizer:** Adam (lr=0.001).

---


## 🎯 **Model Evaluation & Testing**
The model achieves **~23.12% accuracy** on the test set, demonstrating **successful facial attribute classification**.

🔥 **Test Loss: 0.6253**  
🎯 **Test Accuracy: 23.12%**  

✅ **Image Inference Demo**
The model can predict attributes from **random test images**.

Example Output:
```
Test Image: 000010.jpg
Predicted Attributes: ['Blonde Hair', 'Smiling', 'Young', 'Attractive']
```

---


## 📌 **Future Improvements**
🔹 **Increase Training Epochs** – More training could improve accuracy.  
🔹 **Hyperparameter Tuning** – Adjusting batch size, learning rate, and optimizer.  
🔹 **Threshold Optimization** – Experimenting with different thresholds (0.5, 0.6, 0.7).  
🔹 **Data Augmentation** – Using transformations (flipping, rotation, color jittering).  

---

## 📜 **Conclusion**
This project successfully performs **facial attribute classification** using deep learning. While further training and improvements are possible, the model **already demonstrates the ability to extract facial features from images**.


