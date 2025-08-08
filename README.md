<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Superstore Profit Maximization Analysis</title>
  <style>
    :root{--accent:#1f77b4;--muted:#555;--bg:#f6f7f9;--card:#fff;--maxw:1100px}
    body{font-family:Segoe UI, Roboto, Arial, sans-serif;margin:0;background:var(--bg);color:#222;line-height:1.5}
    .wrap{max-width:var(--maxw);margin:28px auto;padding:20px}
    header{background:var(--accent);color:#fff;padding:18px;border-radius:10px}
    header h1{margin:0;font-size:22px}
    header p{margin:6px 0 0 0;opacity:.95}
    .card{background:var(--card);padding:16px;border-radius:10px;margin-top:14px;box-shadow:0 6px 18px rgba(0,0,0,.05)}
    h2{color:var(--accent);margin-top:0}
    ul{margin:8px 0 0 20px}
    .files a{display:inline-block;margin-right:10px;margin-top:6px;padding:9px 12px;border-radius:8px;background:#1f77b4;color:#fff;text-decoration:none}
    .files a.green{background:#28a745}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:18px}
    .gallery{display:flex;flex-direction:column;gap:10px;align-items:center}
    .gallery img{width:100%;max-width:520px;border-radius:8px;box-shadow:0 8px 20px rgba(0,0,0,.08);cursor:pointer}
    .small{color:var(--muted);font-size:14px}
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}
    @media(max-width:980px){.grid{grid-template-columns:1fr}.gallery img{max-width:100%}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>Superstore Profit Maximization Analysis</h1>
      <p>Project: Analyze sales, profit, and discounts (2014–2017) to improve profitability and inform business decisions.</p>
    </header>

    <section class="card">
      <h2>Project Overview</h2>
      <p>This project analyzes Superstore sales, profit, and discount data to identify patterns, improve profitability, and guide business decisions. Using four years of data (2014–2017), we examined product categories, regions, states, and discount strategies to uncover opportunities for growth and cost reduction.</p>
      <p><strong>Core question:</strong> How can the Superstore increase profit without relying solely on sales growth?</p>
    </section>

    <section class="card">
      <h2>Dataset Description</h2>
      <ul>
        <li><strong>Source:</strong> Sample Superstore dataset (2014–2017)</li>
        <li><strong>Rows:</strong> ~10,000</li>
        <li><strong>Key columns:</strong> Order Date, Ship Date, Ship Mode, Category, Sub-Category, Product Name, Sales, Profit, Discount, Quantity, Region, State, City</li>
      </ul>
    </section>

    <section class="card">
      <h2>Key Problem Identified — Discount Impact</h2>
      <ul>
        <li>After a <strong>0.2 (20%)</strong> discount there is no significant spike in sales.</li>
        <li>Profits turn negative at higher discounts; discounts above 20% increase losses without boosting sales.</li>
        <li><strong>Best strategy:</strong> Keep discounts ≤ 20%.</li>
      </ul>
      <p class="small"><strong>Trade-offs:</strong> Sales may slightly decrease, but profit will increase. There is risk of losing customers who buy only at deep discounts — plan retention actions.</p>
    </section>

    <section class="card">
      <h2>Loss-Making Sub-Categories</h2>
      <ul>
        <li><strong>Tables</strong> – Worst-performing, heavy losses every year.</li>
        <li><strong>Bookcases</strong> – Losses in some years.</li>
        <li><strong>Supplies</strong> – Low or negative profit.</li>
        <li><strong>Machines</strong> – Loss only in 2017.</li>
      </ul>
      <p class="small"><strong>Strategy:</strong> Reduce discounts for Tables & Machines to &lt;20% to try to recover profitability. For Bookcases & Supplies, consider discontinuation or new strategies (bundles, promotions), since lowering discount alone may not fix margins.</p>
    </section>

    <section class="card">
      <h2>Loss-Making States</h2>
      <ul>
        <li>Texas, Illinois, Pennsylvania show negative profit in multiple years.</li>
        <li>Texas currently gives ~40% discount but still loses money.</li>
      </ul>
      <p class="small">Action: Reduce discounts in these states to ~15–20% and monitor results — big discounts are not effective in these markets.</p>
    </section>

    <div class="grid">
      <div>
        <section class="card">
          <h2>Project Workflow</h2>
          <h3>1. Data Cleaning & Preparation</h3>
          <ul>
            <li>Remove duplicates & handle missing values</li>
            <li>Standardize categories & sub-categories</li>
            <li>Set correct data types for dates, numeric and categorical fields</li>
          </ul>

          <h3>2. Data Modeling</h3>
          <ul>
            <li>Created measures: Total Sales, Total Profit, Profit Margin %, Average Discount</li>
            <li>Added profitability flags to identify underperforming SKUs and regions</li>
          </ul>

          <h3>3. Dashboard Development</h3>
          <ul>
            <li>Interactive Power BI dashboards with slicers for Year, Region, State, Category, Sub-Category, Discount Range</li>
            <li>KPI cards for Total Sales, Total Profit and Average Profit Margin</li>
          </ul>
        </section>

        <section class="card">
          <h2>Key Visualizations</h2>
          <ul>
            <li>Profit by Region (map)</li>
            <li>Sales & Profit by Category (bar)</li>
            <li>Discount vs Profit (scatter) — optimal 0–20% range</li>
            <li>Loss-making sub-categories list</li>
            <li>State-level performance (highlight high-discount loss states)</li>
            <li>Yearly trends</li>
          </ul>
        </section>

        <section class="card">
          <h2>Recommendations</h2>
          <ul>
            <li>Keep discounts ≤ 20%; reduce excessive discounts in loss-making states.</li>
            <li>Remove or rework Tables; bundle or promote Bookcases & Supplies.</li>
            <li>Promote Machines with targeted campaigns and controlled discounts.</li>
            <li>Focus marketing in West & East regions; investigate Central region costs.</li>
          </ul>
        </section>

        <section class="card">
          <h2>Business Impact, Future Scope & Investment</h2>
          <ul>
            <li><strong>Impact:</strong> Estimated profit increase +12–18% annually with discount optimization and product changes.</li>
            <li><strong>Future scope:</strong> Predictive discount modeling, dynamic pricing, customer segmentation, supply chain optimization.</li>
            <li><strong>Investment needs:</strong> Power BI Pro, analytics tools, cloud storage, team training, data integration.</li>
          </ul>
        </section>
      </div>

      <aside>
        <section class="card">
          <h2>Files & Links</h2>
          <div class="files">
            <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Report.pdf" target="_blank">Open Report (PDF)</a><br>
            <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Presentation1.pdf" class="green" target="_blank">Open Presentation</a><br>
            <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Sample%20-%20Superstore.xlsx" target="_blank">Open Excel Data</a>
          </div>
        </section>

        <section class="card">
          <h2>Dashboard Preview</h2>
          <p class="small">Click image to open the full screenshot on GitHub.</p>
          <div class="gallery" style="align-items:center">
            <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223500.png" target="_blank">
              <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%25202025-08-08%2520223500.png" alt="Dashboard screenshot 1">
            </a>
            <a href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Screenshot%202025-08-08%20223417.png" target="_blank">
              <img src="https://raw.githubusercontent.com/Dhruva912005/Superstore-Data-analysis-and-Report/main/Screenshot%25202025-08-08%2520223417.png" alt="Dashboard screenshot 2">
            </a>
          </div>
        </section>
      </aside>
    </div>

    <section class="card">
      <h2>Full Report & Presentation</h2>
      <p>Open the full analysis and slides:</p>
      <a class="files" href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Report.pdf" target="_blank">Open Report</a>
      <a class="files" href="https://github.com/Dhruva912005/Superstore-Data-analysis-and-Report/blob/main/Presentation1.pdf" target="_blank">Open Presentation</a>
    </section>

    <footer>
      <p class="small">Prepared for: Superstore Profit Maximization Project — 2014–2017 • Created by Dhruva</p>
    </footer>
  </div>

  <script>
    // nothing fancy required; images link to GitHub raw URLs
  </script>
</body>
</html>
