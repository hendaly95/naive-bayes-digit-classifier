# 🔢 Naive Bayes Classifier for Digit Recognition

This project implements a Gaussian Naive Bayes classifier from scratch to distinguish between handwritten digits **0** and **1** using simple statistical features. It uses a subset of the MNIST dataset and demonstrates a complete classification pipeline, including data preprocessing, feature extraction, parameter estimation, classification, and performance evaluation.

## 📌 Project Overview

- Focus: Binary image classification (digits 0 vs. 1)
- Features: Mean and standard deviation of pixel brightness
- Model: Gaussian Naive Bayes
- Output: Accuracy evaluation on test sets

## 🗂️ File Descriptions

| File                 | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `Project1.ipynb`     | Main notebook for feature extraction, training, prediction, and evaluation |
| `geneNewData.py`     | Script for generating student-specific datasets from MNIST digit images     |
| `Project Report.pdf` | Project summary, methodology, accuracy results                              |

## 📁 Dataset

This project uses a curated subset of the **MNIST** dataset focused on digits **0** and **1**.  
⚠️ The raw `.mat` data files are not included due to size and licensing. You may generate them using `geneNewData.py`.

Expected `.mat` files (inside a `data/` directory):

- `train_0_img.mat` – training images of digit 0  
- `train_1_img.mat` – training images of digit 1  
- `test_0_img.mat` – testing images of digit 0  
- `test_1_img.mat` – testing images of digit 1  

These are used to create your student-specific train/test sets.

## 🚀 Features

- Manual Gaussian distribution modeling using extracted brightness statistics
- Feature set:
  - Mean pixel brightness
  - Standard deviation of pixel brightness
- Class-wise parameter estimation (mean, variance)
- Prediction using log-likelihood and Gaussian PDF
- Evaluation using classification accuracy

## 🛠️ How to Run

### **Step 1: Generate Training & Testing Data**

```bash
python geneNewData.py
```

This will generate:
- `digit0_stu_train<ID>.mat`
- `digit1_stu_train<ID>.mat`
- `digit0_testset.mat`
- `digit1_testset.mat`

Be sure to replace `<ID>` with your student identifier when editing the script.

### **Step 2: Train & Evaluate the Classifier**

Run the notebook:

```bash
jupyter notebook Project1.ipynb
```

This will:
- Load and preprocess the data
- Extract features
- Train a Naive Bayes classifier
- Print final classification accuracy on both digit 0 and 1 test sets

## 📊 Sample Output

```
Accuracy for digit 0 test set: 91.73%
Accuracy for digit 1 test set: 92.33%
```

These results confirm the classifier's ability to distinguish digits using only basic statistical features.

## 📄 Summary

The project demonstrates the power of Naive Bayes classification using Gaussian assumptions and minimal features. With proper preprocessing and feature engineering, even simple models can achieve strong performance in structured tasks such as digit recognition.
