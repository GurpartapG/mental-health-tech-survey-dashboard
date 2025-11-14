# 🧠 Mental Health in Tech: Exploratory Data Analysis & Power BI Dashboard

## 📌 Project Overview
This project explores the mental health landscape in the tech industry using a real-world survey dataset. The analysis examines how demographic, workplace, and cultural factors influence:

- Access to mental health benefits  
- Willingness to seek treatment  
- Perceived severity of mental health concerns  
- Awareness of workplace resources  
- Regional differences in mental health support  

This project includes the full data analytics workflow — from cleaning to univariate, bivariate, multivariate analysis, statistical testing, and creation of a Power BI dashboard — culminating in actionable insights.

Mental health challenges are widespread in tech, yet awareness, benefits, and support vary dramatically across demographics and company types. This project uncovers those disparities using real survey data and transforms them into clear, data-driven insights and visual dashboards.

---

## 📁 Project Structure

```
mental_health_analysis/
│── cleaned_mental_health_data.csv ← (cleaned dataset used for analysis)
│── mental_health_analysis.ipynb ← (EDA & statistics notebook)
│── mental_health_in_tech_dashboard.pbix ← (Power BI dashboard)
│── README.md ← (this file)
└── images/ ← (visuals exported from the notebook)
```

---

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
- Consolidated countries into continent groups  
- Created new engineered features:
  - `age_group`
  - `country_grouped`
- Encoded categorical features (Label Encoding + One-Hot Encoding)

### **Resulting Clean Dataset**
- **1,259 records**
- **20+ cleaned and engineered features**

---

## 📊 Exploratory Data Analysis

### 🔹 **Univariate Analysis**
Explored frequency distributions of:
- Age & Age groups  
- Gender  
- Tech vs non-tech employment  
- Benefits, care options, wellness programs  
- Treatment-seeking behavior  

**Key Highlights**
- Largest age group: **25–34**  
- Tech workers form the majority  
- Many respondents **do NOT know** if care options exist  
- High percentage of “No” for mental health benefits  

---

### 🔹 **Bivariate Analysis**

#### **1. Remote Work vs Treatment**
- Minimal difference between remote and non-remote workers  
- Slightly higher help-seeking among remote employees  

#### **2. Gender vs Help-Seeking**
- Men significantly less likely to seek help  
- Women show higher “Yes” responses  
- “Other” genders — very small group but high help-seeking  

#### **3. Company Size Effects**
Larger companies (1000+ employees):
- More benefits  
- More care options  
- Greater awareness of resources  

Smaller companies (1–25 employees) lag behind.

#### **4. Tech vs Non-Tech**
- Tech companies provide more support programs  
- But high “Unknown” percentages → awareness barriers  

#### **5. Family History**
Strongest predictor of treatment behavior:
- Higher treatment rates  
- Higher awareness  
- Stronger belief in mental health severity  

#### **6. Age vs Treatment**
- Similar age distribution across groups  
- Young adults (18–24) least likely to seek help  
- Older adults (45+) more proactive  

---

## 🌍 Regional Insights (Continent Level)

### **Treatment Rates**
- **Higher:** Africa, Oceania  
- **Lower:** Asia, South America  
- **Mid-range:** Europe, North America  

### **Access to Resources**
- **Highest access:** North America, Oceania  
- **Lowest access:** Asia, Europe, South America  
- **Lowest awareness:** Africa & South America  
  - 100% report *not knowing how* to seek help  

---

## 📈 Correlation & Statistical Testing

### 🔥 **Correlation Heatmap — Key Relationships**
- Benefits ↔ Care Options (r ≈ 0.42)  
- Benefits ↔ Wellness Program (r ≈ 0.46)  
- Wellness Program ↔ Seek Help (r ≈ 0.53)  
- Family History ↔ Treatment (r ≈ 0.38)  

### 🧪 **Chi-Square Test Results**

| Variable Pair | Result |
|--------------|--------|
| tech_company × care_options | ❌ Not significant |
| family_history × treatment | ✅ Significant |
| benefits × mental_vs_physical | ✅ Significant |
| age_group × treatment | ❌ Not significant |

**Interpretation**
- Workplace initiatives alone do *not* determine treatment  
- Personal factors (family history, perceived severity) matter more  

---

## 📐 Cramer’s V (Categorical Associations)

### **Strongest Associations**
- wellness_program × seek_help → **0.53**  
- benefits × seek_help → **0.44**  
- benefits × care_options → **0.42**  

**Meaning:**  
Greater awareness/access → higher likelihood of seeking treatment.

---

## 👥 Additional Analysis — Younger vs Older Respondents

### **Younger Respondents**
- More uncertainty about benefits & care options  
- Help-seeking dominated by “No” & “Unknown”  
- Likely influenced by stigma, fear, lack of knowledge  

### **Older Respondents**
- Report higher availability of benefits  
- More willing to seek help  
- Perceive stronger workplace consequences  

---

## 🧾 Summary of Insights

### ✔ High-Level Findings
- Awareness gaps — not resource availability — are the main barrier  
- Younger adults struggle more with help-seeking  
- Family history is a major predictor of treatment behavior  
- Large companies provide more structured support  
- Tech companies offer more programs but have communication gaps  
- Strong global disparities in available resources and awareness  

---

## 📁 Dataset

This project uses the **OSMI Mental Health in Tech Survey** dataset.

- **Original raw dataset on Kaggle:**  
  👉 https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey  
- **Cleaned dataset used in this project:**  
  👉 `cleaned_mental_health_data.csv`

---

## ▶️ How to Run the Notebook

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
jupyter notebook mental_health_analysis.ipynb
```

## 📊 Power BI Dashboard (4 Pages)

This project includes a fully-interactive Power BI dashboard designed to make insights instantly visible for recruiters and decision-makers.

### **📄 Page 1 — Overview & Demographics**
**What it shows**
- Total survey responses  
- Mental health treatment by country  
- Gender distribution  
- Respondents by continent  
- Age group breakdown  

**Insights Revealed**
- Majority of respondents are male and from North America  
- Highest treatment rates appear in the U.S. and the U.K.  
- Age group 25–34 dominates the dataset  

---

### **📄 Page 2 — Workplace Culture & Mental Health**
**What it shows**
- Mental vs physical health importance  
- Work interference by company size  
- Benefits vs treatment seeking  
- Care options vs treatment  
- Employer encouragement vs treatment  

**Insights Revealed**
- Larger companies provide more mental health support  
- Work interference increases in medium-size companies  
- Benefits strongly correlate with seeking treatment  
- Many employees remain unaware of existing care options  

---

### **📄 Page 3 — Additional Insights**
**What it shows**
- Treatment by gender  
- Remote work vs treatment  
- Benefits in tech vs non-tech  
- Family history vs treatment  
- Encouragement to seek help by gender  

**Insights Revealed**
- Females more likely to seek treatment  
- Family history strongly increases likelihood of treatment  
- Tech companies offer more benefits but still have major awareness issues  

---

### **📄 Page 4 — Summary & Advanced Risk Score**
**What it shows**
- **% Seeking treatment**  
- **% Reporting work interference**  
- **% With mental health benefits**  
- **Average Mental Health Risk Score by Company Size**  

**Insights Revealed**
- About half of the industry seeks treatment  
- Work interference affects nearly 48% of employees  
- Smaller companies show higher risk scores and lower support resources  

---
## 🔍 Advanced Insight: RiskScore Feature

To add a model-like analytical layer, a custom **RiskScore** was engineered in Python.  
The score combines several key indicators:

- Work interference frequency  
- Access to benefits  
- Care options availability  
- Employer encouragement  
- Family history  
- Age group and company size  

Each factor was assigned a weighted score reflecting its influence on mental health strain.

### **How It Works**
- Higher interference → higher score  
- Missing or unknown benefits → higher score  
- Lack of awareness → higher score  
- Smaller companies automatically receive slightly higher baseline scores  

### **Why It’s Useful**
This metric acts like a “synthetic feature” similar to a prediction score, helping:
- Identify high-risk employee groups  
- Highlight where mental health programs are lacking  
- Provide actionable insight for HR or policy improvement

You visualize this score in the dashboard on Page 4.

---

## 🎓 Key Learnings

- Importance of cleaning messy real-world survey data  
- How demographic and workplace factors interplay in mental health  
- Significant gaps exist in awareness—not just availability—of mental health resources  
- Larger companies offer more structured support systems  
- Younger employees need targeted education and outreach  
- Statistical tools (Chi-Square, Cramer’s V) confirm which factors matter most  
- Dashboard design taught how to communicate insights visually and effectively  

---

## 🚀 Future Improvements

- Add predictive modeling (e.g., logistic regression) for treatment likelihood  
- Build a recommendation engine for mental health policy improvements  
- Incorporate sentiment analysis from open-ended survey questions  
- Add more years of data for trend analysis  
- Deploy dashboard online using Power BI Service  
- Create an interactive web app using Streamlit / Plotly  




