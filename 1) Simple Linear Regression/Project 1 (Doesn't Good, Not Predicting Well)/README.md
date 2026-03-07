# 🎓 Student Performance Analysis

📌 **Project Overview**  
This project performs **exploratory data analysis (EDA)** and **simple linear regression** on student performance data to understand how **study behavior influences final exam scores**.

The project is intentionally designed as a **learning-focused machine learning workflow**, emphasizing **data cleaning, assumption checking, and honest model evaluation** rather than maximizing prediction accuracy.

---

🎯 **Objectives**
- Understand the relationship between **study time and final grades**
- Practice **real-world data cleaning and preprocessing**
- Perform **linearity, correlation, and outlier analysis**
- Implement **Simple Linear Regression** correctly
- Learn why **a single feature is insufficient** to predict academic performance accurately

---

📊 **Dataset**
- **Source**: UCI Machine Learning Repository – Student Performance Dataset
- **Target Variable**: `G3` (Final Grade: 0–20)

🛠 **Tools & Technologies**
- Python
- Pandas
- NumPy
- Matplotlib
- scikit-learn

### Key Features Used
- `studytime` → converted to **approximate weekly study hours**
- Other features were analyzed but excluded to avoid **target leakage** and to keep the model simple for learning purposes.

📌 *Note*:  
Earlier grades (`G1`, `G2`) were deliberately removed to prevent data leakage and ensure a fair learning experiment.

---

🧹 **Data Cleaning & Preprocessing**
- Removed target leakage columns (`G1`, `G2`)
- Removed invalid records (`G3 = 0`)
- Validated data ranges and integrity
- Converted ordinal study time into numeric study hours
- Checked for missing values (none found)

---

🔍 **Exploratory Data Analysis (EDA)**
- Correlation analysis between study time and final grade
- Linearity check using scatter plots
- Outlier detection using boxplots
- Residual pattern inspection

📌 Feature scaling was **not applied**, as it is unnecessary for single-feature linear regression.

---

🤖 **Modeling Approach**
- **Algorithm**: Simple Linear Regression
- **Train–Test Split**: 80% training, 20% testing
- **Independent Variable**: Study time (hours)
- **Dependent Variable**: Final grade (`G3`)

This setup helps demonstrate how linear regression works under **realistic constraints**.

---

📈 **Model Evaluation**
| Metric | Value |
|------|------|
| MAE | ~2.56 |
| RMSE | ~3.09 |
| R² Score | ~0.01 |

### Interpretation
- The model predicts final marks with an average error of ~2.5 marks.
- **Study time alone explains less than 1% of grade variation**.
- This confirms that **academic performance depends on multiple factors**, not just study hours.

📌 The low R² score is **expected and acceptable** for this learning-focused project.

---

🔍 **Key Insights**
- A single feature is **not sufficient** to accurately predict student performance
- Low R² does **not indicate a faulty ML pipeline**
- Real-world educational data is noisy and influenced by many hidden variables
- Proper ML workflow is more important than high accuracy in learning projects

---

## 📁 Project Structure
📦 **student-performance-analysis**  
 ┣ 📂 data  
 ┣ 📂 notebooks  
 ┣ 📄 README.md  
 ┗ 📄 requirements.txt  

---

✅ **Conclusion**
This project demonstrates a **complete and correct machine learning workflow** using a real dataset.  
It highlights the **limitations of simple linear regression** and reinforces the importance of **feature selection, data understanding, and honest evaluation**.

📌 This project is intended **purely for learning and academic practice**, serving as a foundation for more advanced models such as **Multiple Linear Regression**.
