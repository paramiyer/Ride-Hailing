# Ride-Hailing
# Predicting Customer Rating Probability – Careem Data Science Challenge Submission

This notebook presents a solution to a real-world data science case submitted for a Careem interview process. The task involves predicting the probability that a user will **rate a trip**, based on historical trip and customer data.

## 📌 Problem Statement

To predict the likelihood of a trip being rated (`was_rated = 1`) using available features from trip and rating datasets. Special attention was paid to trip cancellations and customer-level behavior.

## 🧠 Key Assumptions & Strategy

- Trips that are cancelled are **not rated** (`was_rated = 0`).
- Speeds and distances have limited influence on the **act of rating** itself.
- Historical **rating probability** for each customer is a significant feature.
- Default rating probability for unknown customers: **0.5**.

## 🛠️ Feature Engineering

- Computed per-customer historical rating probabilities.
- Merged with training and test data.
- Focused only on **non-cancelled trips** for modeling.

## 🔧 Tech Stack

- R (with `caret`, `e1071`, and data manipulation packages).
- No heavy preprocessing or anomaly filtering done, as test/train inconsistencies were assumed.

## 🚧 Known Limitations

- The notebook ends with transformation and merging steps — final model evaluation and submission logic may need review.
- Mixed or incomplete R environment setup at the end (`install.packages` usage).

## 📂 Structure

- `main.ipynb`: Main notebook with feature engineering and modeling logic.
- `trip_rating` dataset used for historical feature extraction <not included in git>

---

> 📌 Note: This notebook was originally prepared for a confidential interview use case. No proprietary data or internal IP is disclosed.
