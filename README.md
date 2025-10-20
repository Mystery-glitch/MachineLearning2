# Malaria Detection
In this project our aim is to identify whether a cell is infected or not. We used various normalization techniques such as **min-max normalization**, **z-score normalization**, **mean normalization**, **per-image standardization**, and **histogram equalization**.

## Normalization Techniques Summary

| Technique | Output Range | Formula | Uses | Common In |
|------------|--------------|---------|------|------------|
| **Min–Max** | [0, 1] | `x' = (x - min(x)) / (max(x) - min(x))` | General deep learning | CNNs |
| **Z-score** | mean=0, std=1 | `x' = (x - μ) / σ` | Pretrained models | ResNet, VGG |
| **Mean Normalization** | [-1, 1] | `x' = x / 127.5 - 1` | GANs, autoencoders | GANs |
| **Per-Image Standardization** | varies | `x' = (x - mean(x)) / std(x)` | Custom datasets | Image preprocessing |
| **Histogram Equalization** | [0, 255] | – (conceptual) | Contrast enhancement | Grayscale images |
