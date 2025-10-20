# Malaria Detection
In this project our aim is to identify whether a cell is infected or not. We used various normalization techniques such as **min-max normalization**, **z-score normalization**, **mean normalization**, **per-image standardization**, and **histogram equalization**.

## 1. Min–Max Normalization
**Formula:**  
`x' = (x - min(x)) / (max(x) - min(x))`

---

## 2. Z-score Normalization (Standardization)
**Formula:**  
`x' = (x - μ) / σ`

---

## 3. Mean Normalization
**Formula:**  
`x' = x / 127.5 - 1`

---

## 4. Per-Image Standardization
**Formula:**  
`x' = (x - mean(x)) / std(x)`

---

## 5. Histogram Equalization
**Goal:** Improve image **contrast** by spreading out intensity values evenly.  
Makes dark areas lighter and bright areas clearer, helping the model detect features better.  

---

## ✅ Summary Table

| Technique | Output Range | Uses | Common In |
|------------|--------------|------|------------|
| **Min–Max** | [0, 1] | General deep learning | CNNs |
| **Z-score** | mean=0, std=1 | Pretrained models | ResNet, VGG |
| **Mean Normalization** | [-1, 1] | GANs, autoencoders | GANs |
| **Per-Image Standardization** | varies | Custom datasets | Image preprocessing |
| **Histogram Equalization** | [0, 255] | Contrast enhancement | Grayscale images |
