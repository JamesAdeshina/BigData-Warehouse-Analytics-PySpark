# Big Data Warehouse Analytics with PySpark

This repository contains my MSc coursework for **Processing Big Data (7CS516)**.  
It is divided into two main parts:

1. **Evaluation of Cloud Data Warehouses** – a comparative study of AWS Redshift and Google BigQuery.  
2. **Big Data Processing and Analytics with PySpark** – data exploration, cleaning, analysis, and machine learning on sales and product datasets.

---

## 📑 Part 1: Cloud Data Warehouse Evaluation

The report evaluates **Amazon Redshift** and **Google BigQuery** using criteria such as:

- Performance at scale  
- Elasticity  
- Ease of use  
- Security  
- Cost efficiency  
- Integration with other tools  

**Business recommendations:**

- **Small businesses** → BigQuery (cost-effective, serverless, easy BI integration)  
- **Medium businesses** → Redshift (scalability + reserved pricing)  
- **Large enterprises** → Redshift (fine-grained control, strong compliance support)  

📄 Full report available in the [`report/`](report/) folder.  

---

## 📊 Part 2: Big Data Processing and Analytics with PySpark

Implemented in [`code/main.py`](code/main.py).  

### 🔹 Data Preparation
- Standardised column names (snake_case)  
- Checked data integrity across 5 fact tables and 16 dimension tables  
- Validated row counts, duplicates, and null values  

### 🔹 Business and Research Insights
- **Top Products**: Bikes category dominated sales & profit margins  
- **Subcategories**: Road Bikes & Mountain Bikes were the best performers  
- **Territory Analysis**: North America led in sales, followed by Pacific and Europe  
- **Customer Segments**: Middle-income customers (40k–70k) generated the most sales  
- **Occupation Impact**: Professionals contributed the largest revenue share  

### 🔹 Machine Learning (Classification)
**Research Question:** Can we predict product categories based on sales-related features?  

- **Model:** Random Forest Classifier  
- **Features used:** sales_territory_group, order_quantity, sales_amount, freight  
- **Target:** Product Category (English name)  
- **Performance:**  
  - Accuracy → **94.71%**  
  - Precision → 94.76%  
  - Recall → 94.71%  
  - F1-Score → 94.73%  
- Logistic Regression (85.72%) and Naïve Bayes (83.99%) were less effective  
- Confusion matrix confirmed strong prediction accuracy  

---

## 📂 Repository Structure

```
BigData-Warehouse-Analytics-PySpark/
│
├── 📄 README.md
├── requirements.txt
├── .gitignore
│
├── report/
│ ├── Evaluation_of_Big_Data_Platforms_and_Data_Warehouse.pdf
│ └── Evaluation_of_Big_Data_Platforms_and_Data_Warehouse.docx
│
├── code/
│ └── main.py
│
├── datasets/ (sample dataset, if redistribution allowed)
│ ├── DimProduct.csv
│ ├── DimCustomer.csv
│ ├── FactInternetSales.csv
│ └── ...
│
└── figures/
├── sales_by_category.png
├── sales_by_income.png
├── territory_sales.png
├── confusion_matrix.png
└── feature_importance.png
```


---

## 🛠 Technologies Used
- **PySpark** for data processing & ML  
- **Python (pandas, scikit-learn, matplotlib, seaborn)**  
- **AWS Redshift** (evaluated)  
- **Google BigQuery** (evaluated)  

---

## 🚀 Key Outcomes
- Redshift vs BigQuery comparison with real business recommendations  
- Cleaned & validated **fact and dimension tables**  
- Extracted actionable sales insights (product, territory, customer segments)  
- Developed a **Random Forest model with 94.7% accuracy**  

---

## 🔮 Future Work
- Explore boosting algorithms (XGBoost, LightGBM)  
- Apply sequential models (RNNs, LSTMs) for sales forecasting  
- Integrate PySpark pipelines with cloud storage platforms (GCS, S3)  

---

📌 *This repo demonstrates both the theoretical evaluation of cloud data warehouses and the practical application of big data analytics and machine learning using PySpark.*
