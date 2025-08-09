<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

</head>
<body>

<h1>Superstore Profit Maximization Analysis</h1>

<h2>📌 Project Overview</h2>
<p>This project analyzes Superstore sales, profit, and discount data to identify patterns, improve profitability, and guide business decisions. Using four years of data (2014–2017), we examined product categories, regions, states, and discount strategies to uncover opportunities for growth and cost reduction.</p>
<p><b>Core Question:</b> How can the Superstore increase profit without relying solely on sales growth?</p>

<h2>📂 Dataset Description</h2>
<p>Source: Sample Superstore dataset (2014–2017)</p>
<ul>
<li>Rows: ~10,000</li>
<li>Key Columns: Order Date, Ship Date, Ship Mode, Category, Sub-Category, Product Name, Sales, Profit, Discount, Quantity, Region, State, City</li>
</ul>

<h2>🔍 Key Problem Identified – Discount Impact</h2>
<p>After a 20% discount, sales do not significantly increase, and profits turn negative. Higher discounts increase losses without boosting sales. The best strategy is to keep discounts ≤ 20%.</p>
<p><b>Trade-offs:</b> Sales may slightly decrease, but profit will increase. Risk of losing customers who rely on high discounts — need retention strategies.</p>

<h2>📉 Loss-Making Sub-Categories</h2>
<ul>
<li>Tables – Worst-performing, heavy losses every year</li>
<li>Bookcases – Losses in some years</li>
<li>Supplies – Low or negative profit</li>
<li>Machines – Loss only in 2017</li>
</ul>
<p><b>Strategy:</b> Reduce discounts for Tables & Machines to <20% to turn them profitable. For Bookcases & Supplies, either discontinue or create new sales strategies.</p>

<h2>📍 Loss-Making States</h2>
<ul>
<li>Texas, Illinois, Pennsylvania — negative profit in multiple years</li>
<li>Texas has ~40% discount but still loses money</li>
</ul>
<p><b>Action:</b> Reduce discounts in these states to 15–20% for better profitability.</p>

<h2>🛠 Project Workflow</h2>
<ol>
<li>Data Cleaning & Preparation – Removed duplicates, handled missing values, standardized categories, set correct data types</li>
<li>Data Modeling – Created measures (Total Sales, Total Profit, Profit Margin %, Average Discount), added profitability flags</li>
<li>Dashboard Development – Power BI interactive dashboards, slicers, KPIs</li>
</ol>

<h2>📊 Key Visualizations</h2>
<ul>
<li>Profit by Region – Map</li>
<li>Sales & Profit by Category – Bar chart</li>
<li>Discount vs Profit – Scatter plot (0–20% optimal range)</li>
<li>Loss-Making Sub-Categories – Highlighted</li>
<li>State Performance – Discount recommendations</li>
<li>Yearly Trends – Sales & profit over time</li>
</ul>

<h2>💡 Key Recommendations</h2>
<ul>
<li>Keep discounts ≤ 20%</li>
<li>Reduce excessive discounts in loss-making states</li>
<li>Remove: Tables</li>
<li>Revamp: Bookcases, Supplies</li>
<li>Fix: Machines with targeted discounts</li>
<li>Focus marketing in West & East regions</li>
</ul>

<h2>📑 Full Workflow & Results</h2>
<ul>
<li><a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Report.pdf">📄 Full Report (PDF)</a></li>
<li><a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Presentation1.pdf">📊 Presentation (PDF)</a></li>
<li><a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Sample%20-%20Superstore.xlsx">📈 Dataset (Excel)</a></li>
</ul>

<h2>📷 Dashboard Preview</h2>
<p><img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%202025-08-08%20223500.png" width="400">
<img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%202025-08-08%20223417.png" width="400">
<img src="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223417.png" width="400">
  <img src="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223250.png" width="400"></p>

<h2>📈 Business Impact</h2>
<ul>
<li>Expected Profit Increase: +12–18% annually</li>
<li>Customer Retention: Maintain loyalty while cutting unprofitable discounts</li>
<li>Inventory Optimization: Remove loss-making products</li>
<li>Regional Focus: Higher ROI from top-performing regions</li>
</ul>

<h2>🔮 Future Scope</h2>
<ul>
<li>Predictive Discount Modeling</li>
<li>Dynamic Pricing</li>
<li>Customer Segmentation</li>
<li>Supply Chain Optimization</li>
</ul>


<h2>🚀 Conclusion</h2>
<p>By controlling discounts, fixing or discontinuing loss-making products, and focusing on high-profit regions, the Superstore can significantly improve profits while maintaining strong customer relationships.</p>

</body>
</html>
