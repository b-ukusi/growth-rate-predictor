# 🧬 Ovarian Cyst Growth Rate Predictor

This project predicts ovarian cyst growth rate (in cm/day) using patient data and machine learning. It also classifies cysts into categories like "Stable", "Moderate-growing", or "Fast-growing", and generates a PDF report for each case.

---

## 📦 What’s Included

```
growth-rate-predictor/
├── growth_rate_model.pkl       ✅ Trained PyCaret model
├── model.py                    ✅ Script to run predictions and generate reports
├── train_model.py              ✅ (Optional) Code used to train the model
├── requirements.txt            ✅ All dependencies needed to run the project
├── test_data.csv               ✅ Example input file
└── README.md                   ✅ This file
```

---

## 🚀 Getting Started

### 🔧 1. Clone this repository

```bash
git clone https://github.com/YOUR_USERNAME/growth-rate-predictor.git
cd growth-rate-predictor
```

### 📦 2. Install dependencies

Create a virtual environment (optional but recommended), then install:

```bash
pip install -r requirements.txt
```

---

## 📁 3. Prepare Your Data

Use the format in `test_data.csv`. Required columns include:

- `Age`
- `CA_125_Level`
- `Cyst_Size_cm`
- `Menopause_Status`
- `Ultrasound_Features`
- `Reported_Symptoms`
- `Recommended_Management`
- `Region`

Optional:
- `Patient_ID` (used in the report)

Upload your data file (e.g. `your_data.csv`) for prediction.

---

## 🔮 4. Run Predictions and Generate PDF

Use the script below to generate growth rate predictions and export a PDF report.

### 👉 Example:

```python
import pandas as pd
from model import predict_growth_rate

# Load your data
df = pd.read_csv('your_data.csv')

# Run prediction and generate report
predict_growth_rate(df, pdf_filename='cyst_growth_report.pdf')
```

The script will:
- Load the trained model
- Clean and transform your data
- Predict the growth rate
- Classify it (e.g., "Fast-growing")
- Export a summary PDF report
- Print the top 10 fastest-growing cases to the console

---

## 📄 Example Output

PDF report: `cyst_growth_report.pdf`  
Console output: Top 10 fastest-growing cysts

---

## 🧠 About the Model

- Trained with [PyCaret](https://pycaret.org/) using a LightGBM/RandomForest/CatBoost pipeline
- Handles preprocessing (categorical encoding, normalization, etc.)
- Built from anonymized ovarian cyst tracking data

---

## 🤝 Credits

Built by Naomi Bukusi using open-source tools  
Data source: synthetic sample inspired by ovarian cyst tracking studies  
Libraries: PyCaret, scikit-learn, CatBoost, LightGBM, ReportLab

---

## 📬 Need Help?

Open an issue or contact the maintainer via email or GitHub.
