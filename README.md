# Malaria Detection Using Deep Learning (CNN)
This project focuses on detecting malaria-infected cells from microscopic blood smear images using Deep Learning (CNN).
The goal is to build an accurate model that can classify cells as Parasitized or Uninfected.

To achieve better performance, the training process was done in two stages:

1. Initial experimentation with limited data (malariadetection.ipynb).
2. Final training using the best model on a larger dataset (modelTraining.ipynb).

# Folder Explanation
**1. Experimentation phase (malariadetection.ipynb):** <br> 
This folder contains experiments done using a smaller subset of the dataset.
- Purpose:
    - Try different CNN architectures
    - Tune hyperparameters (epochs, batch size, optimizer, etc.)
    - Reduce training time during experimentation
- Outcome: Identification of the best performing model architecture
This step helped avoid overfitting and unnecessary computation.

**2. Final Training Phase (modelTraining.ipynb):** <br>
After selecting the best model, final training was done in this folder.
- Purpose:
    - Train the selected model on more data
    - Improve generalization and accuracy

# Tech Stack
- Programming Language: Python
- Deep Learning: CNN
- Frameworks: Pytorch
- Libraries: Pandas, Numpy, Matplotlib, scikit-learn, torch, torchvision
- Dataset: NIH Malarai Cell Images (Kaggle)

# Dataset
The dataset contains 27,558 cell images, where we got 13779 images of infected cell and remaining 13779 images of uninfected cell. Images that are present in the dataset are of the **Red Blood Cells**. <br>
Hear's a breakdown:
- The **uninfected cells** look uniform, smooth and mostly of single color (like purple).
- The **infected cells** show some purple spots or ring like structures. These are the plasmodium parasite inside the red blood cells.

**Note**: Plasmodim is a tiny organism that live in humans and mosquitoes. It is not a bacteria or virus, but a single-celled parasite.

# Key Highlights
- Two-phase training for better model selection
- Efficient experimentation using limited data
- Final model trained on larger dataset
- Clear and modular project structure

# What This Project Demonstrates
- Image preprocessing and classification
- Practical CNN implementation
- Deep learning workflow followed in real-world projects
- Model selection and optimization

# Future Enhancements
- Apply data augmentation
- Use transfer learning (ResNet, VGG16)
- Build a web app using Flask / FastAPI
- Deploy using Docker or cloud services