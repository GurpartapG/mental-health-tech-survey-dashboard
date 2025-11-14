# 🧠 Mental Health in Tech: Exploratory Data Analysis & Power BI Dashboard

## 📌 Project Overview

This project explores the **mental health landscape in the tech industry** using a real-world survey dataset. The analysis examines how demographic, workplace, and cultural factors influence:

- Access to mental health benefits  
- Willingness to seek treatment  
- Perceived severity of mental health concerns  
- Awareness of workplace resources  
- Regional differences in mental health support  

This project includes the full data analytics workflow—from **cleaning** to **univariate**, **bivariate**, **multivariate**, **statistical testing**, and creation of a **Power BI dashboard**—culminating in actionable insights.

---

## 📁 Project Structure
```
mental_health_analysis/
├── cleaned_mental_health_data.csv
├── mental_health_analysis.ipynb
├── README.md   ← (this file)
└── images/     ← (plots exported from notebook)
```

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy)
- Visualization: Matplotlib, Seaborn
- Statistics: SciPy, Cramer’s V
- Encoding & Preprocessing: Scikit-learn
- Power BI
- Environment: Google Colab / Jupyter Notebook

---

## 🧹 Data Understanding & Cleaning

### **Key Cleaning Steps**

- Removed duplicates and irrelevant columns  
- Standardized categorical responses (gender, benefits, treatment, wellness program, etc.)  
- Handled missing values and grouped small categories  
- Consolidated countries into **continent groups**  
- Created new features:  
  - `age_group`  
  - `country_grouped`  
- Encoded categorical features (Label Encoding + One-Hot Encoding)

### **Resulting Clean Dataset**

- **1,259 records**
- **20+ cleaned and engineered features**

---

# 📊 Exploratory Data Analysis

## 🔹 Univariate Analysis

Explored frequency distributions of:

- Age  
- Age groups  
- Gender  
- Tech vs non-tech employment  
- Benefits, care options, wellness programs  
- Treatment-seeking behavior  

### **Key Highlights**

- Largest age group: **25–34**  
- Tech workers form the majority of respondents  
- Most respondents **do NOT know** whether care options exist  
- High percentage of **“No”** in mental health benefits  

---

## 🔹 Bivariate Analysis

### **1. Remote Work vs Treatment**
- Minimal difference between remote and non-remote employees  
- Slightly higher treatment among remote workers  

### **2. Gender vs Help-Seeking**
- Men are **significantly less likely** to seek help  
- Females show higher “Yes” responses  
- Other genders (low sample) show higher help-seeking tendency  

### **3. Company Size Effects**
Larger companies (1000+ employees):

- Greater access to benefits  
- More care options  
- Higher awareness of mental health resources  

Small companies (1–25 employees) lag behind across all metrics.

### **4. Tech vs Non-Tech**
- Tech companies report **higher benefits and care options**  
- But have a **large “Unknown” population**, indicating communication gaps  

### **5. Family History**
Strongest predictor of treatment-seeking:

- Higher treatment rates  
- Higher awareness  
- Stronger belief in mental health severity  

### **6. Age vs Treatment**
- Treatment-seekers and non-seekers have similar age spread  
- Younger adults (**18–24**) are **least likely** to seek help  
- Older adults (**45–54**, **55+**) are more proactive  

---

# 🌍 Regional Insights (Continent Level)

### **Treatment Rates**
- **Higher:** Africa, Oceania  
- **Lower:** Asia, South America  
- **Mid-range:** Europe, North America  

### **Access to Resources**
- **Highest access:** North America, Oceania  
- **Lowest access:** Asia, Europe, South America  
- **Lowest awareness:** Africa & South America  
  - 100% report **not knowing how** to seek help  

---

# 📈 Correlation & Statistical Testing

## 🔥 Correlation Heatmap — Key Relationships

- **Benefits ↔ Care Options** (r ≈ 0.42)  
- **Benefits ↔ Wellness Program** (r ≈ 0.46)  
- **Wellness Program ↔ Seek Help** (r ≈ 0.53)  
- **Family History ↔ Treatment** (r ≈ 0.38)  
- Age groups show expected mutual exclusivity (one-hot encoding)  

---

## 🧪 Chi-Square Test Results

| Variable Pair                 | Result |
|------------------------------|--------|
| tech_company × care_options  | ❌ Not significant |
| family_history × treatment   | ✅ Significant |
| benefits × mental_vs_physical | ✅ Significant |
| age_group × treatment        | ❌ Not significant |

### **Interpretation**

- Workplace initiatives alone do **not** determine treatment  
- Personal background (**family history**) and **perceived severity** matter more  

---

## 📊 Cramer’s V — Association Strength (Categorical)

### **Strongest Associations**
- **wellness_program × seek_help** → 0.53  
- **benefits × seek_help** → 0.44  
- **benefits × care_options** → 0.42  

**Meaning:**  
> Greater access/awareness of programs → higher likelihood of seeking treatment.

---

# 🧐 Additional Analysis — Younger vs Older Respondents

### **Younger Respondents**
- More uncertain about benefits & care options  
- Help-seeking dominated by **“No”** and **“Unknown”**  
- Likely influenced by stigma, lack of awareness, or fear  

### **Older Respondents**
- Report higher availability of benefits  
- Greater openness to seeking help  
- Report higher perceived workplace consequences  

---

# 🔍 Summary of Insights

### ✔ High-Level Findings

- **Awareness gaps**, not lack of resources, are the main barrier  
- **Younger adults** struggle more with help-seeking  
- **Family history** significantly drives treatment behavior  
- **Large companies** provide more support  
- **Tech companies** offer more programs but face communication issues  
- Major **regional disparities** exist globally  

---

# 📁 Dataset

A cleaned version of the dataset is included:
cleaned_mental_health_data.csv

---

# 🧪 How to Run the Notebook

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
jupyter notebook mental_health_analysis.ipynb
```





## 📊 Dashboard Features

**🧠 Page 1 – Global Overview**
- Total responses, gender and age breakdown
- Respondents by continent
- Mental health treatment by country

**🌍 Page 2 – Work & Support Systems**
- Mental vs. physical health by age group
- Work interference vs. company size
- Treatment vs. care options, benefits, and employer encouragement

**🔍 Page 3 – Deep Dive Insights** *(Work in Progress)*
- Treatment seeking behavior by gender
- Remote work and treatment correlation
- Tech vs. non-tech employer benefits
- Family history vs. treatment
- Encouragement to seek help by gender



## ✨ Key Learnings

- Practiced transforming raw survey data into a structured, analytical format
- Developed visual storytelling using slicers, drill-downs, and multi-page dashboards
- Explored intersections between gender, work environment, and mental health treatment



