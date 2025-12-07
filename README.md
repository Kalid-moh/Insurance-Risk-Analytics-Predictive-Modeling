# 🚗 Insurance Risk Modeling & Dynamic Pricing System

This project develops a robust, explainable, and risk-aware pricing model for auto insurance policies. It incorporates statistical analysis, machine learning, and reproducible data practices to predict insurance claim severity and optimize premium pricing.

> ✅ Completed as part of the Week 3 Challenge at **10Academy**.

---

## 🧭 Project Goals

- Understand and explore insurance data to uncover actionable insights.
- Establish a reproducible data pipeline using Git, GitHub, and DVC.
- Statistically validate hypotheses related to insurance risk.
- Build predictive models to estimate:
  - 💰 **Claim Severity** — How much we might pay.
  - 📈 **Claim Probability** — How likely a customer is to claim.
- Construct a **dynamic pricing formula** that incorporates business margins.

---

## 🔧 Technologies & Tools

| Area            | Tools Used                        |
| --------------- | --------------------------------- |
| Programming     | Python, Jupyter                   |
| Data Handling   | Pandas, NumPy, DVC                |
| Visualization   | Matplotlib, Seaborn, Plotly       |
| Modeling        | Scikit-learn, XGBoost, SHAP, LIME |
| Version Control | Git, GitHub, GitHub Actions       |
| CI/CD           | GitHub Actions                    |
| Environment     | `venv` + `requirements.txt`       |

---

## 📂 Repository Structure

```text
.
├── data/ # Raw and processed data (tracked via DVC)
├── models/ # Saved models
├── notebooks/ # Jupyter notebooks for EDA, testing, modeling
├── src/ # Core source code
│ ├── preprocessing/ # Cleaning, transformation, encoding
│ ├── task_3/ # Hypothesis testing modules
│ └── task_4/ # Modeling pipeline and interpretation
├── tests/ # Unit tests
├── .dvc/ # DVC metadata
├── .github/workflows/ # GitHub Actions CI pipeline
├── dvc.yaml # DVC pipeline definition
├── requirements.txt # Python dependencies
└── README.md # Project overview (this file)
```

---

## 📊 Task Breakdown

### 🔍 Task 1: EDA & Git Setup

- Configured Git and GitHub, created `task-1` branch
- Performed EDA on claims, premiums, and customer demographics
- Visualized insights across provinces, genders, and vehicle types
- Identified key drivers of loss ratio and risk

### 💾 Task 2: Data Version Control (DVC)

- Installed DVC and initialized version control
- Added data files to DVC tracking
- Set up a **local remote storage** and pushed data
- Ensured reproducibility and auditability of datasets

---

## 📦 Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Kalid-moh/Insurance-Risk-Analytics-Predictive-Modeling.git
   cd insurance-risk-model
   Install dependencies:
   ```

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Run notebooks:

```bash
jupyter notebook
```

Run tests:

```bash
pytest
```

🧪 Data Versioning with DVC
bash
dvc init
dvc add data/raw/insurance_data.csv
dvc remote add -d localstorage /path/to/your/storage
dvc push
To reproduce the data pipeline:

bash
dvc pull
✅ CI/CD
GitHub Actions is configured for:

Code linting

Unit tests

Model validation (optional step)
