# Malaria Detection
In this project our aim is to identify whether a cell is infected or not. We used various normalization techniques such as **min-max normalization**, **z-score normalization**, **mean normalization**, **per-image standardization**, and **histogram equalization**.

# Normalizaion Techniques
## Min-Max Normalization

Min-Max normalization scales the pixel values of an image to a fixed range, usually [0, 1].

**Formula:**  
$$
x' = \frac{x - x_{min}}{x_{max} - x_{min}}
$$

**Where:**  
- \(x\) = original pixel value  
- \(x_{min}\) = minimum pixel value in the image  
- \(x_{max}\) = maximum pixel value in the image  
- \(x'\) = normalized pixel value

**Usage:**  
- Brings all pixel values to a common scale  
- Useful when the input values have different ranges

---

## 2. Z-Score Normalization (Standardization)

Z-score normalization standardizes the image data to have a mean of 0 and a standard deviation of 1.

**Formula:**  
$$
z = \frac{x - \mu}{\sigma}
$$

**Where:**  
- \(x\) = original pixel value  
- \(\mu\) = mean of pixel values  
- \(\sigma\) = standard deviation of pixel values  
- \(z\) = normalized pixel value

**Usage:**  
- Commonly used in deep learning models  
- Helps in faster convergence of gradient-based optimization

---

## 3. Mean Normalization

Mean normalization scales the pixel values based on the mean and the range of the dataset.

**Formula:**  
$$
x' = \frac{x - \mu}{x_{max} - x_{min}}
$$

**Where:**  
- \(x\) = original pixel value  
- \(\mu\) = mean of pixel values  
- \(x_{min}\) = minimum pixel value  
- \(x_{max}\) = maximum pixel value  
- \(x'\) = normalized pixel value

**Usage:**  
- Centers the data around 0  
- Reduces the bias due to varying scales

---

## 4. Per-Image Standardization

Per-image standardization normalizes each image individually by subtracting its mean and dividing by its standard deviation.

**Formula:**  
$$
x' = \frac{x - \text{mean}(x)}{\max(\text{std}(x), \epsilon)}
$$

**Where:**  
- \(x\) = original pixel value  
- \(\text{mean}(x)\) = mean of pixel values of the image  
- \(\text{std}(x)\) = standard deviation of pixel values of the image  
- \(\epsilon\) = small constant to avoid division by zero  
- \(x'\) = normalized pixel value

**Usage:**  
- Standardizes each image independently  
- Useful in neural networks like CNNs to improve stability

---

## 5. Histogram Equalization

Histogram equalization enhances the contrast of an image by redistributing pixel intensity values.

**Algorithm:**  
1. Compute the histogram of the image.  
2. Compute the cumulative distribution function (CDF).  
3. Map the original pixel values to the equalized values using the CDF.

**Usage:**  
- Improves visual quality of images  
- Useful for images with poor contrast  

---