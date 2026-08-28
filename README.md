# ANN Multiclass Classification

An Artificial Neural Network (ANN) project for **multiclass image classification** using a 10-class handwritten digit dataset. The model learns from pixel-level features and predicts the digit class from **0 to 9**.

## 📌 Project Overview

This project demonstrates an end-to-end deep learning workflow for multiclass classification:

**Image Dataset → Data Exploration → Duplicate Removal → Feature/Target Separation → ANN → Training → Evaluation → Visualization**

The dataset is represented in tabular form, where each image is described by its pixel values.

- **Task:** Multiclass Classification
- **Number of Classes:** 10
- **Classes:** `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`
- **Input:** 784 pixel features
- **Target:** `label`
- **Model:** Artificial Neural Network

## 📊 Dataset**
**LINK: https://www.kaggle.com/datasets/zalando-research/fashionmnist**
The notebook works with separate training and testing datasets.

### Original Dataset Size

| Dataset | Rows | Columns |
|---|---:|---:|
| Training | 60,000 | 785 |
| Testing | 10,000 | 785 |

Each row contains:

- `label` – the digit class
- `pixel1` through `pixel784` – pixel intensity values for a 28 × 28 image

Therefore, each image contains **784 input features**.

### Data Quality

The notebook reports:

- Training missing values: **0**
- Testing missing values: **0**
- Duplicate rows in training data: **43**
- Duplicate rows in testing data: **1**

After removing duplicates:

- Training dataset: **59,957 rows**
- Testing dataset: **9,999 rows**

The resulting feature and target shapes are:

- Training features: **59,957 × 784**
- Training target: **59,957**
- Testing features: **9,999 × 784**
- Testing target: **9,999**

## 🔢 Target Classes

The target variable contains **10 classes**:

```text
0  1  2  3  4  5  6  7  8  9
```

The class distribution in the cleaned training data is close to balanced, with approximately 6,000 examples per digit.

## 🧹 Data Preprocessing

The notebook performs the following preprocessing and exploration steps:

1. Load the training and testing datasets.
2. Inspect dataset shape and sample records.
3. Check column names and data types.
4. Check for missing values.
5. Identify duplicate rows.
6. Remove duplicate rows from both datasets.
7. Separate the `label` column from the pixel features.
8. Use the resulting 784 pixel values as ANN input features.

## 🧠 Artificial Neural Network

The project uses an Artificial Neural Network to learn the relationship between the 784 pixel inputs and the 10 possible digit classes.

For a multiclass classification problem, the network must produce a prediction for each of the ten digit classes. The class with the highest predicted probability can then be selected as the final digit prediction.

### Conceptual Architecture

```text
784 Pixel Features
       ↓
Input Layer
       ↓
Hidden Layers
       ↓
Output Layer
       ↓
10 Digit Classes (0–9)
```

The complete ANN implementation and configuration are available in the notebook included in this repository.

## 🎯 Multiclass Classification

Unlike binary classification, where the model chooses between two classes, this project has **10 possible output classes**.

For every input image, the model determines which digit from `0` to `9` is the most likely prediction.

## 📈 Evaluation

The notebook is designed to evaluate the trained ANN using classification performance and visual analysis.

Typical evaluation components include:

- Accuracy
- Predicted vs actual classes
- Confusion matrix
- Training/validation performance curves

A confusion matrix is particularly useful for this project because it shows which handwritten digits are correctly classified and which digits are confused with one another.

## 🖼️ Image Classification Concept

Each digit image is originally represented as a **28 × 28 pixel image**. The 2D image is stored as 784 numerical pixel values in the dataset.

The ANN receives these 784 values as input and learns patterns such as:

- Edges
- Strokes
- Curves
- Pixel arrangements
- Overall digit structure

The learned representation is then used to classify the image into one of the ten digit categories.

## 🛠️ Technologies Used

- **Python**
- **Pandas** – dataset loading and manipulation
- **NumPy** – numerical operations
- **Matplotlib** – data and training visualization
- **Scikit-learn** – machine-learning utilities and evaluation
- **TensorFlow / Keras** – Artificial Neural Network development
- **Jupyter Notebook** – experimentation and implementation

## 📁 Repository Structure

```text
ANN-Multiclass-Classification-/
│
├── ANN-Multiclass Classification .ipynb
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/mahi4221/ANN-Multiclass-Classification-.git
cd ANN-Multiclass-Classification-
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow jupyter
```

### 3. Open the notebook

```bash
jupyter notebook "ANN-Multiclass Classification .ipynb"
```

### 4. Run the notebook

Execute the cells sequentially to reproduce the data exploration, preprocessing, ANN training, and evaluation workflow.

## 🔄 Project Workflow

```text
Training & Testing Data
          ↓
Dataset Exploration
          ↓
Missing Value Check
          ↓
Duplicate Detection
          ↓
Remove Duplicate Rows
          ↓
Separate Features & Labels
          ↓
784 Pixel Features
          ↓
ANN Model
          ↓
Training
          ↓
Multiclass Prediction
          ↓
Model Evaluation
          ↓
Visualization
```

## 💡 Key Learning Outcomes

This project demonstrates practical understanding of:

- Multiclass classification
- Artificial Neural Networks
- Image data represented as tabular pixel features
- 28 × 28 image representation
- Feature and target separation
- Dataset quality checking
- Duplicate detection and removal
- Neural-network-based digit recognition
- Model training and validation
- Classification evaluation
- Confusion matrix interpretation
- Visualization of model performance

## ⚠️ Notes

The README documents the dataset characteristics and workflow supported by the notebook. The exact ANN hyperparameters and final evaluation values should be taken directly from the executed notebook rather than assumed from the dataset description.

## 👨‍💻 Author

**Maruthi Bonela**

B.Tech – Computer Science Engineering (AI & ML)

GitHub: https://github.com/mahi4221
