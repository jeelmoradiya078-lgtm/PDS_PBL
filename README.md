# Student Performance Analytics

## 📌 Project Overview

**Student Performance Analytics** is a Python-based data analytics and machine learning project that analyzes student marks and academic performance.

The project loads student data from a CSV file, cleans and processes the data, calculates student results, performs statistical analysis, creates visualizations, predicts Pass/Fail results using **Random Forest Classification**, and groups students according to their performance using **K-Means Clustering**.

---

## 🎯 Objectives

* Analyze student academic performance.
* Clean and preprocess student data.
* Calculate total marks, percentage, grade, and result.
* Perform statistical analysis on student marks.
* Visualize student performance using different graphs.
* Predict whether a student will **PASS or FAIL** using Random Forest.
* Group students into **Low, Average, and High Performance** using K-Means clustering.
* Save the final analyzed dataset as a CSV file.

---

## 🛠️ Technologies and Libraries Used

### Programming Language

* Python

### Libraries

* **Pandas** – Data loading, cleaning, processing, and analysis.
* **NumPy** – Numerical calculations and array operations.
* **Matplotlib** – Creating graphs and charts.
* **Seaborn** – Statistical data visualization.
* **SciPy** – Statistical calculations.
* **Scikit-learn** – Machine learning algorithms.
* **Google Colab** – Development environment.

---

## 📂 Project Structure

```text
Student-Performance-Analytics/
│
├── PDS_PBL.ipynb
├── Student.csv
├── final_student_analysis.csv
└── README.md
```

---

## 📊 Dataset

The project uses a student dataset containing information such as:

* Roll Number
* Student Name
* Branch
* Maths Marks
* Python Marks
* Data Science Marks
* Statistics Marks
* Computer Marks

The dataset is loaded using Pandas.

---

## 🔄 Project Workflow

```text
Student CSV File
       ↓
Import Libraries
       ↓
Load Dataset
       ↓
Data Inspection
       ↓
Data Preprocessing
       ↓
Calculate Total & Percentage
       ↓
Grade & Pass/Fail Result
       ↓
Statistical Analysis
       ↓
Data Visualization
       ↓
Random Forest Classification
       ↓
New Student Prediction
       ↓
K-Means Clustering
       ↓
Performance Groups
       ↓
Final Results
       ↓
Save Final CSV
```

---

## 🧹 Data Preprocessing

The project performs the following preprocessing operations:

* Converts subject marks into numeric values.
* Detects non-numeric values.
* Checks missing values.
* Fills missing marks using the median.
* Removes duplicate records.
* Cleans the Branch column.

---

## 📈 Performance Calculation

For every student, the project calculates:

### Total Marks

```text
Total = Maths + Python + Data Science + Statistics + Computer
```

### Percentage

```text
Percentage = Total Marks / Number of Subjects
```

### Grade

The project assigns grades according to the percentage:

| Percentage   | Grade |
| ------------ | ----- |
| 90 and above | A+    |
| 80–89        | A     |
| 70–79        | B     |
| 60–69        | C     |
| 50–59        | D     |
| 40–49        | E     |
| Below 40     | F     |

The result is:

* **PASS** → Percentage ≥ 40
* **FAIL** → Percentage < 40

---

## 📊 Data Visualization

The project uses Matplotlib and Seaborn to create different visualizations.

### 1. Student Performance Bar Chart

Displays the percentage of individual students.

### 2. Box Plot

Shows the distribution of marks for different subjects.

### 3. Correlation Heatmap

Shows the relationship between marks in different subjects.

### 4. Confusion Matrix

Displays the actual and predicted results of the Random Forest model.

### 5. Performance Clustering Graph

Displays students according to their performance groups.

---

## 🤖 Machine Learning – Random Forest

The project uses **Random Forest Classification** to predict whether a student will pass or fail.

### Input Features

The model uses marks from:

* Maths
* Python
* Data Science
* Statistics
* Computer

### Target

```text
Result
```

The result contains:

```text
PASS
FAIL
```

The dataset is divided into training and testing data using `train_test_split()`.

The Random Forest model is created using:

```python
RandomForestClassifier(
    n_estimators=100,
    random_state=42
)
```

The model then predicts the result of new students.

---

## 👨‍🎓 New Student Prediction

The user can enter:

* Roll Number
* Student Name
* Mobile Number
* Birth Date
* Email
* Marks in all five subjects

The program calculates:

* Total Marks
* Percentage
* Grade
* Predicted Result

Example:

```text
========== PERFORMANCE ==========

Total Marks: 418
Percentage: 83.6
Grade: A
Predicted Result: PASS
```

---

## 🔵 K-Means Clustering

K-Means is used as a **beyond-syllabus machine learning topic** in this project.

The project creates three clusters:

```text
Low Performance
Average Performance
High Performance
```

Before applying K-Means, the marks are standardized using `StandardScaler`.

The project uses:

```python
KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)
```

Students are then assigned to a performance group according to the average percentage of each cluster.

---

## 📉 Statistical Analysis

The project performs statistical analysis using NumPy, Pandas, and SciPy.

It calculates:

* Mean
* Median
* Mode
* Standard Deviation
* Highest Marks
* Lowest Marks
* Average Percentage

---

## 💾 Output

The final processed dataset is saved as:

```text
final_student_analysis.csv
```

The output contains calculated and analyzed information such as:

* Total
* Percentage
* Grade
* Result
* Cluster
* Performance Group

---

## ▶️ How to Run

### Option 1 – Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Upload the student CSV file to Google Drive.
3. Update the CSV file path if required.
4. Run the cells from top to bottom.
5. Enter new student details when prompted.
6. View the analysis, predictions, graphs, and clusters.

### Option 2 – Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

Then open:

```text
PDS_PBL.ipynb
```

---

## 📌 Project Features

* CSV dataset handling
* Data preprocessing
* Missing-value handling
* Duplicate removal
* Pandas data analysis
* NumPy calculations
* SciPy statistics
* Matplotlib visualization
* Seaborn visualization
* Random Forest Classification
* Student Pass/Fail prediction
* K-Means Clustering
* Performance grouping
* Final CSV generation

---



**Project:** Student Performance Analytics

**Subject:** Python for Data Science

**Semester:** 5

**Type:**PBL Project

👥 Contributors
1. Jeel Moradiya

## 📜 License

This project was developed for academic and educational purposes.
