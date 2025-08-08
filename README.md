<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Superstore Profit Maximization Analysis</title>
  <style>
    :root{
      --accent:#1f77b4;
      --bg:#f6f7f9;
      --card:#ffffff;
      --muted:#666;
      --maxw:1100px;
      --radius:10px;
    }
    body{
      margin:0;
      font-family: "Segoe UI", Arial, sans-serif;
      background:var(--bg);
      color:#222;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }
    .container{
      max-width:var(--maxw);
      margin:28px auto;
      padding:20px;
    }
    header{
      background:var(--accent);
      color:#fff;
      padding:20px;
      border-radius:var(--radius);
      box-shadow:0 6px 20px rgba(31,119,180,0.12);
    }
    header h1{margin:0;font-size:22px}
    header p{margin:8px 0 0 0;opacity:0.95}
    .card{
      background:var(--card);
      padding:16px;
      margin-top:18px;
      border-radius:10px;
      box-shadow:0 8px 24px rgba(20,20,20,0.04);
    }
    h2{color:var(--accent);margin-top:0}
    ul{margin:8px 0 0 18px}
    ol{margin:8px 0 0 18px}
    .files a{
      display:inline-block;
      margin-right:10px;
      margin-top:8px;
      padding:10px 14px;
      border-radius:8px;
      color:#fff;
      background:var(--accent);
      text-decoration:none;
    }
    .files a.alt{background:#28a745}
    .gallery{
      display:flex;
      flex-wrap:wrap;
      gap:12px;
      margin-top:12px;
      justify-content:flex-start;
    }
    .gallery a{display:block;width:48%}
    .gallery img{
      width:100%;
      display:block;
      border-radius:8px;
      border:1px solid #e6e9ed;
      box-shadow:0 8px 20px rgba(0,0,0,0.06);
    }
    .small{color:var(--muted);font-size:14px}
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}
    @media(max-width:800px){
      .gallery a{width:100%}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Superstore Profit Maximization Analysis</h1>
      <p>2014–2017 Superstore data — findings, recommendations, report, presentation, and dashboard previews.</p>
    </header>

    <section class="card">
      <h2>Project Overview</h2>
      <p>This project analyzes Superstore sales, profit, and discount data to identify patterns, improve profitability, and guide business decisions. Using four years of data (2014–2017), we examined product categories, regions, states, and discount strategies to uncover opportunities for growth and cost reduction.</p>
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
        <li>After a <strong>0.2 (20%)</strong> discount there is no significant spike in sales.</li>
        <li>Profits turn negative at higher discounts; discounts above 20% generally increase losses without boosting sales.</li>
        <li><strong>Recommendation:</strong> Keep discounts ≤ 20%.</li>
      </ul>
      <p class="small"><strong>Trade-offs:</strong> Sales may slightly drop, but profit will increase. Customers used to big discounts may churn — add retention strategies (loyalty offers, targeted promos).</p>
    </section>

    <section class="card">
      <h2>Loss-Making Sub-Categories</h2>
      <ul>
        <li><strong>Tables</strong> — heavy losses every year (worst performer).</li>
        <li><strong>Bookcases</strong> — losses in some years.</li>
        <li><strong>Supplies</strong> — low or negative profit.</li>
        <li><strong>Machines</strong> — loss noted in 2017 only.</li>
      </ul>
      <p class="small">Strategy: Reduce discounts on Tables & Machines to &lt;20% to attempt recovery. Bookcases & Supplies: consider bundling, promotions, or discontinuation if unfixable.</p>
    </section>

    <section class="card">
      <h2>Loss-Making States</h2>
      <ul>
        <li>Texas, Illinois, Pennsylvania — negative profit in multiple years.</li>
        <li>Texas currently gives ~40% discount but still loses money.</li>
      </ul>
      <p class="small">Action: Reduce discounts in these states to ~15–20% and monitor profitability. Large discounts are not working in these markets.</p>
    </section>

    <section class="card">
      <h2>Project Workflow</h2>
      <ol>
        <li><strong>Data Cleaning & Preparation:</strong> removed duplicates, handled missing values, standardized categories, ensured proper data types.</li>
        <li><strong>Data Modeling:</strong> created measures (Total Sales, Total Profit, Profit Margin %, Average Discount) and profitability flags.</li>
        <li><strong>Dashboard Development:</strong> Power BI dashboards with slicers (Year, Region, State, Category, Sub-Category, Discount Range) and KPI cards.</li>
      </ol>
    </section>

    <section class="card">
      <h2>Key Visualizations</h2>
      <ul>
        <li>Profit by Region (map)</li>
        <li>Sales & Profit by Category (bar)</li>
        <li>Discount vs Profit (scatter) — optimal 0–20% range</li>
        <li>Loss-making sub-categories table</li>
        <li>State-level performance (Texas, Illinois, Pennsylvania)</li>
        <li>Yearly trends for sales & profit</li>
      </ul>
    </section>

    <section class="card">
      <h2>Key Recommendations</h2>
      <ul>
        <li><strong>Discounts:</strong> keep ≤ 20%; reduce high discounts in loss-making states.</li>
        <li><strong>Products:</strong> discontinue or rework Tables; bundle or promote Bookcases & Supplies; target Machines with controlled discounts.</li>
        <li><strong>Regional:</strong> focus marketing on West & East; investigate Central region costs and returns.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Files & Full Results</h2>
      <div class="files">
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Report.pdf" target="_blank" rel="noopener">Full Report (PDF)</a>
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Presentation1.pdf" target="_blank" rel="noopener">Presentation (PDF)</a>
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Sample%20-%20Superstore.xlsx" target="_blank" rel="noopener">Dataset (Excel)</a>
      </div>
      <p class="small">Open the report or presentation for the complete workflow, visuals, and recommendations.</p>
    </section>

    <section class="card">
      <h2>Dashboard Previews</h2>
      <p class="small">Click an image to open the full screenshot on GitHub.</p>
      <div class="gallery">
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223500.png" target="_blank" rel="noopener">
          <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%25202025-08-08%2520223500.png" alt="Dashboard screenshot 1">
        </a>
        <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223417.png" target="_blank" rel="noopener">
          <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%25202025-08-08%2520223417.png" alt="Dashboard screenshot 2">
        </a>
      </div>
    </section>

    <section class="card">
      <h2>Business Impact</h2>
      <ul>
        <li>Estimated profit increase: <strong>+12–18% annually</strong> after discount optimization and product changes.</li>
        <li>Customer retention: keep loyal customers via targeted offers while cutting unprofitable discounts.</li>
        <li>Inventory optimization: remove loss-makers and reallocate capital to high-margin items.</li>
        <li>Regional focus: invest more in West & East regions to improve ROI.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Future Scope & Investment</h2>
      <ul>
        <li>Predictive discount modeling (ML) and dynamic pricing.</li>
        <li>Customer segmentation for personalized offers.</li>
        <li>Supply chain improvements to cut delivery costs in loss-making regions.</li>
        <li>Investment needed: Power BI Pro, analytics tools, cloud storage, training, promotional budget, data integration.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Conclusion</h2>
      <p>By optimizing discounts, fixing or discontinuing loss-making products, and focusing on high-profit regions, the Superstore can significantly improve profits while maintaining customer relationships.</p>
    </section>

    <footer>
      <p class="small">Prepared for: Superstore Profit Maximization Project — 2014–2017 • © 2025</p>
    </footer>
  </div>
</body>
</html>
