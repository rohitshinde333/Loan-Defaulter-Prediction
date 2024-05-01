# TVS Credit E.P.I.C Competition - Loan Defaulter Prediction

## Overview
This project secured the second runner-up position nationwide in the TVS Credit E.P.I.C competition. The objective was to predict loan defaulters, utilizing machine learning techniques. The project consists of a Machine Learning (ML) backend built with Flask and a Node.js frontend.

## Project Structure

The project submission contains two main components:

1. **ML Backend:**
    - The `models` folder holds serialized machine learning models used for prediction.
    - `api.py`: This Python Flask application serves as the backend for making predictions. It provides two endpoints:
        - `/predict/personal`: Predicts loan defaulters for personal loans using a combination of machine learning models.
        - `/predict/two_wheeler_loan`: Predicts loan defaulters for two-wheeler loans using a specific machine learning model.
    - The backend utilizes models including Gradient Boosting Classifier, Isolation Forest, K-Nearest Neighbors, Logistic Regression, One-Class SVM, Random Forest, and XGBoost Classifier.

2. **Node Frontend:**
    - The frontend application, developed using Node.js, allows users to interact with the prediction system.
    - It communicates with the Flask backend to request predictions for loan defaulters.
    - The frontend provides a user-friendly interface for inputting data and viewing predictions.

## Model Evaluation
- **Personal Loan Prediction:**
    - Classification Report:
        ```
        precision    recall  f1-score   support
        0.0       0.98      1.00      0.99     35058
        1.0       0.21      0.01      0.03       801
        accuracy                           0.98     35859
        macro avg       0.59      0.51      0.51     35859
        weighted avg    0.96      0.98      0.97     35859
        ```
- **Two Wheeler Loan Prediction:**
    - Test Accuracy: 93.48%
    - ![ROC Curve](/ml_backend/notebooks/two_wheeler_roc_curve.png)


## Usage

### ML Backend:
1. Navigate to the `ml_backend` folder.
2. Ensure Python and the required dependencies listed in `requirements.txt` are installed.
3. Run the Flask API using `python api.py`.
4. The API will start running locally, and it will be accessible at `http://localhost:5000`.

### Node Frontend:
1. Navigate to the `node_frontend` folder.
2. Ensure Node.js and the required dependencies listed in `package.json` are installed.
3. Start the frontend application using `npm start`.
4. Open your web browser and go to `http://localhost:3000` to access the frontend.

## Contributors
- Rohit Shinde (rohitshinde333)
- Vivek Patil 

## Lisence
Proprietary License

Copyright (c) 2024 Rohit Vishwas Shinde

All rights reserved. This work may not be reproduced, modified, distributed, or transmitted in any form or by any means, electronic or mechanical, including photocopying, recording, or by any information storage or retrieval system, without the prior written permission of the copyright owner.

## Acknowledgements
We would like to express our gratitude to TVS Credit for organizing the E.P.I.C competition and providing us with the opportunity to showcase our skills. Additionally, we would like to thank the entire team for their hard work and dedication throughout the project.
