# PAWsitive-Tails: Shaping Brighter Futures for Shelter Pets

## Project Overview
This project is a comprehensive data science initiative focused on improving the lives of animals in shelters. Using the attached dataset—which includes details on animal demographics, health status, intake reasons (such as old age, sickness, or behavioral issues), and outcomes (like adoption, euthanasia, or transfer)—we aim to leverage advanced analytical methods to predict shelter animal outcomes and optimize resource allocation.

## Objectives and Goals

### Predictive Modeling
Develop state-of-the-art supervised learning models (such as **XGBoost, LightGBM, CatBoost, and other ensemble techniques**) to accurately predict shelter animal outcomes. Performance will be primarily evaluated using the **AUC-ROC metric** to ensure robust model validation.

### Exploratory Data Analysis (EDA) and Feature Engineering
Conduct an in-depth **EDA** to uncover **trends, correlations, and anomalies** within the data. Through meticulous **feature engineering**, we aim to enhance model performance and reveal critical factors that drive animal outcomes.

### Unsupervised Learning Insights
Utilize **unsupervised learning techniques** like **clustering and anomaly detection** to identify **latent patterns** and groupings among the animals. This step will help in understanding **complex relationships** in the data that may not be immediately evident through supervised methods alone.

### Causal Inference
Apply **causal inference methods** to test hypotheses regarding the impact of **specific features** (for example, age, medical condition, or intake reason) on the outcome. This analysis will help determine whether these factors **causally influence outcomes**, guiding more effective interventions.

### Resource Allocation for Shelters
Translate **data-driven insights** into **actionable strategies** that enable shelters to better allocate **funding and resources**. By anticipating the needs of shelter animals through **predictive analytics**, shelters can implement **proactive measures** that enhance **animal welfare** and increase **successful outcomes**.

---

## Stacking Model Performance Analysis

### Overview
To enhance prediction accuracy, we implemented a **stacking ensemble approach** using different **meta-models**. The base models used for stacking included:
- **LightGBM**
- **XGBoost**
- **CatBoost**
- **Random Forest**
- **Decision Trees**

Each stacking model was trained with **three different meta-learners**:
1. **Logistic Regression**
2. **Support Vector Machine (SVM)**
3. **Random Forest**

Additionally, we tested **three different base model combinations**, each consisting of three models.

### Model Combinations and Performance
We trained three stacking models for each meta-learner, evaluating their performance using **cross-validated accuracy scores**. Below is a summary of our results:

| Meta-Model                  | Combination 1 (LGBM + XGB + CatBoost) | Combination 2 (XGB + RF + CatBoost) | Combination 3 (LGBM + DT + CatBoost) | Mean Accuracy |
|-----------------------------|----------------------------------|----------------------------------|----------------------------------|---------------|
| **Logistic Regression**      | **0.8390**                      | 0.8323                           | 0.8385                           | 0.8366        |
| **Support Vector Machine**   | **0.8439**                      | 0.8387                           | 0.8433                           | **0.8420**    |
| **Random Forest**            | 0.8336                           | 0.8255                           | 0.8354                           | 0.8315        |

### Key Insights
- **Support Vector Machine (SVM) as a meta-model** performed the **best**, achieving the **highest mean accuracy** across different stacking combinations.
- **Logistic Regression** was a close second, demonstrating **stable performance** across different combinations.
- **Random Forest**, while still effective, had **slightly lower accuracy** compared to the other two meta-models.
- **Combination 1 (LGBM + XGB + CatBoost) consistently outperformed the other base model combinations** across all meta-models.

**Based on these findings, the SVM-based stacking model using LGBM, XGBoost, and CatBoost is the most effective choice for our dataset.** Future iterations can explore **hyperparameter tuning and additional feature engineering techniques** to further enhance performance.

The final model is stored as a `.pkl` file.

---

# Model Evaluation and Considerations

## Model Evaluation and Accuracy as a Metric
In this study, we used **accuracy** as the primary evaluation metric due to its straightforward interpretability and ease of comparison across different models. While accuracy provides a general measure of overall model performance, it does not account for class imbalances or misclassification costs, which are important considerations in a multiclass setting.

## Threats to Validity
There are a few key limitations in our approach that should be addressed in future iterations:

1. **Evaluation Metrics**: Accuracy alone is not the most informative metric for a multiclass classification problem. It does not distinguish between different types of misclassification. In future work, we would incorporate **precision, recall, F1-score, and confusion matrices** to gain a more detailed understanding of the model's performance across each outcome category.
   
2. **Data Sampling**: Due to computational constraints, we performed training on **only 40% of the dataset** to ensure feasibility within a reasonable time frame. While this approach provided a balance between training time and model performance, future work should aim to train on the **full dataset**, leveraging more efficient computational resources or model optimization techniques.

3. **Data Matching Approach**: Currently, we **only used the latest instance of each outcome and intake event** for a unique animal ID. This simplified approach reduces noise but also **limits the amount of available training data**. In the future, we plan to match **all intake and outcome instances** for each animal to create a richer dataset with more training samples.

## Future Improvements
To enhance model performance and robustness, we suggest the following improvements:
- **Use More Robust Metrics**: Incorporate **F1-score, precision-recall curves, and confusion matrices** to better evaluate performance across different outcome categories.
- **Train on the Full Dataset**: Optimize the model and use more computational resources to **train on 100% of the available data** instead of 40%.
- **Improve Feature Engineering**: Consider **time-based sequences** by analyzing multiple intake and outcome events per animal rather than only using the latest instance.

By addressing these limitations, we can improve the accuracy, generalizability, and interpretability of the model while leveraging more comprehensive data for training.

---

## Impact
At its core, this project is passionate about **transforming negative trajectories**—such as **euthanasia or prolonged shelter stays**—into **positive, life-changing outcomes** for animals. By merging **innovative data science techniques** with a **commitment to animal welfare**, the project strives to provide shelters with the **insights needed to make informed decisions, optimize care processes, and ultimately ensure a brighter future for every animal in their care.** 

---

## Contributors
- Sahil Negi
- Ashraf Elrufaie
- Nehal Joshi
- Atharva Vyas
