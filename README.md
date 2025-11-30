# 🍽️ Feeding Analysis — Python Data Insights Project

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Python](https://img.shields.io/badge/Python-3.10-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-red)
![Data Science](https://img.shields.io/badge/Field-Data%20Science-purple)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Enabled-brightgreen)

---

## 📌 Project Overview

This project analyzes turnout for a **non-profit community feeding program**, where volunteers serve meals and track:

- expected turnout (plan/forecast)
- actual turnout (real number of attendees)
- temperature
- holidays (Thanksgiving, Christmas)
- seasonal effects (Spring, Summer, Fall, Winter)

Using **Python, pandas, and matplotlib**, the analysis explores:

- How far actual turnout deviates from expected turnout  
- Whether weather affects attendance  
- Seasonal differences in attendance  
- Turnout on major holidays  
- How attendance grows year over year  

This notebook demonstrates **real-world data analytics skills**:
data cleaning → feature engineering → exploratory analysis → insights → charts → portfolio visuals.

---

## 🎯 Business Context

Organizations that run feeding programs face real challenges:

- How many people should we expect tomorrow?
- Do holidays increase or decrease turnout?
- Does cold weather reduce attendance?
- Are we trending upward or downward compared to previous years?

This analysis helps solve these questions:

- Provides **forecasting signals** using expected vs actual  
- Shows **seasonal & holiday patterns**  
- Identifies **weather sensitivity**  
- Helps program directors make better resource decisions  

---

## 🛠️ Tech Stack

- **Language:** Python 3  
- **Notebook:** Jupyter  
- **Libraries:**  
  - pandas (data cleaning & transformation)  
  - matplotlib (visualization)  
  - numpy (supporting calculations)  
- **Data source:** CSV file (`data/feedings_analysis.csv`)  
- **Exports:** PNG charts saved to `/visuals`  

---

## 📁 Folder Structure

```
Feeding_Analysis/
│
├── data/
│   └── feedings_analysis.csv
│
├── visuals/
│   ├── expected_vs_actual_turnout.png
│   ├── average_turnout_by_season.png
│   ├── temperature_vs_turnout_by_season.png
│   ├── major_holidays_vs_normal_days.png
│   └── yearly_average_turnout_growth.png
│
├── feeding_analysis.ipynb
└── README.md
```

---

## 📊 Dataset Description

The dataset contains real-world style fields collected during community feeding events.

**Columns include:**

| Column | Description |
|--------|-------------|
| `date` | Date of the meal event |
| `food` | Food served that day |
| `allergens` | Allergen category of the food |
| `expected_turnout` | Forecasted turnout based on planning |
| `actual_turnout` | Actual number of attendees |
| `city` | City where the feeding occurred |
| `holiday` | Marks Thanksgiving/Christmas events |
| `season` | Automatically derived from `date` |
| `temp` | Temperature (°F) on the day of the event |

---

## 🧪 Step-by-Step Analysis

This project follows a clean, professional analytics workflow:

### **1️⃣ Import & Load Data**
- Imported pandas & matplotlib  
- Loaded CSV into a pandas DataFrame  
- Inspected structure with `.head()`, `.info()`, `.describe()`

### **2️⃣ Clean & Prepare**
- Converted date strings → datetime objects  
- Created new features:
  - `season` (Winter/Spring/Summer/Fall)
  - `is_major_holiday` (Yes/No)
- Handled missing values  
- Ensured all numeric fields were correct types  

### **3️⃣ Explore Relationships**
Using charts + summary tables, we analyzed:

- 🟦 Expected vs. Actual turnout  
- 🌡 Temperature vs. turnout  
- 🍂 Seasonal attendance  
- 🎄 Holiday impact  
- 📈 Year-over-year growth  

---

## 🧱 Feature Engineering

Several engineered features strengthened the analysis:

### 🔹 **Season Extraction**
Seasons derived from the event date.

### 🔹 **Major Holiday Flag**
Binary indicator for:
- Thanksgiving  
- Christmas  

### 🔹 **Temperature Buckets (optional)**
Possible future: Cold / Mild / Hot buckets.

### 🔹 **Year Field**
For growth analyses.

These help the model & visuals reveal patterns that raw data can’t.

---

## 📉 Visualizations

All final charts are saved to `/visuals/`.

### **📌 1. Expected vs Actual Turnout Over Time**

Shows whether actual turnout keeps up with (or exceeds) planning.

**Filename:**  
`expected_vs_actual_turnout.png`

![Expected vs Actual Turnout](https://raw.githubusercontent.com/kayla-melton/feeding-analysis-python/main/visuals/expected_vs_actual_turnout.png)

---

### **📌 2. Average Turnout by Season**

Compares attendance across Spring, Summer, Fall, Winter.

**Filename:**  
`average_turnout_by_season.png`

![Average Turnout by Season](https://raw.githubusercontent.com/kayla-melton/feeding-analysis-python/main/visuals/average_turnout_by_season.png)

---

### **📌 3. Temperature vs Turnout (Colored by Season)**

Visualizes weather sensitivity.

**Filename:**  
`temperature_vs_actual_turnout_by_season.png`

![Temperature vs Actual Turnout by Season](https://raw.githubusercontent.com/kayla-melton/feeding-analysis-python/main/visuals/temperature_vs_actual_turnout_by_season.png)

---

### **📌 4. Major Holiday vs Non-Holiday Attendance**

Shows whether big holidays boost turnout.

**Filename:**  
`major_holidays_vs_normal_days.png`

![Major Holidays vs Normal Days](https://raw.githubusercontent.com/kayla-melton/feeding-analysis-python/main/visuals/major_holidays_vs_normal_days.png)

---

### **📌 5. Yearly Average Turnout Growth**

Tracks year-over-year improvement.

**Filename:**  
`yearly_average_turnout_growth.png`

![Yearly Average Turnout Growth](https://raw.githubusercontent.com/kayla-melton/feeding-analysis-python/main/visuals/yearly_average_turnout_growth.png)

---

## 🔍 Key Insights & Findings

### ⭐ 1. **Actual turnout consistently tracks expected turnout**
- Strong alignment = stable forecasting  
- Occasional spikes indicate special events or weather shifts  

### ⭐ 2. **Summer shows the highest turnout**
- Likely due to better weather conditions  
- Winter is the lowest due to cold temperatures  

### ⭐ 3. **Temperature strongly impacts attendance**
- Cold days → lower attendance  
- Warm days → higher turnout  
- Scatterplot shows clear seasonal grouping  

### ⭐ 4. **Major holidays boost turnout**
- Thanksgiving and Christmas have the largest turnout  
- Suggests higher community participation or higher need  

### ⭐ 5. **Year-over-year turnout is rising**
- Indicates program growth  
- Useful for budgeting & forecasting  

---

## 🧠 How to Run This Project

Follow these steps to run the notebook and generate all visuals:

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd Feeding_Analysis
```

### **2️⃣ Install Dependencies**
Make sure you have Python 3 and pip installed.

Then install the required libraries:
```bash
pip install pandas matplotlib
```

### **3️⃣ Open the Notebook**
```bash
jupyter notebook feeding_analysis.ipynb
```

### **4️⃣ Generate Visuals**
Run **all cells** to:

- Load the data  
- Prepare features  
- Create charts  
- Automatically save PNGs into the `/visuals` folder  

Your charts will appear in:

```
/visuals/
    expected_vs_actual_turnout.png
    avg_turnout_by_season.png
    temp_vs_turnout_by_season.png
    holiday_vs_normal.png
    yearly_growth.png
```

---

## 🤖 Predictive Modeling

In addition to exploratory analysis, this project includes a simple predictive model designed to estimate **actual feeding turnout** based on several engineered features.

### 🎯 Goal
Predict the number of attendees using:

- expected_turnout  
- season  
- temperature  
- holiday indicators  
- year  

This represents a real-world scenario where program coordinators need to forecast attendance for staffing, budgeting, and food preparation.

---

### 🧠 Modeling Approach

A regression model was built using:
- **Train/Test Split**
- **Feature Encoding** (for season & holidays)
- **Normalization/Scaling** (if applicable)
- **Linear Regression** (baseline)
  - Easy to interpret  
  - Good for understanding feature influence

---

### 📈 Model Performance

The model outputs:

- **Predicted turnout values**
- **Residuals** (actual – predicted)
- **R² score** to measure how well features explain turnout

While this is a simple baseline model, it demonstrates:

- How structured features can predict attendance  
- How seasonality, holidays, and weather affect turnout  
- How forecasting can support decision-making  

---

### 🔍 Key Modeling Insights

- Expected turnout is the strongest predictor, as anticipated.  
- Temperature and season both significantly impact turnout — warmer seasons predict higher attendance.  
- Major holidays increase predicted turnout compared to similar non-holiday days.  
- The model performs well for general prediction but could be improved with:
  - More data  
  - Additional weather features  
  - Nonlinear algorithms  

---

### 🧪 Example Output (from notebook)

The notebook includes:
- A prediction column (`predicted_turnout`)
- A residual analysis chart  
- A comparison plot of **actual vs. predicted turnout**  

These help validate model accuracy and show where the model under/over-predicts.

---

## 🧠 Skills Demonstrated

This project highlights a full range of Data Analyst and Data Scientist skills, including:

### **📊 Data Cleaning & Preparation**
- Handling missing values  
- Converting data types (e.g., dates)  
- Renaming columns & standardizing formats  
- Creating new calculated fields (feature engineering)

### **🧮 Exploratory Data Analysis (EDA)**
- Descriptive statistics  
- Grouping and aggregating with pandas  
- Identifying trends, seasonality, and anomalies  
- Comparing expected vs actual behavior  

### **📈 Data Visualization**
- Time-series line charts  
- Scatter plots with grouped categories  
- Seasonal comparisons  
- Residual plots  
- Model evaluation visuals  
- Saving professional charts programmatically  

### **🔧 Feature Engineering**
- Extracting year & season  
- Holiday classification (Thanksgiving, Christmas)  
- Weather-based variables  
- Preparing inputs for predictive modeling  

### **🤖 Predictive Modeling**
- Train/test split  
- Linear regression (baseline model)  
- Generating prediction outputs  
- Evaluating model accuracy (R², residuals)  
- Visualizing model performance  
- Interpreting feature impact  

### **📂 Project Structure & GitHub Workflow**
- Organizing a multi-folder Python project  
- Using relative paths for portability  
- Exporting visuals for GitHub  
- Writing a professional README  
- Version control with Git  

### **💡 Business Insight & Storytelling**
- Translating data findings into real-world implications  
- Highlighting factors that influence turnout  
- Communicating insights clearly and professionally  

---

This section demonstrates that the project isn’t just code —  
it showcases **real data analytics ability**, clearly and confidently.

---

## 📬 Contact

If you'd like to discuss this project or collaborate:

**Kayla Melton**  
📧 Email: kaylamelton22@icloud.com    
💼 LinkedIn: https://www.linkedin.com/in/jakayla-melton-001a782bb/  
🗂️ GitHub: https://github.com/kayla-melton  

---

## ⭐ If you found this project helpful…
Please consider giving the repo a **star**! ⭐

