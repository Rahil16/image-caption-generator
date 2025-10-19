# 🧠 Image Caption Generator

This project demonstrates how **Transfer Learning** can be applied to automatically generate captions for images using a **Convolutional Neural Network (CNN)** and a **Recurrent Neural Network (RNN)** (specifically, an **LSTM**).  
The model combines **InceptionV3** (pre-trained on ImageNet) for visual feature extraction and an **LSTM network** for text sequence generation.

---

## 🎯 Objective

To build a deep learning model that can look at an image and describe it in natural language — showcasing understanding of both **computer vision** and **natural language processing** concepts through **transfer learning**.

---

## 🧩 Concept: What Is Transfer Learning?

Transfer learning means **reusing a model’s pre-learned knowledge** from one task to solve another, similar task.  
Instead of training a model from scratch (which requires a large dataset and computational power), we take a **pre-trained CNN** that already understands general image patterns (edges, colors, shapes) and **adapt it** for image captioning.

---

## ⚙️ How It Works

1. **Feature Extraction (Vision Part):**  
   - Use **InceptionV3**, a pre-trained CNN on ImageNet, to extract a 2048-length feature vector for each image.  
   - These features represent high-level visual understanding of the image.

2. **Caption Generation (Language Part):**  
   - Use an **LSTM** (Long Short-Term Memory) network to generate text sequences word-by-word.  
   - The LSTM learns how to describe the extracted features in natural language.

3. **Integration:**  
   - The CNN encodes the image → The LSTM decodes that information into words.  
   - The model is trained end-to-end to minimize caption prediction error.

---

## 🧪 Dataset

For this demonstration, a **small custom dataset** of sample images (soccer player, dog, and car) was used to keep runtime light and GPU usage minimal.  
Each image has a few manually defined captions for supervised training.

*Precisely the Flickr8k dataset was used.*

---

## 🚀 Model Architecture

- **Feature Extractor:** InceptionV3 (Transfer Learning)
- **Language Model:** LSTM with Embedding
- **Loss:** Categorical Crossentropy

---

## 🧰 Tech Stack

- Python  
- TensorFlow / Keras  
- NumPy, Pillow, Matplotlib  

---

## 🖼️ Example Output
<img width="593" height="468" alt="image" src="https://github.com/user-attachments/assets/aa6dbb88-503e-4f81-a5a1-ca7415ef0304" />


---

## 🧾 Results & Insights

- The model successfully learned to describe images in short, meaningful phrases.  
- Demonstrates **semantic understanding** (colors, actions, and objects).  
- Even with a small dataset, transfer learning helped achieve good generalization.






