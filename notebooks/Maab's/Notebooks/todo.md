# 🧠 Random Ideas and To-Do List

## 1. Data Preprocessing
- Check for and handle **outliers**.
- Apply **scaling** (standardization or normalization) as needed.
- **Encode categorical features**, e.g., using **One-Hot Encoding**.

---

## 2. Feature Engineering
- Work on **creating new features specific to females** (especially for ADHD diagnosis).
- **Amplify emotional problems** features (they might be more revealing for ADHD, especially in females).
- **Make ADHD a feature** for **predicting sex** (model chaining).
- Try **predicting ADHD in females only** to see which symptoms are most apparent — use this insight to engineer features.
- Explore **feature selection techniques**:
  - Use **Information Gain** or similar metrics.
  - Try **LOFO** (Leave-One-Feature-Out) analysis.

---

## 3. Modeling Ideas
- Try **self-supervised learning** or **contrastive learning** approaches to address **data imbalance**.
- Try **model chaining**:
  - **First predict sex**, then **predict ADHD** based on sex.
- Explore **multioutput models** (predicting both ADHD and sex together).
- Experiment with **SVMs** and other **linear models**.
- Try **ensemble learning** approaches (stacking, voting, blending).

---

## 4. Specific Experiments
- Predict **sex** based on **fMRI** and **ADHD features** only.
- Predict **ADHD** without using **fMRI** data (since fMRI-based insights are already reflected in ADHD data).
- Research **predicting sex from fMRI data** independently (ignore ADHD at first to understand the baseline).
- Compare **different techniques for calculating final F1 scores** — see if it impacts rankings.
- Try changing the **seed** and see how that impacts performance (if at all)

---

## 5. Open Questions / Investigations
- Why were `y_Sex` and `y_ADHD` **output as probabilities** instead of **binary values**? 
- Should we **avoid using feature importance** to select features directly? (Possible biases?)
- Should we **amplify certain symptom categories** to better model ADHD in females?
- Dropping ADHD features that are in common between males and females and only leave the different ADHD symptoms and amplify them. To predict if someone has ADHD, check the male and female symptoms in an OR statement. if one of them is more present then mark the person to have ADHD and the specific gender (since now symptoms are in two catergories based on sex) If no symptoms are present then predict sex based on fMRI
- predict sex in ADHD patients only without the use of fMRI

---


# 📝 Notes
- Prioritize experiments that can **improve baseline** first (especially in the next 1-2 days).
- Clearly document which feature engineering or modeling strategy leads to improvement (use validation consistently).
