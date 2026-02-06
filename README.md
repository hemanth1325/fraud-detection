Fraud Detection App

A Machine Learning project to detect fraudulent financial transactions. Built with Python, Pandas, Scikit-learn, and Streamlit, deployed using Docker and Kubernetes.

This repo includes both the data exploration / ML workflow (from Jupyter Notebook) and the interactive deployed app.

Features

End-to-end ML pipeline: data cleaning, visualization, feature engineering, model training

Real-time fraud prediction with Streamlit UI

Dockerized for easy deployment

Kubernetes-ready for scalability

Tech Stack

Python 3.x

Pandas, NumPy

Matplotlib, Seaborn (visualizations)

Scikit-learn, Joblib (ML + model saving)

Streamlit (interactive app)

Docker (containerization)

Kubernetes (deployment + service manifests)

Project Structure
fraud-detection/
├── fraud.py                   # Streamlit app for real-time prediction
├── fraud_detection_model.pkl  # Trained ML model
├── fraud_analysis.ipynb       # Step-by-step Jupyter Notebook
├── requirements.txt           # Python dependencies
├── Dockerfile                 # Docker container definition
├── k8s-deployment.yaml        # Kubernetes manifests
├── README.md                  # Project documentation
└── assets/                    # Screenshots / plots

Step-by-Step Workflow (Jupyter Notebook)

Load Dataset

Load your CSV dataset into Pandas.

Inspect data for nulls, duplicates, and incorrect values.

Data Cleaning

Handle missing values.

Fix incorrect balances or transaction types.

Create derived features if necessary (e.g., balanceDiff = oldbalanceOrg - newbalanceOrig).

Exploratory Data Analysis (EDA)

Visualize transaction types, amounts, and fraud distribution.

Example plots:

Fraud count per transaction type

Transaction amount distribution

Correlation heatmap

Feature Engineering

Encode categorical features (Transaction Type) using one-hot encoding or label encoding.

Scale numeric features if needed.

Machine Learning

Split dataset into train/test.

Train model (e.g., Logistic Regression, RandomForest, XGBoost).

Evaluate model using metrics: accuracy, precision, recall, F1-score.

Save trained model using joblib.

Streamlit App

Load saved ML model.

Collect user input for new transactions.

Predict fraud in real-time.

Display results (Fraud / Not Fraud) with Streamlit UI.

Installation (Local)
# Clone repo
git clone https://github.com/hemanth1325/fraud-detection.git
cd fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook (optional, for step-by-step analysis)
jupyter notebook fraud_analysis.ipynb

# Run Streamlit app
streamlit run fraud.py

Docker Deployment
# Build Docker image
docker build -t fraud-detection-app .

# Run Docker container
docker run -p 8501:8501 fraud-detection-app

# Open in browser: http://localhost:8501

Kubernetes Deployment
# Apply deployment
kubectl apply -f k8s-deployment.yaml

# Forward port locally to access the app
kubectl port-forward service/fraud-detection-service 8501:8501



Include a plot example from EDA (optional).

Future Improvements

Add more ML models and compare performance

Feature importance visualization

CI/CD pipeline for automatic redeployment

Cloud deployment (AWS/GCP/Azure)

Multi-user dashboard with authentication

This structure shows your complete ML workflow to recruiters:

Step-by-step analysis (Jupyter Notebook)

Code reproducibility (requirements + Docker + K8s)

Deployment skills (Streamlit, Docker, Kubernetes)
