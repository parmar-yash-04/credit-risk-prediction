<h1 align="center">📊 Credit Risk Prediction using Machine Learning</h1>

<p align="center">
  <b>Predicting loan applicant risk levels using LendingClub dataset (2014–2018)</b>
</p>

---

<h2>🚀 Project Overview</h2>
<p>
This project focuses on predicting the <b>credit risk</b> of loan applicants using machine learning techniques.  
By analyzing LendingClub loan data, the model classifies applicants as <b>low-risk</b> or <b>high-risk</b>, 
helping financial institutions make better lending decisions.
</p>

---

<h2>📂 Dataset</h2>
<p>
The dataset is very large (cannot be uploaded to GitHub due to the 25MB limit).  
You can access the dataset here:  
👉 <a href="https://drive.google.com/file/d/1xTW766DWN4dXBk4vkFOjBekxWKbpPMqJ/view?usp=sharing" target="_blank"><b>Download Dataset</b></a>
</p>

---

<h2>⚙️ Steps Performed</h2>
<ul>
  <li>Data Cleaning & Missing Value Handling</li>
  <li>Feature Engineering (categorical, numerical, date features)</li>
  <li>Feature Selection (Correlation + Recursive Feature Elimination)</li>
  <li>Data Scaling using <code>StandardScaler</code></li>
  <li>Model Training with <b>Random Forest</b> and evaluation</li>
</ul>

---

<h2>🧠 Model Training</h2>
<p>
- Target variable: <code>loan_status_binary</code>  
- 1 = Good Loan (Low Risk)  
- 0 = Defaulted Loan (High Risk)  
</p>

---

<h2>📊 Results</h2>
<p>
The Random Forest model achieved strong predictive performance.  
(Fill in your <b>accuracy/precision/recall/AUC</b> values here from notebook results.)
</p>

---

<h2>📌 How to Run</h2>
<pre>
# Clone this repository
git clone https://github.com/your-username/credit-risk-prediction.git
cd credit-risk-prediction

# Install dependencies
pip install -r requirements.txt

# Run the Jupyter Notebook
jupyter notebook credit-risk-prediction.ipynb
</pre>

---

<h2>🔗 References</h2>
<ul>
  <li><a href="https://drive.google.com/file/d/1xTW766DWN4dXBk4vkFOjBekxWKbpPMqJ/view?usp=sharing" target="_blank">Dataset</a></li>
  <li><a href="https://www.kaggle.com/" target="_blank">Kaggle</a></li>
</ul>

---
<p align="center">✨ Developed with ❤️ using Python & scikit-learn ✨</p>
