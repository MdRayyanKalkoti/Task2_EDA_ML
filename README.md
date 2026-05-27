<div align="center">

# 🧠 Task2\_EDA\_ML — Mental Health & Social Media Usage

### Exploratory Data Analysis | Python | Pandas | Seaborn | Matplotlib

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.26%2B-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8%2B-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.13%2B-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/)
[![VS Code](https://img.shields.io/badge/IDE-VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

**Internship Project · TechnoHacks Solutions · Task 2**

*Submitted by [Mohammad Rayyan Kalkoti](https://github.com/)*

</div>

---

## 📌 Project Overview

This project is part of my Machine Learning internship at **TechnoHacks Solutions**. The objective of **Task 2** is to perform a structured and reproducible **Exploratory Data Analysis (EDA)** on a real-world Mental Health and Social Media Usage dataset sourced from Kaggle.

The analysis investigates behavioral patterns, usage habits, and mental health indicators across survey respondents. The workflow covers data loading, cleaning, univariate and bivariate analysis, correlation study, and professional visualization — all documented within a single Jupyter Notebook for reproducibility.

> **Note:** This project is scoped to EDA and does not include predictive modeling or deployment.

---

## 🎯 Objectives

- Understand the structure and quality of the dataset through statistical inspection
- Identify patterns and distributions in key mental health and usage variables
- Analyze relationships between social media consumption, stress, sleep, and academic performance
- Produce clean, interpretable visualizations suitable for portfolio and presentation
- Follow a professional Git & GitHub workflow throughout the project

---

## 🗂 Project Structure

```
Task2_EDA_ML/
│
├── datasets/               # Raw dataset downloaded via Kaggle API
├── outputs/                # Summary tables, exported stats
├── graphs/                 # All saved visualization files (.png)
│
├── Task2_EDA.ipynb         # Main Jupyter Notebook (EDA workflow)
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
└── LICENSE                 # MIT License
```

---

## 📦 Dataset

| Attribute     | Details                                         |
|---------------|-------------------------------------------------|
| **Source**    | Kaggle — Mental Health and Social Media Usage   |
| **Format**    | CSV                                             |
| **Access**    | Downloaded using Kaggle API via VS Code terminal|
| **Domain**    | Mental Health, Behavioral Analysis, Social Media|

The dataset includes self-reported survey responses covering daily social media usage, sleep patterns, stress levels, academic performance, and platform-specific addiction metrics.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/Task2_EDA_ML.git
cd Task2_EDA_ML
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Download Dataset via Kaggle API

Ensure your Kaggle API credentials (`kaggle.json`) are placed in the appropriate directory:

```
~/.kaggle/kaggle.json           # macOS/Linux
C:\Users\<username>\.kaggle\    # Windows
```

Then run the following in your VS Code terminal:

```bash
kaggle datasets download -d <dataset-slug> -p datasets/ --unzip
```

> The Kaggle API was used throughout this project for direct, reproducible dataset access from the terminal — avoiding manual downloads and ensuring a clean workflow.

### 5. Launch the Notebook

```bash
jupyter notebook Task2_EDA.ipynb
```

---

## 🔬 EDA Workflow

The analysis follows a structured, step-by-step pipeline:

**Step 1 — Data Loading**
Dataset is loaded using `pandas.read_csv()`. Column names, data types, and shape are inspected to understand the overall structure.

**Step 2 — Data Inspection & Cleaning**
Missing value counts, data types, and descriptive statistics (`df.info()`, `df.describe()`) are reviewed. Null handling and type casting are performed where necessary to ensure analysis integrity.

**Step 3 — Univariate Analysis**
Individual distributions of key variables — stress level, addiction level, sleep hours, and social media usage duration — are examined using histograms and count plots.

**Step 4 — Bivariate & Comparative Analysis**
Relationships between variables (e.g., sleep hours vs. stress, usage time vs. academic performance) are explored using scatter plots and grouped bar charts to identify directional trends.

**Step 5 — Correlation Analysis**
A Pearson correlation heatmap is generated using Seaborn to quantify linear relationships between numerical features. This enables identification of multicollinearity and strong feature associations.

**Step 6 — Insight Extraction**
Key behavioral and mental health patterns are summarized based on observed distributions and relationships. These insights are documented inline in the notebook using Markdown cells.

**Step 7 — Graph Export**
All visualizations are saved as `.png` files to the `graphs/` directory using `matplotlib.pyplot.savefig()` with `dpi=150` for clear, shareable outputs.

---

## 📊 Visualizations

All graphs are saved in the `graphs/` folder. Below is a summary of each visualization produced:

| Visualization                    | Type            | Purpose                                                                 |
|----------------------------------|-----------------|-------------------------------------------------------------------------|
| Stress Level Distribution        | Histogram       | Shows the frequency distribution of reported stress levels              |
| Addiction Level Analysis         | Count Plot      | Displays categorical distribution of social media addiction scores      |
| Sleep Hours vs. Stress Level     | Scatter Plot    | Examines the relationship between sleep duration and reported stress    |
| Academic Performance Analysis    | Count / Bar Plot| Compares academic performance across different usage and stress groups  |
| Social Media Usage Distribution  | Histogram       | Visualizes daily usage time patterns across respondents                 |
| Correlation Heatmap              | Heatmap         | Displays pairwise Pearson correlations between all numerical variables  |

> Visualizations are styled using Seaborn's `whitegrid` theme with consistent color palettes for readability and consistency across the notebook.

---

## 💡 Key Insights

The following patterns were observed during the analysis:

- Respondents with higher daily social media usage tended to report elevated stress levels, though the relationship is not strictly linear.
- Sleep hours showed a moderate inverse association with stress scores — lower sleep correlated with higher reported stress in a notable portion of respondents.
- Addiction level scores were right-skewed, with the majority of respondents clustering at moderate levels rather than extreme values.
- The correlation heatmap revealed moderate positive correlations between usage time, addiction level, and stress — suggesting these variables move together but are not redundant.
- Academic performance appeared to decline in groups reporting both high stress and high social media usage, consistent with existing research on digital distraction.

> These are descriptive, data-driven observations drawn from the dataset — not causal claims.

---

## 🛠 Tech Stack

| Tool / Library    | Role in Project                                      |
|-------------------|------------------------------------------------------|
| **Python 3.10+**  | Core programming language                            |
| **Pandas**        | Data loading, inspection, cleaning, transformation   |
| **NumPy**         | Numerical operations and array handling              |
| **Matplotlib**    | Base plotting engine and figure export               |
| **Seaborn**       | Statistical visualizations and heatmap generation    |
| **Jupyter Notebook** | Interactive EDA and inline documentation          |
| **Kaggle API**    | Programmatic dataset download via CLI                |
| **VS Code**       | Primary development environment with terminal access |
| **Git & GitHub**  | Version control and project portfolio hosting        |

---

## 📁 Requirements

```
pandas>=2.0.0
numpy>=1.26.0
matplotlib>=3.8.0
seaborn>=0.13.0
jupyter>=1.0.0
kaggle>=1.6.0
```

Install all at once:

```bash
pip install -r requirements.txt
```

---

## 🚀 VS Code Workflow Note

The entire project was developed in **Visual Studio Code** using:

- The integrated terminal for Kaggle API dataset download and Git operations
- The Jupyter extension for interactive notebook execution
- Python virtual environment managed within the workspace

This setup allowed a seamless, terminal-driven workflow without switching between tools — reflecting a practical, professional development habit.

---

## 📜 License

This project is licensed under the **MIT License**.
See the [LICENSE](./LICENSE) file for full terms.

---

## 👤 Author

**Mohammad Rayyan Kalkoti**

Machine Learning Intern — TechnoHacks Solutions

[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=flat-square&logo=github)](https://github.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/)

---

<div align="center">

*Task 2 of the Machine Learning Internship Program at TechnoHacks Solutions*

*Focused on Exploratory Data Analysis · Python · Data Visualization*

</div>