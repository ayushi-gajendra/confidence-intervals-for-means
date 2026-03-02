# 🛌 Human Sleep Patterns & Stress: Inferential Analysis (Part 1)

## 📌 Project Overview

This project focuses on the application of **Inferential Statistics** to evaluate personal health data. By analyzing sleep variables collected from a wearable fitness tracker over a 6-month period, this study aims to determine if the subject is experiencing physiological signs of stress—specifically through the lens of **REM Sleep** percentages.

The analysis utilizes **Point Estimates** and **Confidence Intervals (CI)** to move beyond simple averages and account for sampling uncertainty.

---

## 📉 The Business Problem

Stress is a significant disruptor of sleep architecture. While "Normal" REM sleep typically accounts for **20–25%** of total sleep time, significant stress can suppress this to **15–20%**.

The objective is to analyze the user's recorded sleep data to answer the following:

* What is the true population mean ($\mu$) of the user’s REM sleep?
* Based on a 95% and 90% Confidence Interval, can we statistically suggest that the user is suffering from stress-related sleep deficiency?

---

## 🛠️ Data Features

The dataset contains daily observations with the following features:

* **DATE**: The evening of the recording.
* **SLEEP SCORE**: An aggregate quality metric (Fitbit).
* **HOURS OF SLEEP**: Total duration of sleep.
* **REM SLEEP**: Percentage of sleep spent in the Rapid Eye Movement stage (**Target Variable**).
* **DEEP SLEEP**: Percentage of sleep spent in the Deep sleep stage.
* **HEART RATE BELOW RESTING**: Percentage of time HR remained below the resting baseline.
* **SLEEP TIME**: Timestamps for sleep start and wake.

---

## 🧪 Methodology & Approach

### 1. Data Summarization

We first calculated the descriptive statistics for the REM Sleep column to establish our point estimates.

* **Sample Mean ($\bar{x}$):** The average REM percentage.
* **Sample Standard Deviation ($s$):** The spread of the REM data.
* **Sample Size ($n$):** Total number of days recorded.

### 2. Statistical Formulas Used

To determine the range in which the true mean likely falls, we calculated the **Margin of Error (MOE)** and the **Confidence Intervals** using the following formulas:

* **Standard Error ($SE$):** 
$$SE = \frac{s}{\sqrt{n}}$$


* **Margin of Error ($E$):** 
$$E = z \cdot \left(\frac{s}{\sqrt{n}}\right)$$


* **Confidence Interval:** 
$$CI = \bar{x} \pm E$$



### 3. Comparison of Confidence Levels

We performed the analysis at two distinct levels—**95%** and **90%**—to observe how the "width" of our certainty changes the resulting interval.

---

## 📊 Results & Calculations

Based on the dataset of **179 observations**, the following values were obtained:

| Metric | Value |
| --- | --- |
| **Sample Mean ($\bar{x}$)** | 19.39% |
| **Standard Deviation ($s$)** | 3.915 |
| **Sample Size ($n$)** | 179 |

### Confidence Interval Comparison

| Confidence Level | z-score | Margin of Error | Lower Bound | Upper Bound | Interval Width |
| --- | --- | --- | --- | --- | --- |
| **95%** | 1.96 | 0.5736 | **18.82%** | **19.96%** | 1.1472 |
| **90%** | 1.645 | 0.4814 | **18.91%** | **19.87%** | 0.9628 |

---

## 🧠 Insights & Conclusions

### 1. Interval Comparison

* **Narrower Interval:** The **90% Confidence Interval** is narrower (0.96) compared to the 95% interval (1.15). This is because a lower confidence level requires less "surface area" under the normal curve, resulting in a smaller margin of error.
* **Common Center:** Both intervals are centered exactly at the sample mean of **19.39%**. The mean is our "best guess" (point estimate), while the intervals represent our uncertainty around that guess.

### 2. Clinical Significance

* The "Healthy" threshold for REM sleep starts at **20%**.
* Our analysis shows that even at the **Upper Bound** of a 95% confidence interval (19.96%), the value remains below the 20% threshold.

### 3. Recommendations

* **Hypothesis Testing:** While the intervals suggest a deficiency, a formal **One-Sample T-Test** should be conducted to statistically confirm if the mean is significantly lower than the 20% benchmark.
* **Lifestyle Correlation:** It is recommended to cross-reference these "Low REM" days with the "Heart Rate Below Resting" metric. If HR stays high during sleep, it further validates the presence of physiological stress.
* **Actionable Step:** Given that the 95% CI is entirely below 20%, the user should consider stress-reduction techniques (e.g., meditation, earlier wind-down times) to improve sleep architecture.

---

## 🎓 Project Credits
This analysis was developed as part of the **Applied Statistics for Data Analytics** course by **DeepLearning.AI** on Coursera. It focuses on using discrete distributions to solve predictive problems in media and entertainment.

---

## 👤 About the Author
**Ayushi Gajendra** 

*Data Analyst | Former EdTech Co-Founder*

* **7+ Years** of experience in business operations, strategic growth, and entrepreneurial leadership.
* I specialize in bridging the gap between raw data and **high-stakes business decisions**.
* My goal is to help organizations move beyond "gut feeling" to drive growth through evidence-based strategy.

### 🔗 Connect with me: [LinkedIn](https://www.linkedin.com/in/ayushi-gajendra/)
