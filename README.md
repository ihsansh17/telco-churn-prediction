# Telco Customer Churn Prediction

This project aims to assist customer retention team in identifying at-risk customers and making informed decisions to improve retention strategies. The solution includes two machine learning models tailored for different business needs, a user-friendly Streamlit web application, and a FastAPI-based API deployed on AWS Lambda for seamless integration into technical workflows.

## Project Overview

### Problem Statement
Customer churn is a critical challenge in the telecom industry. Retaining customers is more cost-effective than acquiring new ones. This project provides tools to identify potential churners and understand their likelihood of churning, enabling targeted and effective retention efforts.

### Objectives
- Build a high-recall model to catch as many prospective churners as possible.
- Build a probability-calibrated model to accurately estimate churn probabilities.
- Deploy a prediction system with flexible user interaction options.

### Dataset
The dataset is from [Kaggle](https://www.kaggle.com/datasets/johnflag/jb-link-telco-customer-churn). It includes various customer-related features such as:
- Customer demographics (e.g., age, gender, number of dependents).
- Services subscribed (e.g., Internet service, unlimited data, online security).
- Others (e.g., payment method, monthly charges, total refunds).

---

## Models

### 1. **Model 1: Recall-Optimized Model**
- **Purpose**:
  - Predict churn classes (churn/non-churn).
  - Identify as many churners as possible to minimize false negatives (churners predicted as non-churners).
- **Use Case**: Useful for broad retention campaigns as well as high-stakes situations where losing any customer could lead to significant revenue loss.

### 2. **Model 2: Brier Score-Optimized Model**
- **Purpose**:
  - Predict churn probabilities (0-1).
  - Provide reliable churn probabilities with well-calibrated predictions.
- **Use Case**: Useful when retention strategies are based on predicted probabilities rather than just the predicted class. Well-suited for precise retention efforts when resources are limited.


---
## Models

### 1. **Model 1: Recall-Optimized Model**
- **Purpose**: Predict churn classes (churn/non-churn). Identify as many churners as possible to minimize false negatives.
- **Best Use Case**: Useful when the retention team has the budget for broad campaigns and wants to prevent as much churn as possible by casting a wide net. This model helps them target a larger group of at-risk customers. 
- **Best Use Case**: 
  - High-priority scenarios where missing a potential churner is costly.
  - Early-stage churn prevention campaigns to cast a wide net.
- **Benefit**: Maximizes the opportunity to engage with all possible churners, ensuring no one slips through.

### 2. **Model 2: Brier Score-Optimized Model**
In scenarios where decisions are based on predicted probabilities rather than just the predicted class, calibration is essential. For instance, in credit scoring, knowing the exact probability of default helps in setting appropriate interest rates.
- **Purpose**: Provide reliable churn probabilities with well-calibrated predictions.
- **Best Use Case**: Ideal when the team needs to focus on high-risk customers due to budget constraints. They can use Model 2’s reliable probabilities to prioritize customers more likely to churn, allowing for tailored, high-impact interventions.
  - Decision-making where understanding the likelihood of churn is critical.
  - Resource allocation to focus on customers with a higher risk of churning.
- **Benefit**: Ensures actionable and precise insights, enabling data-driven decisions for targeted retention strategies.

---
## Tools & Technologies

1. **Streamlit Web Application**: 
   - **For Non-Technical Users**: 
     - Allows customer retention teams to interact with the models.
     - Two modes:
       - Predict for a single customer with a detailed probability score.
       - Batch predictions via file upload for large-scale analysis.
     - **Output**: Downloadable CSV file with predictions.

2. **FastAPI API**:
   - **For Technical Users**:
     - A RESTful API deployed on AWS Lambda for integration into technical systems.
     - Enables automated and large-scale model usage.

---

## Deployment

- **Streamlit Web App**:
  - Hosted locally or on a cloud platform for easy access by customer retention teams.
  - Interactive interface with no need for technical expertise.

- **FastAPI API**:
  - Deployed on AWS Lambda for scalability and reliability.
  - Designed for technical teams to integrate churn prediction into existing systems.

---

## How to Use

### When to Use Each Model
- **Recall-Optimized Model**:
  - Early churn intervention campaigns.
  - Scenarios where missing a churner has a high impact on revenue or business reputation.

- **Brier Score-Optimized Model**:
  - Post-intervention analysis or high-stakes decisions.
  - Situations requiring precise insights into churn likelihood for resource prioritization.

### Where to Use
- **Streamlit Web App**:
  - Ideal for non-technical users like customer retention teams.
  - Enables quick predictions and insights without requiring programming knowledge.

- **FastAPI API**:
  - Suitable for technical teams building workflows or dashboards.
  - Provides programmatic access to the models for custom use cases.

---

## Key Features

- **Recall-Optimized Model**: Maximizes recall to capture potential churners.
- **Brier Score-Optimized Model**: Reliable churn probability predictions with calibration curve validation.
- **Streamlit Web App**: Simple, intuitive interface for single and bulk predictions.
- **FastAPI API**: High-performance API for seamless integration.
- **AWS Lambda Deployment**: Scalable and cost-effective infrastructure.

---

## Conclusion

This project equips customer retention teams with the tools to make informed, data-driven decisions. By leveraging both models appropriately, businesses can improve their churn management strategies, optimize resources, and enhance customer satisfaction.

For questions or feedback, feel free to [contact me](mailto:your-email@example.com).
