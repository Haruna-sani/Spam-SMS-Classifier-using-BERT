# SMS Spam Classification with BERT and Bi-LSTM

## Overview
This project focuses on classifying SMS messages as spam or not spam using BERT and Bi-LSTM models. The dataset was balanced to ensure fair training, and different architectures were evaluated for performance.

## Model 1: BERT-based Classifier
- **Model:** `TFBertForSequenceClassification`
- **Batch Size:** 16
- **Learning Rate:** 5e-5
- **Epochs:** 5
- **Accuracy:** **0.9995**

### Results
```
Accuracy: 0.9994821336095288

              precision    recall  f1-score   support

           0       1.00      1.00      1.00       954
           1       1.00      1.00      1.00       977

    accuracy                           1.00      1931
   macro avg       1.00      1.00      1.00      1931
weighted avg       1.00      1.00      1.00      1931
```

## Model 2: Bi-LSTM Classifier
- **Preprocessing:** Tokenization & sequence padding
- **Epochs:** 20
- **Accuracy:** **0.9974**

### Results
```
Accuracy: 0.9974

              precision    recall  f1-score   support

           0       1.00      0.99      1.00       954
           1       0.99      1.00      1.00       977

    accuracy                           1.00      1931
   macro avg       1.00      1.00      1.00      1931
weighted avg       1.00      1.00      1.00      1931
```

## Conclusion
- The **BERT-based model** outperformed the Bi-LSTM model with a **higher accuracy (0.9995 vs. 0.9974)**.
- Both models performed exceptionally well, achieving near-perfect precision, recall, and F1 scores.
- The **BERT model is recommended** for spam detection due to its superior performance and efficiency with fewer epochs.

## Future Work
- Exploring other transformer-based models like `DistilBERT` for faster inference.
- Evaluating the impact of larger datasets on model performance.
- Implementing real-time spam detection using the trained model.

