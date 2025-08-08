<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8"/>
  <meta name="viewport" content="width=device-width,initial-scale=1"/>
  <title>Superstore Profit Maximization — Project</title>
  <style>
    :root{
      --accent:#175fa6;
      --muted:#6b7280;
      --card:#ffffff;
      --bg:#f4f6f8;
      --maxw:1100px;
      --radius:10px;
      --glass: rgba(255,255,255,0.8);
    }
    *{box-sizing:border-box}
    body{
      font-family: "Inter", "Segoe UI", Roboto, Arial, sans-serif;
      margin:0;
      background: linear-gradient(180deg,var(--bg),#eef2f6);
      color:#111827;
      -webkit-font-smoothing:antialiased;
    }
    .wrap{max-width:var(--maxw);margin:28px auto;padding:22px;}
    header{display:flex;gap:14px;align-items:center;margin-bottom:18px}
    .logo{width:64px;height:64px;border-radius:10px;background:var(--accent);display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700;font-size:20px;box-shadow:0 8px 30px rgba(23,95,166,.12)}
    h1{margin:0;font-size:20px}
    p.lead{color:var(--muted);margin:6px 0 0}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:18px;align-items:start}
    .card{background:var(--card);padding:16px;border-radius:var(--radius);box-shadow:0 8px 24px rgba(15,23,42,.04)}
    .section-title{font-weight:700;margin:0 0 8px 0;color:var(--accent)}
    ul{margin:8px 0 0 18px;color:#1f2937}
    .muted{color:var(--muted)}
    .gallery{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .gallery img{width:100%;height:180px;object-fit:cover;border-radius:8px;border:2px solid #eef2f6;cursor:pointer;transition:transform .12s}
    .gallery img:hover{transform:scale(1.02)}
    .btn{display:inline-block;padding:10px 12px;background:var(--accent);color:#fff;border-radius:8px;text-decoration:none;font-weight:600}
    .btn.green{background:#16a34a}
    .small{font-size:13px;color:var(--muted)}
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}
    .kpis{display:flex;gap:8px;flex-wrap:wrap}
    .kpi{background:#f8fafc;padding:10px;border-radius:8px;min-width:140px;text-align:center;box-shadow:inset 0 -1px 0 rgba(0,0,0,.02)}
    .kpi .val{font-size:18px;color:var(--accent);font-weight:700}
    /* modal */
    .modal{position:fixed;inset:0;background:rgba(0,0,0,.6);display:none;align-items:center;justify-content:center;z-index:9999}
    .modal .box{max-width:95%;max-height:95%;background:var(--card);padding:10px;border-radius:10px;box-shadow:0 24px 60px rgba(2,6,23,.5)}
    .modal img{max-width:100%;max-height:80vh;border-radius:6px;display:block}
    @media (max-width:980px){
      .grid{grid-template-columns:1fr}
      .gallery img{height:140px}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">SS</div>
      <div>
        <h1>Superstore Profit Maximization Analysis</h1>
        <p class="lead">Project analyzing sales, profit, and discounts (2014–2017). Goal: increase profit through data-driven actions.</p>
      </div>
    </header>

    <div class="grid">
      <!-- Main column -->
      <main>
        <section class="card">
          <div class="section-title">Project Overview</div>
          <p class="small muted">Core question: How can the Superstore increase profit without relying solely on sales growth?</p>

          <h3 style="margin-top:12px;margin-bottom:6px">Dataset</h3>
          <ul>
            <li>Source: Sample Superstore dataset (2014–2017)</li>
            <li>Rows: ~10,000</li>
            <li>Key columns: Order Date, Ship Date, Category, Sub-Category, Sales, Profit, Discount, Region, State</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Key Insights</div>
          <ul>
            <li>Profit is highest when discounts are <strong>≤ 20%</strong>. Higher discounts often cause losses.</li>
            <li><strong>Technology</strong> is the most profitable category; <strong>Furniture</strong> has strong sales but low profit.</li>
            <li>Loss-making sub-categories: <em>Tables, Bookcases, Labels, Fasteners, Machines</em>.</li>
            <li>West & East regions perform well; Central region shows good sales but low profit.</li>
            <li>Example state: <strong>Texas</strong> offers ~40% discount but remains loss-making — reduce discount to ~15–20%.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Recommendations</div>
          <ul>
            <li>Cap discounts at <strong>≤ 20%</strong> and reduce high discounts in loss-making states.</li>
            <li>Discontinue or rework persistent loss-makers (e.g., Tables).</li>
            <li>Use bundling and seasonal promotions for Bookcases and Labels.</li>
            <li>Promote Machines with targeted offers instead of blanket high discounts.</li>
            <li>Focus marketing and expansion on West & East regions.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Project Workflow</div>
          <h4 style="margin:8px 0 4px 0">1. Data Cleaning & Preparation</h4>
          <ul>
            <li>Removed duplicates and handled missing values.</li>
            <li>Standardized category and sub-category names.</li>
            <li>Set correct data types for dates and numeric fields.</li>
          </ul>

          <h4 style="margin:8px 0 4px 0">2. Data Modeling</h4>
          <ul>
            <li>Created measures: Total Sales, Total Profit, Profit Margin %, Average Discount.</li>
            <li>Added profitability flags to spot loss-makers quickly.</li>
          </ul>

          <h4 style="margin:8px 0 4px 0">3. Dashboard Development</h4>
          <ul>
            <li>Built Power BI visuals with slicers for Year, Region, State, Category, Sub-Category, Discount Range.</li>
            <li>Included KPI cards for quick monitoring.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Key Visuals</div>
          <ul>
            <li>Profit by Region (map)</li>
            <li>Sales & Profit by Category (bar)</li>
            <li>Discount vs Profit (scatter)</li>
            <li>Loss-Making Sub-Categories (highlight)</li>
            <li>State-Level Performance (table / chart)</li>
            <li>Yearly Trends (line)</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Dashboard Preview</div>
          <p class="small muted">Click any image to enlarge.</p>
          <div class="gallery" id="gallery">
            <img src="Screenshot 2025-08-08 223417.png" alt="Dashboard 1" data-full="Screenshot 2025-08-08 223417.png">
            <img src="Screenshot 2025-08-08 223250.png" alt="Dashboard 2" data-full="Screenshot 2025-08-08 223250.png">
            <img src="Screenshot 2025-08-08 223142.png" alt="Dashboard 3" data-full="Screenshot 2025-08-08 223142.png">
            <img src="Screenshot 2025-08-08 223500.png" alt="Dashboard 4" data-full="Screenshot 2025-08-08 223500.png">
          </div>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Business Impact</div>
          <ul>
            <li>Estimated profit improvement: <strong>12–18% annually</strong> after discount optimization and product changes.</li>
            <li>Better customer retention by offering targeted offers instead of blanket deep discounts.</li>
            <li>Inventory freed from loss-making items can be reallocated to high-margin products.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Future Scope</div>
          <ul>
            <li>Predictive discount modeling per product/region (ML).</li>
            <li>Dynamic pricing based on demand and competition.</li>
            <li>Customer segmentation for personalized offers.</li>
            <li>Supply chain optimization to reduce costs in loss-making regions.</li>
          </ul>
        </section>

        <section class="card" style="margin-top:14px">
          <div class="section-title">Investment Needs</div>
          <ul>
            <li>Power BI Pro and analytics tools.</li>
            <li>Training for teams to use dashboards and act on insights.</li>
            <li>Integration of POS, CRM, and inventory for near real-time analytics.</li>
            <li>Marketing budget for targeted campaigns in profitable regions.</li>
          </ul>
        </section>

      </main>

      <!-- Right column -->
      <aside>
        <div class="card">
          <div class="section-title">Quick Links & Files</div>
          <p class="small muted">Open or download full documents</p>
          <div style="margin-top:8px;display:flex;flex-direction:column;gap:8px">
            <a class="btn" href="Report.pdf" download>Download Full Report (PDF)</a>
            <a class="btn green" href="Presentation1.pdf" download>Download Presentation</a>
          </div>
        </div>

        <div class="card" style="margin-top:14px">
          <div class="section-title">KPIs (example)</div>
          <div style="margin-top:10px" class="kpis">
            <div class="kpi"><div class="small">Average Discount</div><div class="val">0.16</div></div>
            <div class="kpi"><div class="small">Sum of Sales</div><div class="val">2.30M</div></div>
            <div class="kpi"><div class="small">Sum of Profit</div><div class="val">286.4K</div></div>
          </div>
        </div>

        <div class="card" style="margin-top:14px">
          <div class="section-title">Preview Report</div>
          <iframe src="Report.pdf" style="width:100%;height:220px;border-radius:8px;border:none;margin-top:10px"></iframe>
        </div>
      </aside>
    </div>

    <footer>
      <div class="small muted">Prepared for: Superstore Profit Maximization Project • Data period: 2014–2017</div>
    </footer>
  </div>

  <!-- Modal for large image -->
  <div id="modal" class="modal" onclick="closeModal()">
    <div class="box" onclick="event.stopPropagation()">
      <img id="modalImg" src="" alt="preview">
      <div style="text-align:right;margin-top:8px">
        <a id="openFull" class="btn" href="#" target="_blank" style="background:#333;padding:8px 10px">Open full image</a>
      </div>
    </div>
  </div>

  <script>
    // Open image in modal
    document.querySelectorAll('.gallery img').forEach(img=>{
      img.addEventListener('click', ()=>{
        const full = img.getAttribute('data-full') || img.src;
        document.getElementById('modalImg').src = full;
        document.getElementById('openFull').href = full;
        document.getElementById('modal').style.display = 'flex';
      });
    });
    function closeModal(){ document.getElementById('modal').style.display = 'none'; }
    // hide iframe if can't load
    document.querySelectorAll('iframe').forEach(f=>{
      f.onerror = ()=>f.style.display='none';
    });
  </script>
</body>
</html>
