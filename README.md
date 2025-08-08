<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Superstore Profit Maximization Project</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f8f9fa; color: #222; }
    .container { max-width: 1100px; margin: auto; padding: 20px; }
    h1, h2, h3 { color: #1f77b4; }
    p { line-height: 1.6; }
    section { background: #fff; padding: 16px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
    ul { margin: 0 0 0 20px; }
    .gallery { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 12px; }
    .gallery img { width: 100%; border-radius: 8px; border: 2px solid #eee; }
    .btn { display: inline-block; background: #1f77b4; color: white; padding: 10px 14px; margin: 5px 0; border-radius: 6px; text-decoration: none; }
    .btn.green { background: #28a745; }
  </style>
</head>
<body>
<div class="container">

  <h1>📊 Superstore Profit Maximization Analysis</h1>
  <p>This project analyzes <b>Superstore sales, profit, and discount data</b> to identify patterns, improve profitability, and guide business decisions. Data from <b>2014–2017</b> was used to explore category, region, and discount performance.</p>

  <section>
    <h2>📂 Dataset Description</h2>
    <ul>
      <li>Source: Sample Superstore dataset (2014–2017)</li>
      <li>Rows: ~10,000</li>
      <li>Key Columns: Order Date, Ship Date, Category, Sub-Category, Sales, Profit, Discount, Quantity, Region, State, City</li>
    </ul>
  </section>

  <section>
    <h2>🔍 Key Insights</h2>
    <ul>
      <li>Profit is highest when discounts are ≤ 20%.</li>
      <li>Tables have consistent heavy losses — removal recommended.</li>
      <li>Texas has ~40% discount but is loss-making — reduce to ~15–20%.</li>
      <li>Technology is the most profitable category.</li>
    </ul>
  </section>

  <section>
    <h2>💡 Recommendations</h2>
    <ul>
      <li>Optimize discounts to stay below 20%.</li>
      <li>Remove loss-making products like Tables.</li>
      <li>Revamp Bookcases and Labels through bundling or promotions.</li>
      <li>Focus on West & East regions for higher ROI.</li>
    </ul>
  </section>

  <section>
    <h2>📷 Dashboard Preview</h2>
    <div class="gallery">
      <img src="Screenshot 2025-08-08 223417.png" alt="Dashboard 1">
      <img src="Screenshot 2025-08-08 223250.png" alt="Dashboard 2">
      <img src="Screenshot 2025-08-08 223142.png" alt="Dashboard 3">
      <img src="Screenshot 2025-08-08 223500.png" alt="Dashboard 4">
    </div>
  </section>

  <section>
    <h2>📑 Files</h2>
    <a class="btn" href="Report.pdf" download>📄 Download Full Report</a><br>
    <a class="btn green" href="Presentation1.pdf" download>📊 Download Presentation</a>
  </section>

  <section>
    <h2>📈 Business Impact</h2>
    <ul>
      <li>Expected profit increase: 12–18% annually with discount optimization.</li>
      <li>Better inventory control by removing loss-makers.</li>
      <li>Increased ROI in profitable regions.</li>
    </ul>
  </section>

  <section>
    <h2>🔮 Future Scope</h2>
    <ul>
      <li>Predictive discount modeling.</li>
      <li>Dynamic pricing strategies.</li>
      <li>Customer segmentation for targeted marketing.</li>
    </ul>
  </section>

  <section>
    <h2>💰 Investment Needs</h2>
    <ul>
      <li>Power BI Pro and advanced analytics tools.</li>
      <li>Team training for dashboard usage.</li>
      <li>Data infrastructure for real-time updates.</li>
    </ul>
  </section>

</div>
</body>
</html>
