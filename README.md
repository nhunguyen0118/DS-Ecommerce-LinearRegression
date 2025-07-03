# 🛍️ E-Commerce Customer Spending Analysis

An Ecommerce company based in New York City that sells clothing online but they also have in-store style and clothing advice sessions. Customers come in to the store, have sessions/meetings with a personal stylist, then they can go home and order either on a mobile app or website for the clothes they want.

The company is trying to decide whether to focus their efforts on their mobile app experience or their website.

---

## 📊 Dataset Description

The dataset contains information on customer demographics and usage behavior:

* `Avg. Session Length`: Average time customers spend in each session.
* `Time on App`: Time spent on the mobile app.
* `Time on Website`: Time spent on the website.
* `Length of Membership`: Years as a customer.
* `Yearly Amount Spent`: Target variable.

---

## 🔍 Exploratory Data Analysis (EDA)

* `length_of_membership` and `time_on_app` showed strong positive correlations with `yearly_amount_spent`.
* `time_on_website` had a very weak correlation.
* Pairplot and scatterplots confirmed linear relationships for `length_of_membership` and `time_on_app`.

---

## 🤖 Model Summary

A Linear Regression model was trained to predict `yearly_amount_spent` based on customer behavior features.

* **R² Score**: \~0.989
* **RMSE**: \~8.93
* **MAE**: \~7.23

### ✅ Residual Analysis

* Residuals were approximately normally distributed and centered around zero.
* This supports the assumption of linearity and indicates the model is unbiased and reliable.

---

## 📈 Feature Impact Overview

| Feature                | Coefficient | Insight                                                     |
| ---------------------- | ----------- | ----------------------------------------------------------- |
| `length_of_membership` | Highest     | Long-term customers tend to spend significantly more.       |
| `time_on_app`          | Strong      | App usage has a strong positive relationship with spending. |
| `time_on_website`      | Very low    | Minimal impact on customer spending.                        |

---

## 📌 Conclusion & Recommendation

Based on the model results:

> **Time spent on the mobile app** has a much stronger influence on customer spending than time spent on the website.

### 🔎 Recommendation

The company should **prioritize improving the mobile app experience**, focusing on:

* Better UI/UX design
* Personalized recommendations
* Mobile-specific promotions

These changes are likely to drive higher customer engagement and spending.

---

## 💻 Tech Stack

* Python (pandas, matplotlib, seaborn, scikit-learn, statsmodels)
* Jupyter Notebook

---

## 📂 Project Structure

```
.
├── data/                   # CSV files
├── notebooks/             # Jupyter notebook
├── images/                # Plots and visualizations
├── README.md              # Project summary
```

---
