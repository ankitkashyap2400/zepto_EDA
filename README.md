📊 Zepto Retail Data Analysis (EDA)

A comprehensive Exploratory Data Analysis (EDA) project on Zepto product data to uncover insights related to revenue, pricing strategy, discounts, and inventory optimization.

🚀 Project Overview

This project analyzes product-level data from a quick-commerce platform (Zepto) to extract meaningful business insights.

The analysis focuses on:

📈 Revenue generation patterns
💰 Profit estimation across products
🏷️ Discount effectiveness
📦 Inventory and dead stock detection
🧠 Product segmentation (High vs Low value)
🎯 Objectives
Understand pricing and discount strategies
Identify top-performing and underperforming products
Detect inventory inefficiencies
Provide actionable business insights
📂 Dataset Description
Column	Description
Category	Product category
name	Product name
mrp	Maximum Retail Price
discountedSellingPrice	Final selling price
discountPercent	Discount applied
availableQuantity	Available inventory
quantity	Units sold
outOfStock	Stock status
weightInGms	Product weight
🛠️ Tech Stack
Python 🐍
Pandas – Data manipulation
NumPy – Numerical operations
Matplotlib & Seaborn – Visualization
⚙️ Feature Engineering
df["revenue"] = df["discountedSellingPrice"] * df["quantity"]
df["profit_estimate"] = df["mrp"] - df["discountedSellingPrice"]
📊 Analysis Performed
🔹 1. Revenue Analysis
Category-wise revenue contribution
Product-level revenue comparison
df.groupby("Category")["revenue"].sum()
🔹 2. Profit Analysis
Estimated profit across categories
df.groupby("Category")["profit_estimate"].sum()
🔹 3. Discount Analysis
Products with highest discounts
df.sort_values(by="discountPercent", ascending=False)
🔹 4. Inventory Risk (Dead Stock)
dead_stock = df[(df["quantity"] == 0) & (df["availableQuantity"] > 0)]

👉 Helps identify products with zero sales but available inventory

🔹 5. Product Segmentation
def segment(row):
    if row["revenue"] > df["revenue"].median():
        return "High Value"
    else:
        return "Low Value"

df["segment"] = df.apply(segment, axis=1)
📈 Key Visualizations
📊 Revenue by Category
📊 Revenue by Product
📊 Profit by Category
📊 Discount Distribution
📊 Dead Stock Analysis
🔍 Key Insights
💰 Revenue Insights
A small number of products contribute to the majority of revenue
Certain categories dominate sales performance
📉 Discount Insights
Higher discounts do not always increase sales
Some products with low discounts perform better
📦 Inventory Insights
Presence of dead stock indicates inefficient inventory planning
Overstocking leads to capital being blocked
📊 Profit Insights
High revenue ≠ high profit
Lower discounts often result in better margins
🧠 Strategic Recommendations
Optimize discount strategies
Focus on high-performing products
Reduce dead stock with demand-based inventory
Improve pricing for better profit margins
📂 Project Structure
zepto_EDA/
│── data/
│   └── dataset.csv
│── notebooks/
│   └── eda.ipynb
│── src/
│   └── analysis.py
│── outputs/
│   └── charts/
│── README.md
│── requirements.txt
📦 Installation
git clone https://github.com/ankitkashyap2400/zepto_EDA.git
cd zepto_EDA
pip install -r requirements.txt
▶️ Usage
python analysis.py
🧪 Future Improvements
📊 Build dashboard using Streamlit / Power BI
🤖 Add demand forecasting model
⚙️ Automate pipeline using Airflow
☁️ Integrate with AWS S3
💼 Interview Questions You Can Answer
How do you identify dead stock?
Does discount increase sales?
How do you calculate revenue and profit?
What business insights can be derived from EDA?
How would you improve inventory management?
👤 Author

Ankit Kashyap
🔗 GitHub: https://github.com/ankitkashyap2400

⭐ Support

If you found this project helpful, give it a ⭐ on GitHub!

🔥 If you want next upgrade:

I can turn this into:

Resume bullet points (🔥 very important for fresher jobs)
Portfolio explanation (for interviews)
End-to-end Data Engineering project (Airflow + AWS)

Just tell me 👍
