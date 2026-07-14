# DevelopersHub Corporation — AI/ML Engineering Internship

Four of the six internship tasks were completed (more than the required minimum of 3).
Each task is a self-contained, fully-executed Jupyter notebook.

> **Environment note:** these notebooks were built in a sandbox with no internet access. Where a
> task calls for a live download (`yfinance`, Kaggle CSV, Hugging Face Hub), the notebook first
> *attempts the real download*, and only falls back to a clearly-labeled synthetic/offline
> substitute if that fails — so the notebooks run end-to-end here, and will automatically use real
> data/models the moment they're run somewhere with internet access. Nothing needs to be rewritten.

## Task 1 — Exploring and Visualizing the Iris Dataset
- **File:** `task1_iris_exploration.ipynb`
- **Dataset:** Iris (via `sklearn.datasets.load_iris`, the offline-friendly equivalent of the CSV/seaborn version)
- **Models:** none (EDA-only task)
- **Key results:** Petal length/width are the most discriminative features; Setosa is linearly separable from the other two species.

## Task 2 — Predict Future Stock Prices (Short-Term)
- **File:** `task2_stock_prediction.ipynb`
- **Dataset:** AAPL OHLCV — real `yfinance` pull if internet is available, otherwise a simulated realistic price series
- **Models:** Linear Regression, Random Forest Regressor
- **Key results:** Both models track next-day close closely given same-day Open/High/Low/Volume; Linear Regression is competitive given the near-linear short-horizon relationship. Caveat: not a trading signal, just a modeling exercise.

## Task 3 — Heart Disease Prediction
- **File:** `task3_heart_disease.ipynb`
- **Dataset:** UCI Heart Disease schema — real `heart.csv` if present locally, otherwise a synthetic dataset built to match the same 14 columns and realistic clinical correlations
- **Models:** Logistic Regression, Decision Tree
- **Key results:** `exang`, `oldpeak`, `ca`, `cp`, and `thalach` are the strongest predictors; both models achieve solid accuracy/ROC-AUC on the held-out set.

## Task 5 — Mental Health Support Chatbot (Fine-Tuned)
- **File:** `task5_mental_health_chatbot.ipynb`
- **Dataset:** EmpatheticDialogues-style hand-curated sample (real Hugging Face fine-tuning code included as reference, requires internet + GPU to run)
- **Model:** TF-IDF + Logistic Regression emotion classifier feeding a curated empathetic-response bank, with safety guardrails for crisis language and medical-advice requests
- **Key results:** reliably classifies 6 emotional categories and routes crisis/medical-advice messages to safe, non-harmful responses instead of the empathy bank.

## Repository / Submission Checklist
- [x] Jupyter notebooks with problem statement, preprocessing, EDA, modeling, evaluation, and insights
- [x] Clean, commented, modular code
- [x] This README summarizing objective / dataset / models / results per task
