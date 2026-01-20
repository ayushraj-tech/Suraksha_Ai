# Suraksha_Ai
Suraksha.AI is a machine learning project that analyzes historical crime data to predict safety levels for a given location and time. The system classifies areas into Safe, Not Safe, or Dangerous to support awareness-driven decision making, especially in the context of women’s safety.

# 🔐 Suraksha.AI

### Crime-Based Safety Prediction Using Machine Learning

Suraksha.AI is a machine learning project that analyzes **historical crime data** to estimate the **safety level of a location at a given time**.
The system classifies areas as **Safe**, **Not Safe**, or **Dangerous** based on learned patterns from past incidents.

> ⚠️ This project is intended for **educational and awareness purposes only**.
> It does **not predict crimes** or guarantee safety.

---

## 📌 Project

Safety-related decisions often depend on intuition and incomplete information.
Suraksha.AI explores how **data preprocessing and machine learning** can help identify **risk patterns** using publicly available crime data, with a focus on **women’s safety and social impact**.

---

## ⚙️ How the System Works

### 1️⃣ Data Loading & Cleaning

* Loads real-world crime data (Los Angeles dataset)
* Skips corrupted rows to ensure smooth processing
* Removes records with missing values

### 2️⃣ Feature Selection

Only the most relevant features are used:

* **Latitude (LAT)**
* **Longitude (LON)**
* **Time of Occurrence**

These features strongly influence crime patterns.

### 3️⃣ Time Processing

* Converts time values into **numeric format**
* Extracts the **hour of the day** (e.g., night vs day patterns)
* Removes raw time once hour is derived

### 4️⃣ Risk Labeling Logic

Crime descriptions are mapped to risk levels using keyword-based rules:

| Label | Meaning   |
| ----- | --------- |
| 0     | Safe      |
| 1     | Not Safe  |
| 2     | Dangerous |

This converts text-based crime descriptions into **machine-readable targets**.

### 5️⃣ Model Training

* Uses a **Random Forest Classifier**
* The model is **not pretrained**
* It learns patterns only after being trained on the dataset
* Trained using latitude, longitude, and hour as inputs

### 6️⃣ Prediction

Given:

* Latitude
* Longitude
* Hour

The model predicts a safety level:
**Safe / Not Safe / Dangerous**

---

## 🧠 Key Learnings

* Data preprocessing is critical for meaningful predictions
* Time-based features significantly affect safety patterns
* Machine learning supports **risk awareness**, not certainty
* Model intelligence comes from **data quality**, not algorithm choice

---

## 🛠️ Tech Stack

* **Python**
* **Pandas**
* **Scikit-learn**
* **Random Forest Algorithm**

---

## 📁 Project Structure

```
Suraksha-AI/
│
├── crime_in_la.csv        # Dataset
├── suraksha_ai.ipynb     # Main notebook
├── README.md             # Project documentation
```

---

## ▶️ Example Usage

```python
sample = [[34.05, -118.25, 22]]  # LAT, LON, HOUR
prediction = model.predict(sample)

labels = ['Safe', 'Not Safe', 'Dangerous']
labels[prediction[0]]
```

---

## 📎 Disclaimer

This project:

* Does **not** predict future crimes
* Should **not** be used for real-world safety decisions
* Is built for **learning, experimentation, and awareness**

---

## 🙌 Acknowledgements

This project was developed as part of a learning initiative focused on applying **machine learning for social good**, with guidance and mentorship during the process.

