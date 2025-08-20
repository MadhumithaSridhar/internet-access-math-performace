
# 📊 Investigating the Impact of Internet Access on Student Math Performance

## 🧠 Introduction

### 🎓 Background

Education is a key driver of social mobility and economic growth. In the digital age, internet access plays a critical role in enhancing students' access to information and educational resources. This study explores whether having internet access at home significantly impacts students' performance in mathematics.

### ❓ Research Questions

1. Is there a significant difference in mean final math grades between students **with** and **without** internet access at home?
2. Is there a significant difference in the **proportion of high-achieving students** (those scoring > 15/20) between the two groups?

---

## 📁 Data Overview

* **Population**: Secondary school students studying mathematics
* **Sample**: Students from two Portuguese schools (Gabriel Pereira and Mousinho da Silveira)
* **Data Source**: Collected by Paulo Cortez and Alice Silva through school reports and questionnaires
* **Dataset**: [`student-mat.csv`](student-mat.csv)
* **Size**: 395 students

  * With internet: 329
  * Without internet: 66

---

## 📐 Methodology

### 🔢 Statistical Techniques Used

* **Difference in Means**: To assess the average grade difference
* **Difference in Proportions**: To compare the rates of high achievers

Both metrics are bootstrapped to generate **95% confidence intervals**, ensuring robustness of inference.

---

## 🔍 Data Preparation

Key steps included:

* Creating a new binary variable `high_achiever` (G3 > 15)
* Summarizing student counts by internet access
* Exploring final grade statistics (mean, median, std deviation)
* Generating visualizations for:

  * Internet access distribution
  * Grade distributions
  * High achiever proportions

---

## 📊 Exploratory Data Analysis Highlights

* **Internet Access**: 83.29% of students have access
* **Grade Distribution**:

  * Students with internet show broader, higher score distribution
  * Mean grade with internet: **10.6** vs **9.41** without
* **High Achievers**:

  * 12-13% with internet are high achievers
  * 3-4% without internet are high achievers

Visuals include bar charts and density plots to show distribution differences.

---

## 🔬 Inferential Analysis

### ✅ Difference in Mean Grades

* **Point Estimate**: Students with internet scored **1.21** points higher on average
* **95% CI**: \[**0.11**, **2.46**] — statistically significant

### ✅ Difference in High Achiever Proportions

* **Point Estimate**: Students with internet were **6.7%** more likely to be high achievers
* **95% CI**: \[**0.3%**, **12.5%**] — statistically significant

Bootstrap histograms with confidence intervals were plotted for both analyses.

---

## 📌 Conclusion

### 🔎 Summary of Findings

* Students **with internet access**:

  * Score significantly higher on average
  * Are significantly more likely to be high achievers

### ⚠️ Validity Considerations

* **Construct Validity**: Internet access is binary; quality or educational usage not captured
* **External Validity**: Only Portuguese students from 2008; findings may not generalize broadly
* **Internal Validity**: Observational data, potential confounding (e.g., socioeconomic status)

### 💡 Implications

While internet access is associated with better performance, causality cannot be concluded. Students with internet may also have better home environments, higher SES, etc.

---

## 📈 Future Research Suggestions

* Use nuanced measures of internet quality and educational use
* Include socioeconomic variables as controls
* Broaden to more schools and updated datasets
* Explore experimental or quasi-experimental designs

---

## 📚 References

Cortez, P. and Silva, A. M. Gonçalves. *Using data mining to predict secondary school student performance.* (2008).

---

## 🛠 Requirements

This project uses R. Main packages used:

* `tidyverse`
* `ggplot2`
* `infer`
* `dplyr`
* `readr`

Install all packages via:

```r
install.packages(c("tidyverse", "infer", "ggplot2", "dplyr", "readr"))
```

