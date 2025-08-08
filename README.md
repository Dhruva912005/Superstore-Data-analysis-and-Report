<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Superstore Profit Maximization Analysis</title>
  <style>
    :root{--accent:#1f77b4;--muted:#555;--bg:#f6f7f9}
    body{font-family:Arial,Helvetica,sans-serif;margin:0;background:var(--bg);color:#222;line-height:1.6}
    .wrap{max-width:1000px;margin:28px auto;padding:20px}
    header{background:var(--accent);color:#fff;padding:18px;border-radius:8px}
    header h1{margin:0;font-size:22px}
    header p{margin:6px 0 0 0;opacity:.95}
    .card{background:#fff;padding:16px;margin-top:14px;border-radius:8px;box-shadow:0 6px 18px rgba(0,0,0,0.05)}
    h2{color:var(--accent);margin-top:0}
    ul{margin:6px 0 6px 20px}
    .files a{display:inline-block;padding:8px 12px;margin-right:8px;margin-top:6px;border-radius:6px;background:#1f77b4;color:#fff;text-decoration:none}
    .files a.alt{background:#28a745}
    .gallery{display:flex;flex-wrap:wrap;gap:12px;margin-top:12px}
    .gallery img{width:48%;max-width:460px;border-radius:6px;border:1px solid #e6e9ed;cursor:pointer}
    .small{color:var(--muted);font-size:14px}
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}
    @media(max-width:720px){.gallery img{width:100%}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>Superstore Profit Maximization Analysis</h1>
      <p>2014–2017 Superstore data — findings, recommendations and downloadable report/dashboard files.</p>
    </header>

    <section class="card">
      <h2>Project Overview</h2>
      <p>
        This project analyzes Superstore sales, profit, and discount data to identify patterns, improve profitability, and guide business decisions.
        Using four years of data (2014–2017), we examined product categories, regions, states, and discount strategies to uncover opportunities for growth and cost reduction.
      </p>
      <p><strong>Core Question:</strong> How can the Superstore increase profit without relying solely on sales growth?</p>
    </section>

    <section class="card">
      <h2>Dataset Description</h2>
      <ul>
        <li><strong>Source:</strong> Sample Superstore dataset (2014–2017)</li>
        <li><strong>Rows:</strong> ~10,000</li>
        <li><strong>Key Columns:</strong> Order Date, Ship Date, Ship Mode, Category, Sub-Category, Product Name, Sales, Profit, Discount, Quantity, Region, State, City</li>
      </ul>
    </section>

    <section class="card">
      <h2>Key Problem Identified — Discount Impact</h2>
      <ul>
        <li>After a <strong>0.2 (20%)</strong> discount, there’s no significant spike in sales.</li>
        <li>Profits turn negative at higher discounts.</li>
        <li>Higher discounts increase losses without boosting sales.</li>
        <li><strong>Best strategy:</strong> Keep discounts ≤ 20%.</li>
      </ul>
      <p class="small"><strong>Trade-offs:</strong> Sales may slightly decrease, but profit will increase. Risk of losing customers who usually buy at high discounts — prepare retention strategies.</p>
    </section>

    <section class="card">
      <h2>Loss-Making Sub-Categories</h2>
      <ul>
        <li><strong>Tables:</strong> Worst-performing — heavy losses every year.</li>
        <li><strong>Bookcases:</strong> Losses in some years.</li>
        <li><strong>Supplies:</strong> Low or negative profit.</li>
        <li><strong>Machines:</strong> Loss only in 2017.</li>
      </ul>
      <p class="small">Strategy: Reduce discounts for Tables & Machines to &lt;20% (data shows 0–0.2 discount range yields good profits). For Bookcases & Supplies, consider discontinuation or new sales strategies (bundles, targeted promos).</p>
    </section>

    <section class="card">
      <h2>Loss-Making States</h2>
      <ul>
        <li>Texas, Illinois, Pennsylvania — negative profit in multiple years.</li>
        <li>Texas has ~40% discount but still loses money.</li>
      </ul>
      <p class="small">Action: Reduce discounts in these states to ~15–20% to increase chance of profitability. Large discounts are not effective in these markets.</p>
    </section>

    <section class="card">
      <h2>Project Workflow</h2>
      <ol>
        <li><strong>Data Cleaning & Preparation:</strong> Removed duplicates, handled missing values, standardized categories, set correct data types.</li>
        <li><strong>Data Modeling:</strong> Created measures (Total Sales, Total Profit, Profit Margin %, Average Discount) and profitability flags.</li>
        <li><strong>Dashboard Development:</strong> Built Power BI dashboards with slicers and KPI cards (Year, Region, State, Category, Sub-Category, Discount Range).</li>
      </ol>
    </section>

    <section class="card">
      <h2>Key Visualizations</h2>
      <ul>
        <li>Profit by Region — map of profitable & loss-making areas.</li>
        <li>Sales & Profit by Category — bar chart comparison.</li>
        <li>Discount vs Profit — scatter showing 0–20% as optimal.</li>
        <li>Loss-making sub-categories — Tables, Machines, etc.</li>
        <li>State-level performance — Texas, Illinois, Pennsylvania flagged.</li>
        <li>Yearly Trends — sales and profit over time.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Recommendations</h2>
      <ul>
        <li><strong>Discount optimization:</strong> Keep discounts ≤ 20%; reduce excessive discounts in loss-making states.</li>
        <li><strong>Product strategy:</strong> Remove Tables; revamp Bookcases & Supplies via bundling/promotions; apply targeted discounts for Machines.</li>
        <li><strong>Regional strategy:</strong> Focus marketing on West & East regions; investigate Central region costs.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Full Workflow & Results — Files</h2>
      <div class="files">
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Report.pdf" target="_blank" rel="noopener">Open Full Report (PDF)</a>
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Presentation1.pdf" target="_blank" rel="noopener" class="alt">Open Presentation (PDF)</a>
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Sample%20-%20Superstore.xlsx" target="_blank" rel="noopener">Open Excel Data</a>
      </div>
      <p class="small">Open the report/presentation links above for the complete workflow, visuals, and recommendations.</p>
    </section>

    <section class="card">
      <h2>Dashboard Preview</h2>
      <div class="gallery">
        <!-- screenshot 1 -->
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223500.png" target="_blank" rel="noopener">
          <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%202025-08-08%20223500.png" alt="Dashboard screenshot 1">
        </a>
        <!-- screenshot 2 -->
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223417.png" target="_blank" rel="noopener">
          <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%202025-08-08%20223417.png" alt="Dashboard screenshot 2">
        </a>
      </div>
      <p class="small">Click an image to open the full screenshot on GitHub.</p>
    </section>

    <section class="card">
      <h2>Business Impact</h2>
      <ul>
        <li>Expected profit increase: <strong>+12–18% annually</strong> (estimate) with discount optimization and product fixes.</li>
        <li>Customer retention: protect loyal customers via targeted offers while cutting unprofitable discounts.</li>
        <li>Inventory optimization: discontinue loss-makers to free working capital.</li>
        <li>Regional focus: invest in high-performing areas for better ROI.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Future Scope</h2>
      <ul>
        <li>Predictive discount modeling (ML) to set optimal discounts per SKU × region.</li>
        <li>Dynamic pricing for demand-driven revenue optimization.</li>
        <li>Customer segmentation for personalized offers and retention.</li>
        <li>Supply chain optimization to lower delivery and fulfillment costs in loss-making regions.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Investment Needs</h2>
      <ul>
        <li>Power BI Pro, advanced analytics tools, and cloud storage.</li>
        <li>Training for sales & marketing teams to use dashboards and act on insights.</li>
        <li>Promotional budget for targeted campaigns in profitable regions.</li>
        <li>Data integration across POS, CRM, and inventory for near real-time analytics.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Conclusion</h2>
      <p>By controlling discounts, fixing or discontinuing loss-making products, and focusing on high-profit regions, the Superstore can significantly improve profits while maintaining strong customer relationships.</p>
    </section>

    <footer>
      <p class="small">Prepared for: Superstore Profit Maximization Project — 2014–2017 • © 2025</p>
    </footer>
  </div>
</body>
</html>
