# **Customer Churn Prediction**

## ** Overview**
Customer churn is important for business, particularly in the telecom industry, where retaining customers is as important as acquiring new ones. This project uses machine learning models to predict customer churn and identify key factors influencing churn behavior.

## **Business and Data Understanding**
Stakeholder: The telecom company's customer retention team, including marketing and customer service managers.

### **Dataset Choice**
- The dataset contains the following information belonging to telecom customers:
- **state**: The state where the customer lives.  
- **account length**: Number of days the customer has had an account.  
- **area code**: Customer's area code.  
- **phone number**: Customer's phone number.  
- **international plan**: Yes if the customer has the international plan, No otherwise.  
- **voice mail plan**: Yes if the customer has the voice mail plan, No otherwise.  
- **number vmail messages**: Number of voicemails sent by the customer.  
- **total day minutes**: Total call duration (minutes) during the day.  
- **total day calls**: Total number of calls during the day.  
- **total day charge**: Total charges for calls made during the day.  
- **total eve minutes**: Total call duration (minutes) in the evening.  
- **total eve calls**: Total number of calls in the evening.  
- **total eve charge**: Total charges for calls made in the evening.  
- **total night minutes**: Total call duration (minutes) at night.  
- **total night calls**: Total number of calls at night.  
- **total night charge**: Total charges for calls made at night.  
- **total intl minutes**: Total call duration (minutes) for international calls.  
- **total intl calls**: Total number of international calls.  
- **total intl charge**: Total charges for international calls.  
- **customer service calls**: Number of calls made to customer service.  
- **churn** (*Target Variable*): `True` if the customer terminated their contract, `False` otherwise.
- 
## **Modeling Approach**
Multiple ML models were used to predict churn:

### **Logistic Regression**
- Simple and interpretable.

### **Decision Tree**
- Captures nonlinear relationships
- Easy to visualize and explain to stakeholders

### **Random Forest (Best Model)**
- Combines multiple decision trees to improve accuracy
- Achieved highest AUC and recall score

### **Handling Imbalanced Data**
- Churn is a minority class in the dataset.
- SMOTE was used to balance the dataset and improve model performance.

---

### **ROC Curve for Model Comparison**
- The RF model outperformed other models.
- This means the model can effectively distinguish between churners and non-churners.

---

## **Conclusion**
**Top Factors Influencing Churn:**
- **Higher International Charges** increase churn risk.
- **High Customer Service Calls** increase churn probability.
- **Lack of a Voice Mail Plan** increases churn risk.

**Business Recommendations**
- Improve customer support efficiency to reduce complaints.
- Offer loyalty incentives for long-term customers.
- Target customers at risk of churning with special retention offers.
