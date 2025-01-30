# VISI-TAG: Automated Product Attribute Prediction for E-Commerce

E-commerce platforms often struggle with inaccurate product descriptions. Sellers may input incorrect attributes, leading to customer dissatisfaction and return costs. This project aims to:
- Develop an ML model that predicts product attributes from images.
- Assist sellers in filling product details efficiently.
- Enhance the accuracy and reliability of online product catalogs.

## Introduction
**VISI-TAG** is an AI-powered solution that enhances e-commerce product cataloging by automatically predicting product attributes (such as color, pattern, and sleeve length) directly from images. By leveraging deep learning and computer vision techniques, VISI-TAG ensures that product listings are more accurate and efficient, minimizing discrepancies between images and textual descriptions.


## Technologies Used
VISI-TAG is built using a combination of modern AI frameworks and web technologies:
   * PyTorch & Torchvision
   * ResNet18 (Pretrained CNN Model)
   * PIL & OpenCV for image processing
   * Tesseract OCR (optional for text extraction)


## Installation Guide
To set up VISI-TAG on your local system, follow these steps:

### Clone the Repository
```sh
git clone https://github.com/your-username/VISI-TAG.git
cd VISI-TAG
```
1. Download repository
2. Install Parcel by typing the following command: npm install parcel -g
3. Make sure to install dependencies: open project in VSCode -> open command line -> type: npm install
4. Run Parcel by typing this command: npm parcel ./src/index.html


## Evaluation Metrics
- **Harmonic Mean of Macro & Micro F1-Score** for each attribute
- Averaging F1-scores across categories and attributes

---

## Download dataset from here:
https://www.kaggle.com/competitions/visual-taxonomy/data


---
**If you find a bug or want to enhance the model**, Happy coding! 🚀

