# Loan_Approval-System

**Business Objective of the Project**

The primary goal of this project is to build a predictive model that identifies and evaluates the likelihood of loan default for individuals applying for loans. This model is designed to address key business objectives such as:

**Mitigating Financial Risk:**

Financial institutions can minimize their exposure to high-risk borrowers by accurately predicting loan defaults, thus safeguarding their assets and reducing non-performing loans (NPLs).

**Optimizing Credit Decision-Making:**
The model supports faster and more data-driven decisions in the loan approval process, ensuring that loans are granted to creditworthy individuals while reducing manual intervention.

**Enhancing Profitability:**
The institution can maintain a profitable balance between risk and reward by approving loans for low-risk customers and implementing stricter terms for high-risk ones.

**Improving Operational Efficiency:**
Automating the risk assessment process through machine learning reduces the time and resources required for traditional credit checks and underwriting processes.

**Personalized Loan Offers:**
The insights from the model (e.g., identifying key risk factors) can help tailor loan products, interest rates, and repayment terms to match customer profiles, improving customer satisfaction and retention.

**Regulatory Compliance:**
Ensures adherence to legal and regulatory guidelines by providing a systematic and fair credit evaluation process, reducing potential biases in loan approval.

# End Goal
The ultimate objective is to create a scalable and reliable loan default prediction system that aids financial institutions in making more informed, data-driven decisions, thus balancing profitability and risk management.

# Summary	of	the	Dataset
 This	dataset	is	a	synthetic	version	inspired	by	the	original	Credit	Risk	dataset	and	enriched	with	additional	variables	based	on	Financial
 Risk	for	Loan	Approval	Data.	The	dataset	is	structured	for	both	categorical	and	continuous	features.
 The	dataset	contains	45,000	records	(rows)	and	14	variables	(Columns),	each	described	below:
 
 **Column	description**
 1.	*person_age:-Age	of	the	person	(Float)*
 2.	*person_gender:-	*Gender	of	the	person	(Categorical)*
 3.	*person_education:-Highest	education	level	(Categorical)*
 4.	*person_income:-	Annual	Income	(Float)*
 5.	*person_emp_exp:-Years	of	employment	experience	(Integer)*
 6.	*person_home_ownership:-Home	ownership	status	(e.g.,	rent,	own,	mortgage)	(Categorical)*
 7.	*loan_amnt:-	Loan	amount	requested	(Float)*
 8.	*loan_intent:-Purpose	of	the	loan	(Categorical)*
 9.	*loan_int_rate:-Loan	interest	rate	(Float)*
 10.	*loan_percent_income:-	Loan	amount	as	a	percentage	of	annual	income	(Float)*
 11.	*cb_person_cred_hist_length:-Length	of	credit	history	in	years	(Float)*
 12.	*credit_score:-	Credit	score	of	the	person	(Integer)*
 13.	*previous_loan_defaults_on_file:-Indicator	of	previous	loan	defaults	(Categorical)*
 14.	*loan_status	(target	variable):-Loan	approval	status:	1	=	approved;	0	=	rejected	(Integer)*

# Best Performing Model After Hyperparameter Tuning
To determine which model performs best between LightGBM and the Neural Network, we need to compare their evaluation metrics on the test set.

**LightGBM Performance:**

1. Accuracy: 93.43%
2. Precision: 87.91%
3. Recall: 80.95%
4. F1-Score: 84.29%
5. ROC-AUC: 97.99%

**Neural Network Performance:**

1. Accuracy: 91.94%
2. Precision: 81.37%
3. Recall: 81.66%
4. F1-Score: 81.52%
5. ROC-AUC: 97.10%

# Comparison:

**Accuracy:**
1. LightGBM (93.43%) outperforms the Neural Network (91.94%).
2. Indicates that LightGBM makes fewer overall classification errors.

**Precision:**
1. LightGBM (87.91%) outperforms the Neural Network (81.37%).
2. LightGBM is better at avoiding false positives (cases predicted as positive but are actually negative).

**Recall:**
1. Neural Network (81.66%) slightly outperforms LightGBM (80.95%).
2. Neural Network is better at identifying true positives (cases that are positive and correctly classified).

**F1-Score:**

1. LightGBM (84.29%) outperforms the Neural Network (81.52%).
2. Indicates that LightGBM achieves a better balance between precision and recall.

**ROC-AUC:**

1. LightGBM (97.99%) outperforms the Neural Network (97.10%).
2. LightGBM has slightly better discriminatory power, meaning it can better distinguish between positive and negative classes.

**Conclusion:**

1. LightGBM performs better overall based on most evaluation metrics, especially in terms of accuracy, precision, F1-Score, and ROC-AUC.
2. The Neural Network has a slight edge in recall, but the difference is minimal.

**Recommendation:**

1. Use LightGBM as the final model for deployment or further testing, especially if precision and overall accuracy are critical for the business problem.
2. Consider the Neural Network if recall (i.e., minimizing false negatives) is more important in your application.
