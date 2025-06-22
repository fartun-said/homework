# ECON484 - Homework 2: Classification of Student Grades with k-NN

## 📌 Overview

This project explores the use of machine learning — specifically the **k-Nearest Neighbors (k-NN)** algorithm — to classify university students into grade categories based on their performance.

The aim is to treat the grading process as a **classification task**, using real course data (e.g., project scores, final exam results) and evaluating the accuracy and precision of machine-predicted labels compared to manually assigned categories.

---

## 🧠 Concept

Grading in a course can be seen as a classification problem:
- **Input features:** Homework, quizzes, midterm, project, final exam
- **Output class:** Final letter grade (or simplified category)

The simplified classification used in this project:
- `Outstanding`: Grade ≥ 85
- `Successful`: Grade between 55 and 84
- `Failing`: Grade < 55

---

## 🧪 Methodology

### 📊 Data
- Original dataset: 141 students
- Training set: 21 students (manually labeled)
- Test set: 120 students

### 🔧 Features Used
- `Project` score (out of 100)
- `Final Exam` score (out of 100)

These two features were selected because they carry the highest weight (40% and 25%) and had the least missing data.

### 🧮 Algorithm
- **Classifier:** k-NN (k = 3)
- **Distance Metric:** Euclidean distance

### 🧩 Confusion Matrix Evaluation
While trying to evaluate **True Positive**, **False Positive**, etc. in Google Colab, automatic labeling didn’t work as expected — Colab returned only `True` or `False`. Therefore, the final evaluation was done **manually in Excel**, which allowed for accurate confusion labeling and easier interpretation.

---

## 📁 Project Structure

```bash
📂 ECON484-HW2
├── HW2-Data-2.xlsx - Sheet1.csv   # Original dataset
├── hw2_knn_classifier.ipynb       # Google Colab notebook with k-NN implementation
├── HW2_with_Correct_Confusion_Labels.csv  # Final output with predictions + labels
└── README.md                      # Project documentation
