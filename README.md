# Fraud Detection App

A Machine Learning project to detect fraudulent financial transactions. Built with **Python, Streamlit, and Scikit-learn**, deployed using **Docker and Kubernetes**.

---

## Features

- Real-time fraud detection with Streamlit UI
- User inputs transaction details and receives prediction
- Dockerized for easy deployment
- Kubernetes-ready for scalability

---

## Tech Stack

- Python 3.x
- Pandas, Scikit-learn, Joblib
- Streamlit
- Docker
- Kubernetes (Deployment + Service manifests)

---


## Installation (Local)

```bash
# Clone the repo
git clone https://github.com/hemanth1325/fraud-detection.git
cd fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run app
streamlit run fraud.py
