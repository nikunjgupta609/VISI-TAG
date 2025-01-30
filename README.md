# VISI-TAG: Automated Product Attribute Prediction for E-Commerce

## Introduction
**VISI-TAG** is an AI-powered solution that enhances e-commerce product cataloging by automatically predicting product attributes (such as color, pattern, and sleeve length) directly from images. By leveraging deep learning and computer vision techniques, VISI-TAG ensures that product listings are more accurate and efficient, minimizing discrepancies between images and textual descriptions.

## Problem Statement
E-commerce platforms often struggle with inaccurate product descriptions. Sellers may input incorrect attributes, leading to customer dissatisfaction and return costs. This project aims to:
- Develop an ML model that predicts product attributes from images.
- Assist sellers in filling product details efficiently.
- Enhance the accuracy and reliability of online product catalogs.

## Technologies Used
VISI-TAG is built using a combination of modern AI frameworks and web technologies:

1. **Deep Learning & Image Processing**
   - PyTorch & Torchvision
   - ResNet18 (Pretrained CNN Model)
   - PIL & OpenCV for image processing
   - Tesseract OCR (optional for text extraction)

2. **Data Processing & Analysis**
   - Pandas & NumPy
   - scikit-learn for preprocessing & evaluation
   - NetworkX for graph-based analysis

3. **Web Development & API**
   - FastAPI for backend API
   - Next.js & TypeScript for frontend interface
   - PostgreSQL / MongoDB for storing product data

## Installation Guide
To set up VISI-TAG on your local system, follow these steps:

### 1. Clone the Repository
```sh
git clone https://github.com/your-username/VISI-TAG.git
cd VISI-TAG
```

### 2. Install Dependencies
#### **Backend Setup (Python)**
```sh
cd backend
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
pip install -r requirements.txt
```

#### **Frontend Setup (Next.js)**
```sh
cd frontend
npm install
```

### 3. Prepare Dataset
- Place training images in `train_images/`
- Place test images in `test_images/`
- Ensure `train.csv` and `test.csv` are in the root directory

### 4. Run the Backend Server
```sh
cd backend
uvicorn app:app --reload
```

### 5. Run the Frontend Application
```sh
cd frontend
npm run dev
```

## Directory Structure
```
VISI-TAG/
│── backend/                # Backend API service
│   ├── models.py           # Model definition (ResNet-based classifier)
│   ├── preprocess.py       # Image preprocessing utilities
│   ├── train.py            # Training pipeline
│   ├── inference.py        # Model inference
│   ├── routes/             # API routes
│   ├── requirements.txt    # Python dependencies
│
│── frontend/               # Frontend UI (Next.js)
│   ├── pages/              # Main UI pages
│   ├── components/         # UI components
│   ├── styles/             # CSS styles
│   ├── public/             # Static assets
│   ├── package.json        # Frontend dependencies
│
│── dataset/                # Data files
│   ├── train.csv           # Training labels
│   ├── test.csv            # Test data
│   ├── category_attributes.parquet # Attribute mapping
│
│── images/                 # Image dataset
│   ├── train_images/       # Training images
│   ├── test_images/        # Test images
│
│── README.md               # Project documentation
└── .gitignore              # Git ignore file
```

## Evaluation Metrics
Submissions are evaluated based on:
- **Harmonic Mean of Macro & Micro F1-Score** for each attribute
- Averaging F1-scores across categories and attributes
- A strict validation system that prevents null values

## Expected Submission Format
Predictions should be submitted in the following format:
```
id, Category, len, attr_1, attr_2, ..., attr_10
1, Sarees, 10, 'same as border', 'woven design', 'big border', ..., 'no'
2, Men Tshirts, 5, 'black', 'round', 'printed', ..., 'dummy_value'
```
Ensure to fill missing attributes with **dummy_value** to avoid errors.

## Resources
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Next.js Documentation](https://nextjs.org/docs)
- [Meesho Challenge Details](https://meesho.com/data-challenge)
- [Image Classification Techniques](https://arxiv.org/abs/1512.03385)

## Future Improvements
- **Expand Model**: Support more product categories beyond fashion.
- **Integrate NLP**: Combine text and image data for improved accuracy.
- **Cloud Deployment**: Deploy on AWS/GCP for scalability.

---
**Contributions & Issues:** If you find a bug or want to enhance the model, feel free to contribute via pull requests. 🚀

