# Malaria Detection
In this project our aim is to identify whether a cell is infected or not. We used various normalization techniques such as **min-max normalization**, **z-score normalization**, **mean normalization**, **per-image standardization**, and **histogram equalization**.

# 🖼️ Image Normalization Techniques

Image normalization makes **training stable and faster** by ensuring all images have **similar scales**.  
It helps the model learn better and avoid being biased toward large pixel values.

---

## ⚙️ 1. Min–Max Normalization
**Goal:** Convert pixel values from **0–255** to **0–1** range.  

**Why:**  
Keeps all pixel values small and consistent, which helps neural networks train faster.  

**Formula:**  
\[
x' = \frac{x - \text{min}(x)}{\text{max}(x) - \text{min}(x)}
\]

---

## 📊 2. Z-score Normalization (Standardization)
**Goal:** Normalize data using **mean** and **standard deviation**.  

**Why:**  
Makes data have **mean = 0** and **std = 1**, improving model stability.  

**Formula:**  
\[
x' = \frac{x - \mu}{\sigma}
\]

---

## ⚖️ 3. Mean Normalization
**Goal:** Scale pixel values to the range **[-1, 1]**.  

**Why:**  
Some models (like GANs) perform better when values are between -1 and 1.  

**Formula:**  
\[
x' = \frac{x}{127.5} - 1
\]

---

## 🧮 4. Per-Image Standardization
**Goal:** Normalize each image **individually** so that every image has **zero mean** and **unit standard deviation**.  

**Why:**  
Useful when images vary in brightness or lighting.  

**Formula:**  
\[
x' = \frac{x - \text{mean}(x)}{\text{std}(x)}
\]

---

## 🌈 5. Histogram Equalization
**Goal:** Improve image **contrast** by spreading out intensity values evenly.  

**Why:**  
Makes dark areas lighter and bright areas clearer, helping the model detect features better.  

**Concept:**  
Redistribute pixel intensities to achieve a **uniform histogram** (equal distribution of pixel brightness).

---

## ✅ Summary Table

| Technique | Output Range | Uses | Common In |
|------------|--------------|------|------------|
| **Min–Max** | [0, 1] | General deep learning | CNNs |
| **Z-score** | mean=0, std=1 | Pretrained models | ResNet, VGG |
| **Mean Normalization** | [-1, 1] | GANs, autoencoders | GANs |
| **Per-Image Standardization** | varies | Custom datasets | Image preprocessing |
| **Histogram Equalization** | [0, 255] | Contrast enhancement | Grayscale images |
