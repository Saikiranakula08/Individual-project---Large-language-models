# Individual-project---Large-language-models
Assignment 2 - LLM coding
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ctmgueCcNIX71cGV3I17wSCs_IcjJW0t?usp=sharing)
# Fine-Tuning DistilBERT for Sentiment Analysis on Android App Reviews

This project fine-tunes **DistilBERT**, a lightweight variant of BERT, for binary sentiment classification (Positive/Negative) using user reviews of Android apps. The dataset is sourced from Hugging Face, originally compiled from Google Play and F-Droid open-source apps.

## 🧠 Project Summary

- **Objective**: To apply transfer learning using DistilBERT for analyzing user sentiment in Android app reviews.
- **Dataset**: `sealuzh/app_reviews` (Hugging Face)
- **Model**: `distilbert-base-uncased` fine-tuned using Hugging Face's `Trainer` API
- **Evaluation**: Achieved **90% accuracy** and an F1-score of **0.94** for the positive class

## 📦 Dataset Description

- **Source**: 288,065 user reviews collected from Google Play for 395 open-source Android apps from F-Droid.
- **Features**: Each entry includes the app name, review text, rating, and a derived sentiment label.
- **Classes**: For this project, neutral reviews were excluded. Final dataset contains:
  - Positive reviews
  - Negative reviews

Dataset link: [Hugging Face - sealuzh/app_reviews](https://huggingface.co/datasets/sealuzh/app_reviews)

## 🛠️ Training Setup

- Pre-trained model: `distilbert-base-uncased`
- Framework: 🤗 Transformers & Datasets
- Fine-tuned for **1 epoch** with a batch size of 16
- Evaluation metrics: Accuracy, Precision, Recall, F1-Score
- Optimizer: AdamW

## 🔍 Results

| Metric         | Score     |
|----------------|-----------|
| Accuracy       | 90%       |
| F1-Score (Pos) | 0.94      |
| F1-Score (Neg) | 0.71      |
| Eval Loss      | 0.2857    |

Sample predictions:

- "I love this app! It works flawlessly." → Positive (98.7%)
- "Crashes all the time. Useless." → Negative (84.0%)

## 📊 Analysis

- **Class Distribution**: Imbalanced (Majority: Positive)
- **Confusion Matrix**: Misclassifications mostly occurred in Negative class due to limited data
- **Model Efficiency**: Training was fast and resource-friendly thanks to the distilled model

## 📁 Repository Structure

├── data/ # Sample input data
├── models/ # Fine-tuned model checkpoints
├── scripts/ # Training & evaluation scripts
├── images/ # Confusion matrix, plots
├── report/ # LaTeX and PDF report
├── requirements.txt # Python dependencies
└── README.md

🧪 Tools Used

Python 3.10
Hugging Face Transformers
PyTorch
scikit-learn
matplotlib / seaborn (for visualizations)
📚 References

DistilBERT: Smaller, faster, cheaper
BERT: Language Understanding
Hugging Face Dataset - App Reviews
👨‍💻 Author

Sai Kiran Akula
MSc Data Science (22098314)
GitHub: @Saikiranakula08

