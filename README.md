🛒 E-Commerce Sales EDA Project
📌 Overview

This project performs Exploratory Data Analysis (EDA) on an e-commerce dataset to uncover insights related to pricing, discounts, revenue, and inventory management.

The goal is to help businesses make data-driven decisions by identifying:

High-performing products
Profit opportunities
Inventory risks
Discount effectiveness
📂 Dataset Description

The dataset contains the following columns:

Column Name	Description
Category	Product category
name	Product name
mrp	Maximum Retail Price
discountPercent	Discount percentage
discountedSellingPrice	Final selling price
availableQuantity	Available stock
quantity	Units sold
outOfStock	Stock status
weightInGms	Product weight
⚙️ Tech Stack
🐍 Python
📊 Pandas
📉 Matplotlib / Seaborn
📓 Jupyter Notebook
📊 Key Analysis Performed
1️⃣ Revenue Analysis
Calculated revenue:
df["revenue"] = df["discountedSellingPrice"] * df["quantity"]
Identified top-performing categories and products
2️⃣ Profit Estimation
df["profit_estimate"] = df["mrp"] - df["discountedSellingPrice"]
Found categories with highest profit margins
3️⃣ Discount Analysis
Products with highest discounts
Impact of discount on sales
4️⃣ Inventory Risk Analysis
Identified dead stock
dead_stock = df[(df["quantity"] == 0) & (df["availableQuantity"] > 0)]
5️⃣ Customer Value Segmentation
def segment(row):
    if row["revenue"] > df["revenue"].median():
        return "High Value"
    else:
        return "Low Value"
📈 Key Insights
📌 High discounts do not always lead to higher sales
📌 Some products generate high revenue with low discounts
📌 Presence of dead stock indicates poor inventory planning
📌 Certain categories dominate overall revenue
📌 Profit margins vary significantly across categories
📊 Visualizations
Revenue by Category
Revenue by Product
Discount Distribution
Profit Analysis
Inventory Risk Charts
🚀 How to Run
Clone the repository
git clone https://github.com/your-username/your-repo-name.git
Install dependencies
pip install pandas matplotlib seaborn
Run the notebook
jupyter notebook
📌 Project Structure
📁 EDA-Project
│── 📄 data.csv
│── 📄 eda.ipynb
│── 📄 README.md
🎯 Future Improvements
Add machine learning for demand prediction
Build dashboard using Power BI / Tableau
Deploy using Streamlit
🤝 Contributing

Feel free to fork this repo and improve it!

