<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>LendingClub Credit Risk Prediction — README</title>
  <style>
    /* Basic reset */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: Inter, Roboto, "Segoe UI", Arial, sans-serif;
      line-height: 1.6;
      color: #0f172a;
      background: #f7fafc;
      padding: 32px;
    }

    .container {
      max-width: 980px;
      margin: 0 auto;
      background: #ffffff;
      border-radius: 12px;
      box-shadow: 0 8px 28px rgba(15,23,42,0.06);
      overflow: hidden;
    }

    header {
      padding: 28px 36px;
      background: linear-gradient(90deg, #0ea5a4 0%, #6366f1 100%);
      color: white;
    }

    header h1 {
      font-size: 20px;
      margin-bottom: 6px;
      letter-spacing: -0.2px;
    }

    header p {
      opacity: 0.95;
      font-size: 14px;
      margin-top: 4px;
    }

    .content {
      padding: 28px 36px;
    }

    h2 {
      font-size: 16px;
      margin-bottom: 10px;
      color: #0f172a;
    }

    p.lead {
      color: #374151;
      margin-bottom: 16px;
    }

    .badge-row {
      display:flex;
      gap:8px;
      margin:12px 0 22px;
      flex-wrap:wrap;
    }

    .badge {
      background:#eef2ff;
      color:#3730a3;
      padding:6px 10px;
      border-radius:999px;
      font-weight:600;
      font-size:12px;
    }

    .section {
      margin-bottom: 20px;
      padding-bottom: 18px;
      border-bottom: 1px dashed #e6edf3;
    }

    ul {
      margin-left: 18px;
      margin-top: 8px;
      color: #334155;
    }

    pre.code {
      background: #0b1220;
      color: #e6eef8;
      padding: 16px;
      border-radius: 8px;
      overflow-x: auto;
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", monospace;
      font-size: 13px;
      line-height: 1.45;
      margin-top: 12px;
    }

    .metrics {
      display:flex;
      gap:18px;
      margin-top:8px;
      flex-wrap:wrap;
    }

    .metric {
      background: #f1f5f9;
      padding: 12px 14px;
      border-radius: 10px;
      min-width: 160px;
      text-align: left;
    }

    .metric .value {
      font-weight: 700;
      font-size: 18px;
      color: #0f172a;
    }

    .metric .label {
      font-size: 12px;
      color: #475569;
      margin-top:4px;
    }

    .footer {
      padding: 18px 36px;
      background: linear-gradient(90deg, rgba(15,23,42,0.03), rgba(99,102,241,0.03));
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:12px;
      flex-wrap:wrap;
    }

    a.cta {
      display:inline-block;
      background:#0ea5a4;
      color:white;
      padding:10px 14px;
      border-radius:8px;
      text-decoration:none;
      font-weight:600;
      font-size:14px;
    }

    .muted { color:#64748b; font-size:13px; }

    @media (max-width:640px){
      .container{ margin: 20px; }
      header h1{ font-size:18px; }
    }
  </style>
</head>
<body>
  <div class="container" role="main">
    <header>
      <h1>LendingClub Credit Risk Prediction</h1>
      <p>Machine learning pipeline to predict loan applicant credit risk using LendingClub data — with focus on accuracy and model stability.</p>
    </header>

    <div class="content">
      <div class="badge-row">
        <div class="badge">Python</div>
        <div class="badge">scikit-learn</div>
        <div class="badge">TensorFlow / Keras</div>
        <div class="badge">Pandas • NumPy</div>
        <div class="badge">Power BI</div>
      </div>

      <section class="section">
        <h2>Project Summary</h2>
        <p class="lead">
          Designed and implemented an end-to-end ML pipeline on a large lending dataset (~405K records) for loan status prediction.
        </p>

        <ul>
          <li>Data preprocessing: missing value imputation, categorical encoding, feature scaling, and removal of leakage features.</li>
          <li>Feature selection using Random Forest importance, reducing dimensionality from 143 → 11 key features.</li>
          <li>Modeling: trained and benchmarked Logistic Regression, Random Forest, Gradient Boosting, and MLP models.</li>
          <li>Model selection based on accuracy and AUC; final model: MLPClassifier.</li>
        </ul>
      </section>

      <section class="section">
        <h2>Key Results</h2>
        <div class="metrics">
          <div class="metric">
            <div class="value">99.6%</div>
            <div class="label">Accuracy (MLPClassifier on hold-out test)</div>
          </div>

          <div class="metric">
            <div class="value">0.998</div>
            <div class="label">ROC AUC (Hold-out test)</div>
          </div>

          <div class="metric">
            <div class="value">143 → 11</div>
            <div class="label">Feature reduction (Random Forest importance)</div>
          </div>
        </div>

        <p style="margin-top:12px; color:#334155;">
          Evaluated performance using confusion matrix, ROC curve, and cross-validation to ensure model reliability and stability over time.
        </p>
      </section>

      <section class="section">
        <h2>Approach & Pipeline</h2>
        <ul>
          <li><strong>Data acquisition:</strong> Load LendingClub loan records and basic cleaning.</li>
          <li><strong>Preprocessing:</strong> Impute missing values, encode categorical columns (one-hot/ordinal), scale numeric features, remove leakage features.</li>
          <li><strong>Feature selection:</strong> Random Forest feature importance to select top predictors.</li>
          <li><strong>Model training:</strong> Train multiple models, tune hyperparameters, and select best by AUC and accuracy.</li>
          <li><strong>Validation:</strong> Cross-validation and hold-out test set for stability monitoring and generalization performance.</li>
        </ul>
      </section>

      <section class="section">
        <h2>How to run</h2>
        <p class="muted">Steps to reproduce results locally</p>

        <pre class="code">
# 1. Clone repo
git clone https://github.com/your-username/lendingclub-credit-risk-prediction.git
cd lendingclub-credit-risk-prediction

# 2. Create / activate virtual environment
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate      # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run notebooks or scripts
# Example: start Jupyter and open the EDA & modeling notebooks
jupyter notebook
        </pre>
      </section>

      <section class="section">
        <h2>Project Structure</h2>
        <pre class="code">
lendingclub-credit-risk-prediction/
├─ data/               # raw and processed datasets
├─ notebooks/          # EDA and modeling notebooks
├─ src/                # scripts for preprocessing, training, evaluation
├─ models/             # saved model artifacts (pkl / h5)
├─ results/            # metrics, plots, and reports
├─ requirements.txt
└─ README.html
        </pre>
      </section>

      <section style="margin-bottom:18px;">
        <h2>Notes & Next Steps</h2>
        <ul>
          <li>Implement model explainability (SHAP / LIME) to improve interpretability for stakeholders.</li>
          <li>Set up model monitoring for drift and performance decay in production.</li>
          <li>Consider deployment with Flask or Streamlit and automated retraining pipelines.</li>
        </ul>
      </section>
    </div>

    <div class="footer">
      <div>
        <div style="font-weight:700;">Yash Parmar — Data Analyst / Data Science Enthusiast</div>
        <div class="muted">Email: py6632388@gmail.com • GitHub: parmar-yash-04</div>
      </div>

      <div style="text-align:right">
        <a class="cta" href="https://github.com/your-username/lendingclub-credit-risk-prediction" target="_blank" rel="noopener">View on GitHub</a>
      </div>
    </div>
  </div>
</body>
</html>
