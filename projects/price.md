---
layout: default

permalink: /projects/price/
---


<style>
/* ── RESET & BASE  */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --navy:        #042338;
  --navy-mid:    #1E3A5F;
  --navy-light:  #2A4A7F;
  --white:       #FFFFFF;
  --off-white:   #F8FAFC;
  --slate:       #64748B;
  --slate-light: #CBD5E1;
  --coral:       #FF6B35;
  --emerald:     #10B981;
  --red:         #EF4444;
  --amber:       #F59E0B;
  --text-dark:   #0F172A;
}

html { scroll-behavior: smooth; }

body {
  font-family: Georgia, 'Times New Roman', serif !important;
  background: var(--off-white);
  color: var(--text-dark);
  line-height: 1.7;
}

/* ---------- */
.container { max-width: 1100px; margin: 0 auto; padding: 0 32px; }
/* .mono { font-family: 'JetBrains Mono', 'Courier New', monospace; } */
.section-eyebrow {
  font-size: 1.2rem;
  font-weight:700;
  text-transform: uppercase;
  color: var(--coral);
  margin-bottom: 10px;
  display: block;
}

/* Nav*/
nav {
  /* position: sticky; */
  top: 0;
  z-index: 100;
  /* background: rgba(10, 15, 30, 0.96); */
  backdrop-filter: blur(8px);
  border-bottom: 1px solid rgba(255,255,255,0.08);
  padding: 14px 0;
}
.nav-inner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 2px;
  display: flex;
  align-items: center;
  gap: 32px;
  flex-wrap: wrap;
}
.nav-brand {
  font-family: system-ui, sans-serif;
  font-weight: 800;
  font-size: 0.9rem;
  color: var(--white);
  text-decoration: none;
  letter-spacing: -0.01em;
  margin-right: auto;
}
nav a.nav-link {
  font-family: system-ui, sans-serif;
  font-size: 0.82rem;
  color: var(--slate-light);
  text-decoration: none;
  letter-spacing: 0.02em;
  transition: color 0.2s;
}
nav a.nav-link:hover { color: var(--coral); }
.back-btn {
  font-family: system-ui, sans-serif;
  font-size: 0.82rem;
  font-weight: 700;
  background: var(--coral);
  color: var(--white);
  padding: 7px 16px;
  border-radius: 6px;
  text-decoration: none;
  transition: opacity 0.2s;
}
.back-btn:hover { opacity: 0.88; }

/*HERO */
.hero {
  background:#37332f;
  /* background-image:
    linear-gradient(to bottom, rgba(10,15,30,0.55) 0%, rgba(10,15,30,0.88) 60%, rgba(10,15,30,1) 100%),
    url('dashboard-overview.png'); */
  background-size: cover;
  background-position: center top;
  padding: 32px 0 32px;
  border-bottom: 1px solid rgba(255,255,255,0.06);
}
.hero-inner { max-width: 1100px; margin: 0 auto; padding: 0 32px; text-align:center; }
.hero-tag {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255,107,53,0.15);
  border: 1px solid rgba(255,107,53,0.35);
  border-radius: 100px;
  padding: 5px 14px;
  font-family: system-ui, sans-serif;
  font-size: 0.78rem;
  font-weight: 600;
  color: var(--coral);
  letter-spacing: 0.06em;
  text-transform: uppercase;
  margin-bottom: 24px;
}
.hero-tag::before { content: ''; width: 7px; height: 7px; border-radius: 50%; background: var(--coral); }
.hero h1 {
  font-family: system-ui, -apple-system, sans-serif;
  font-size: clamp(2.2rem, 5vw, 2.6rem);
  font-weight: 900;
  color: var(--white);
  letter-spacing: -0.03em;
  line-height: 1.08;
  margin-bottom: 20px;
}
.hero h1 em {
  font-style: normal;
  color: var(--coral);
}
.hero-lead {
  font-size: 1.12rem;
  color: rgba(255,255,255,0.72);
  /* max-width: 640px; */
  margin-bottom: 36px;
  line-height: 1.65;
}
.hero-tech {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  justify-content:center;
}
.tech-pill {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.75rem;
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.14);
  color: rgba(255,255,255,0.75);
  padding: 5px 12px;
  border-radius: 4px;
}

/*  SECTION */
.section-light { background: var(--white); padding: 16px 0; }
.section-dark  { background: var(--navy);  padding: 16px 0; }
.section-off   { background: var(--off-white); padding: 16px 0; }

.section-title {
  font-family: system-ui, sans-serif;
  font-size: 1.75rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color: var(--text-dark);
  margin-bottom: 6px !important;
  margin-top:1rem!important;
}
.section-title-white {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--white);
  margin-bottom: 16px;
}
.section-body {
  font-size: 1.02rem;
  color: #374151;
  /* max-width: 760px; */
  margin-bottom: 24px;
}
.section-body-white {
  font-size: 1.02rem;
  color: rgba(255,255,255,0.72);
  /* max-width: 760px; */
  margin-bottom: 24px;
}

/*  KPI */
.kpi-rail {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 16px;
  margin: 24px 0;
}
.kpi-card {
  background: var(--white);
  border: 1px solid #E5E7EB;
  border-radius: 12px;
  padding: 22px 24px;
  display: flex;
  flex-direction: column;
  gap: 6px;
  transition: box-shadow 0.2s;
}
.kpi-card:hover { box-shadow: 0 4px 20px rgba(0,0,0,0.07); }
.kpi-label {
  font-family: system-ui, sans-serif;
  font-size: 0.78rem;
  font-weight: 600;
  color: var(--slate);
  text-transform: uppercase;
  letter-spacing: 0.06em;
}
.kpi-value {
  font-family: system-ui, sans-serif;
  font-size: 1.5rem;
  font-weight: 900;
  color: var(--text-dark);
  letter-spacing: -0.03em;
  line-height: 1;
}
.kpi-value.accent { color: var(--coral); }
.kpi-sub {
  font-size: 0.8rem;
  color: var(--slate);
  font-family: system-ui, sans-serif;
}

.scale-bar-wrap { margin: 32px 0; }
.scale-label {
  font-family: system-ui, sans-serif;
  font-size: 0.82rem;
  font-weight: 600;
  color: var(--slate);
  margin-bottom: 6px;
}
.scale-row {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 10px;
}
.scale-name {
  font-family: system-ui, sans-serif;
  font-size: 0.82rem;
  color: var(--text-dark);
  width: 160px;
  flex-shrink: 0;
}
.scale-bar {
  height: 10px;
  border-radius: 100px;
  transition: width 0.4s ease;
}
.scale-count {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.78rem;
  color: var(--slate);
}

.findings-grid {
  /* display: grid; */
  /* grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); */
  gap: 20px;
  padding:24px;
}
.finding-card {
  background: var(--white);
  border-radius: 4px;
  border: 1px solid #E5E7EB;
  padding: 24px 24px 24px 22px;
  margin-bottom:12px;
}

.finding-title {
  font-family: system-ui, sans-serif;
  font-size: 1rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 8px;
}
.finding-body {
  font-size: 0.92rem;
  color: #4B5563;
  line-height: 1.6;
}
.finding-stat {
  margin-top: 12px;
  font-family: system-ui, sans-serif;
  font-size: 1.4rem;
  font-weight: 900;
  letter-spacing: -0.02em;
}



.hosp-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 16px;
  margin: 28px 0;
}
.hosp-card {
  background: #e5e5e5;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 22px 24px;
}
.hosp-name {
  font-family: system-ui, sans-serif;
  font-size: 1rem;
  font-weight: 800;
  color: #333;
  margin-bottom: 4px;
}
.hosp-detail {
  font-family: system-ui, sans-serif;
  font-size: 0.82rem;
  color: rgba(0,0,0,0.8);
  margin-bottom: 14px;
}
.hosp-stat-row { display: flex; gap: 20px; flex-wrap: wrap; }
.hosp-stat { display: flex; flex-direction: column; gap: 2px; }
.hosp-stat-val {
  font-family: system-ui, sans-serif;
  font-weight: 800;
  font-size: 1.3rem;
  /* color: var(--coral); */
  letter-spacing: -0.02em;
}
.hosp-stat-lbl {
  font-family: system-ui, sans-serif;
  font-size: 0.72rem;
  color: #333;
  text-transform: uppercase;
  letter-spacing: 0.06em;
}
.hosp-format-pill {
  display: inline-block;
  margin-top: 12px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.7rem;
  padding: 3px 9px;
  border-radius: 4px;
  background: rgba(255,255,255,0.08);
  color: #333;
}


.bq-list { list-style: none; padding: 0; margin: 24px 0; display: flex; flex-direction: column; gap: 12px; }
.bq-item {
  display: flex;
  gap: 14px;
  align-items: flex-start;
  background: var(--white);
  border: 1px solid #E5E7EB;
  border-radius: 8px;
  padding: 16px 18px;
}
.bq-num {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--coral);
  min-width: 28px;
  padding-top: 1px;
}
.bq-text {
  font-size: 0.95rem;
  color: var(--text-dark);
  line-height: 1.55;
}

/* ── MODEL IMAGE ──────────────────────────────────── */
.img-frame {
  border: 1px solid #E5E7EB;
  border-radius: 10px;
  overflow: hidden;
  margin: 28px 0;
  box-shadow: 0 4px 24px rgba(0,0,0,0.07);
}
.img-frame img { display: block; width: 100%; height: auto; margin-bottom:0!important }
.img-caption {
  font-family: system-ui, sans-serif;
  font-size: 0.78rem;
  color: var(--slate);
  text-align: center;
  padding: 10px;
  background: var(--off-white);
  border-top: 1px solid #E5E7EB;
}



.schema-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 14px;
  margin: 28px 0;
}
.schema-card {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 8px;
  padding: 18px;
}
.schema-card.fact {
  border-color: rgba(255,107,53,0.4);
  background: rgba(255,107,53,0.06);
}
.schema-table-name {
  font-family: system-ui, sans-serif;
  font-size: 0.8rem;
  font-weight: 800;
  color: var(--white);
  margin-bottom: 10px;
  padding-bottom: 8px;
  border-bottom: 1px solid rgba(255,255,255,0.08);
}
.schema-card.fact .schema-table-name { color: var(--coral); }
.schema-col {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.72rem;
  color: rgba(255,255,255,0.55);
  padding: 3px 0;
  display: flex;
  gap: 8px;
  align-items: center;
}
.schema-col-tag {
  font-size: 0.62rem;
  font-weight: 700;
  padding: 1px 5px;
  border-radius: 3px;
  min-width: 24px;
  text-align: center;
}
.pk { background: rgba(16,185,129,0.2); color: #10B981; }
.fk { background: rgba(245,158,11,0.2); color: #F59E0B; }
.m  { background: rgba(255,107,53,0.2); color: var(--coral); }

.proc-cloud { display: flex; flex-wrap: wrap; gap: 8px; margin: 20px 0; }
.proc-tag {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.75rem;
  background: var(--white);
  border: 1px solid #E5E7EB;
  color: var(--slate);
  padding: 5px 11px;
  border-radius: 5px;
}


footer {
  border-top: 1px solid rgba(255,255,255,0.06);
  text-align: left;
}
footer p {
  font-family: system-ui, sans-serif;
  font-size: 0.85rem;
  color: rgba(0, 0, 0, 0.35);
}
footer a {
  color: var(--coral);
  text-decoration: none;
  font-weight: 600;
}
/* .footer-back {
  display: inline-block;
  margin-bottom: 20px;
  font-family: system-ui, sans-serif;
  font-size: 0.85rem;
  font-weight: 700;
  background: var(--coral);
  color: var(--white);
  padding: 10px 22px;
  border-radius: 6px;
  text-decoration: none;
} */

/* ── RESPONSIVE ───────────────────────────────────── */
@media (max-width: 640px) {
  .container { padding: 0 20px; }
  .hero { padding: 80px 0 60px; }
  .nav-link { display: none; }
  .kpi-rail { grid-template-columns: repeat(2, 1fr); }
}
</style>
<nav>
  <div class="nav-inner">
    <a class="back-btn" href="/">← Back to Home</a>
  </div>
</nav>

<body>
<header class="hero" id="overview">
  <div class="hero-inner">
    <h1>Price Transparency<br>in <em>Healthcare</em></h1>
    <p class="hero-lead">
      Analyzing 6K rows by filtering out from 7.2 million raw hospital pricing records across three Louisville, Kentucky hospitals to expose negotiation gaps and payer disparities.
    </p>
    <div class="hero-tech">
      <span class="tech-pill">Python</span>
      <span class="tech-pill">pandas</span>
      <span class="tech-pill">Power BI</span>
      <span class="tech-pill">DAX</span>
      <span class="tech-pill">Star Schema</span>
      <span class="tech-pill">CMS Price Transparency</span>
    </div>
   
  </div>
</header>

<!-- CONTEXT -->
<section class="section-light" id="context">
  <div class="container">
    <p style="text-align:right; font-size:14px; padding-right:8px margin:0px">Check out: <a class="footer-back" href="https://github.com/laxmiadh08/Healthcare-Price-Transparency"  target="_blank">Github</a></p>
  
    <span class="section-eyebrow">Background</span>
  
    <p class="section-body">
  <i>Since 2021, the CMS Hospital Price Transparency Rule requires every U.S. hospital to publish machine-readable files disclosing their gross charges, cash prices, and payer-negotiated rates. In practice, these files arrive in incompatible formats, somewith hundreds of payer columns, others long with one row per payer, making cross-hospital comparison difficult.</i>
    </p>
    <p class="section-body">
   The original hospital pricing files contained 7,230,075 records combined for three hospitals. For this analysis, the data was narrowed to 49 high-impact healthcare procedures spanning inpatient, outpatient, emergency, laboratory, and pharmacy services, resulting in a curated dataset of approximately 6,681 records optimized for cross-hospital price comparisons.
    </p>

<!-- KPI RAIL -->
    <div class="kpi-rail">
      <div class="kpi-card">
        <span class="kpi-label">CPT Procedures</span>
        <span class="kpi-value">48</span>

      </div>
      <div class="kpi-card">
        <span class="kpi-label">Unique Payers</span>
        <span class="kpi-value">46</span>
        
      </div>
     
      <div class="kpi-card">
        <span class="kpi-label">Max Price Spread</span>
        <span class="kpi-value ">$122K</span>
      </div>
      <div class="kpi-card">
        <span class="kpi-label">Cash vs Min Rate</span>
        <span class="kpi-value ">$1.8K</span>
      </div>
    </div>
  </div>
</section>

<!-- HOSPITALS -->
<section class="section-off" id="data">
  <div class="container">
    <span class="section-eyebrow" style="color:var(--coral)">Data Sources</span>
    <p class="section-body-off">
      Data was collected from publicly available CMS Hospital Price Transparency files. Each hospital publishes a different file structure, which was a challenge to clean and process these files to create a final clean dataset.
  
  </p>
    <p class="section-body-off" style="margin-top:24px; font-size:0.92rem;">
      Challange: UofL's file used a wide format with one column per payer (379 total), requiring a melt operation to convert 97 rows into 1,940 long-format rows. Norton and Baptist used long format. I used LLM to format these files and consolidate into 13 columns for this analysis.
    </p>
  <p style="text-align:right; font-size:14px; padding-right:8px margin:0px">Check out code here: <a class="footer-back" href="https://github.com/laxmiadh08/Healthcare-Price-Transparency"  target="_blank">Github</a></p>
 <div class="hosp-grid">
      <div class="hosp-card">
        <div class="hosp-name">University of Louisville Health</div>
        <div class="hosp-detail">Louisville, KY</div>
        <div class="hosp-stat-row">
          <div class="hosp-stat">
            <span class="hosp-stat-val">379</span>
            <span class="hosp-stat-lbl">Columns</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">4,423</span>
            <span class="hosp-stat-lbl">Output rows</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">40</span>
            <span class="hosp-stat-lbl">Payer contracts</span>
          </div>
        </div>
     
</div>
      <div class="hosp-card">
        <div class="hosp-name">Baptist Health</div>
        <div class="hosp-detail">Louisville, KY </div>
        <div class="hosp-stat-row">
          <div class="hosp-stat">
            <span class="hosp-stat-val">28</span>
            <span class="hosp-stat-lbl">Columns</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">420</span>
            <span class="hosp-stat-lbl">Output rows</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">28</span>
            <span class="hosp-stat-lbl">Payer contracts</span>
          </div>
        </div>
      
</div>
      <div class="hosp-card">
        <div class="hosp-name">Norton Hospital</div>
        <div class="hosp-detail">Louisville, KY</div>
        <div class="hosp-stat-row">
          <div class="hosp-stat">
            <span class="hosp-stat-val">30</span>
            <span class="hosp-stat-lbl">Columns</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">1,838</span>
            <span class="hosp-stat-lbl">Output rows</span>
          </div>
          <div class="hosp-stat">
            <span class="hosp-stat-val">13</span>
            <span class="hosp-stat-lbl">Payer contracts</span>
          </div>
        </div>
      </div>
    </div>

 
  </div>
</section>

<!-- BUSINESS QUESTIONS -->
<section class="section-off" id="questions">
  <div class="container">
    <span class="section-eyebrow">Analysis</span>
    <h2 class="section-title">Business Questions:</h2>

   <ul class="bq-list">
      <li class="bq-item">
        <span class="bq-text">Which hospital charges the highest gross charge for the same CPT code and how does their negotiated rate compare to competitors?</span>
      </li>
      <li class="bq-item">
        <span class="bq-text">For which procedures does the negotiated rate exceed the gross charge and which payers and hospitals are involved?</span>
      </li>
      <li class="bq-item">
        <span class="bq-text">Which payer consistently negotiates the lowest rates, and which plan type gets the deepest discount?</span>
      </li>
      <li class="bq-item">
        <span class="bq-text">How does the cash price compare to the minimum negotiated rate are uninsured patients paying more than the best-insured patients?</span>
      </li>
      <li class="bq-item">
        <span class="bq-text">Which procedures show the widest min-to-max negotiated rate spread?</span>
      </li>
      <li class="bq-item">
        <span class="bq-text">How complete is each hospital's gross charge disclosure and does incomplete disclosure correlate with higher negotiated rates?</span>
      </li>
    </ul>
  </div>
</section>

<!-- DATA MODEL -->
<section class="section-off" id="model">
  <div class="container">
    <span class="section-eyebrow" style="color:var(--coral)">Data Model</span>
    <h3 style="margin-top:16px; font-weight:700">Star Schema Design </h3>
   
<div class="img-frame" style="margin-top:28px;">
 <img src="/images/price-transparency/data-model.png?raw=true"
        alt="Hospital Comparison"
        class="project-image"/>
        <!-- <div class="img-caption">Data Model</div> -->
        </div>
  </div>
</section>

<!-- KEY FINDINGS -->
<section class="section-light" id="findings">
  <div class="container">
    <span class="section-eyebrow">Analysis: Key Findings</span>


  <div class="finding-card insight">
        <div class="finding-title">Cash Patients Pay $1,800 More Than Best Payer Rate</div>
        <div class="finding-body">
          On average, the minimum payer-negotiated rate across all procedures is $1,800 lower than the cash price charged to uninsured patients. For the highest-cost procedures, this gap widens dramatically, uninsured patients face not the gross charge sticker price, but a cash price that still substantially exceeds what even the most expensive insurer pays.
        </div>
        <div class="finding-stat">$1,800 avg premium for uninsured</div>
      </div>
  
   <h2 style="margin-top:16px;margin-bottom:0px; font-weight:700">Price Transparency Gap </h2>
    <div class="img-frame" style="margin-top:8px;">
        <img src="/images/price-transparency/price-gap.png?raw=true"
        alt="Hospital Comparison"
        class="project-image"/>
    </div>
    
  <div class="img-frame" style="margin-top:8px;">
            <img src="/images/price-transparency/comparison-price-gap.png?raw=true"
            alt="Hospital Comparison"
            class="project-image"/>
    </div>
           
  <h2 style="margin-top:28px;margin-bottom:0px; font-weight:700">25 Most expensive procedures by hospital </h2>
<div class="img-frame" style="margin-top:8px;">
        <img src="/images/price-transparency/expensive-gross.png?raw=true"
        alt="Hospital Comparison"
        class="project-image"/>
        </div>

  <h2 style="margin-top:28px;margin-bottom:0px; font-weight:700">Gross charge and Average Negotiated Rates overview </h2>
    <div class="img-frame" style="margin-top:8px;">
            <img src="/images/price-transparency/3_comparison.png?raw=true"
            alt="Hospital Comparison"
            class="project-image"/>
            </div> 
    <div class="findings-grid">
      <div class="finding-card flag">
        <div class="finding-title">CPT 871: Negotiated Rate Exceeds Gross Charge</div>
        <div class="finding-body">
          At Baptist Health, CPT 871 shows a gross charge of $61,621 with a negotiated rate of $23,961, sitting visibly above the diagonal reference line. This means the contracted payer rate exceeds the hospital's own listed price, representing a direct financial loss.
        </div>
        <div class="finding-stat">$61,621 → $23,961 above line</div>
      </div>
      <div class="finding-card insight">
        <div class="finding-title">Norton Hospital:Minimal Payer Discounts</div>
        <div class="finding-body">
          Norton Hospital's procedures (CPT codes 291, 292, 193, 310, 603, 872) cluster tightly along the diagonal reference line across the $10K–$40K gross charge range. Payers are achieving minimal discounts off Norton's list price.
        </div>
        
   </div>
      
  <div class="finding-card good">
        <div class="finding-title">CPT 470:74% Discount on Joint Replacement</div>
        <div class="finding-body">
          CPT 470 (Major Joint Replacement - hip/knee) at Baptist Health shows the deepest payer discount in the dataset. With a gross charge of $122,570 and an average negotiated rate of $31,844, payers achieved approximately a 74% reduction from list price.
        </div>
        <div class="finding-stat">74% below gross charge</div>
      </div>
       

        

  <div class="finding-card warning">
        <div class="finding-title">18% Gross Charge Non-Disclosure at Norton &amp; UofL</div>
        <div class="finding-body">
          Baptist Health disclosed gross charges for 100% of procedure rows. Norton Hospital disclosed 83.24% and UofL Health 82.16%, leaving approximately 1 in 6 rows without a gross charge.
        </div>
        <div class="finding-stat">Baptist 100% · Norton 83% · UofL 82%</div>
      </div>

      
 

<div class="finding-card flag">
        <div class="finding-title">CPT 470 Skews All Hospital-Level Averages</div>
        <div class="finding-body">
          Baptist Health's average negotiated rate of $15K is nearly 8× UofL's $1K average. However, this comparison is misleading — the hospitals bill for fundamentally different procedure mixes. CPT 470's $31,844 rate alone pulls Baptist's average dramatically upward. 
        </div>
        <div class="finding-stat">Mean $7,740 · Median $1,284</div>
      </div>
    </div>
  </div>
</section>

<!-- DAX MEASURES -->
<section class="section-off" id="dax">
  <div class="container">
    <span class="section-eyebrow">Technical Detail</span>
    <h2 class="section-title">Key DAX Measures</h2>

<div class="code-block">
      <div class="code-block-header">Average Negotiated Rate</div>
<pre>
Avg Negotiated Rate = AVERAGE(Fact_Prices[negotiated_rate])
</pre>
</div>
<!--  -->
<div class="code-block">
      <div class="code-block-header">Median Negotiated Rate</div>
<pre>
Median Negotiated Rate = CALCULATE(MEDIAN(Fact_Prices[negotiated_rate]))
</pre>
</div>
<!--  -->
<div class="code-block">
      <div class="code-block-header">Gross Charge Coverage</div>
<pre>
Gross Charge Coverage = 
DIVIDE(
    CALCULATE(COUNTROWS(Fact_Prices), NOT ISBLANK(Fact_Prices[gross_charge])),
    COUNTROWS(Fact_Prices),
    0
)
</pre>
</div>

<!--  -->


<!--  -->
<div class="code-block">
      <div class="code-block-header">Cash vs Min Negotiated</div>
<pre>
Cash vs Min Negotiated = AVERAGE(Fact_Prices[cash_price]) - AVERAGE(Fact_Prices[min_negotiated])
</pre>
</div>
<!--  -->
<div class="code-block">
      <div class="code-block-header">Discount % off Gross  </div>
<pre>
Discount % off Gross = 1 - DIVIDE([Avg Negotiated Rate],[Avg Gross Charge])
</pre>
</div>
<!--  -->
<div class="code-block">
      <div class="code-block-header">Price Spread</div>
<pre>
Price Spread = AVERAGE(Fact_Prices[max_negotiated]) - AVERAGE(Fact_Prices[min_negotiated])
</pre>
</div>

<!--  -->
<div class="code-block">
      <div class="code-block-header">Max Price Spread</div>
<pre>
Max Price Spread = MAX(Fact_Prices[max_negotiated]) - MIN(Fact_Prices[min_negotiated])
</pre>
</div>
<!--  -->
</div>

</section>

<!-- PROCEDURES -->
<section class="section-light" id="procedures">
  <div class="container">
    <span class="section-eyebrow">Scope</span>
    <h2 class="section-title">Procedures Included in Analysis</h2>
    <p class="section-body">
      48 CPT codes were selected spanning emergency, surgical, imaging, laboratory, and inpatient services — chosen to enable meaningful cross-hospital comparison where the same standardized code appears at more than one hospital.
    </p>
    <div class="proc-cloud">
      <span class="proc-tag">99285 · ED Visit</span>
      <span class="proc-tag">470 · Knee Replacement</span>
      <span class="proc-tag">29827 · Shoulder Arthroscopy</span>
      <span class="proc-tag">45378 · Colonoscopy</span>
      <span class="proc-tag">45385 · Colonoscopy w/ Polypectomy</span>
      <span class="proc-tag">43239 · Upper GI Endoscopy</span>
      <span class="proc-tag">29881 · Knee Meniscectomy</span>
      <span class="proc-tag">76830 · Pelvic Ultrasound</span>
      <span class="proc-tag">93306 · Echo w/ Doppler</span>
      <span class="proc-tag">93451 · Right Heart Cath</span>
      <span class="proc-tag">72148 · MRI Lumbar</span>
      <span class="proc-tag">73721 · MRI Knee</span>
      <span class="proc-tag">73221 · MRI Shoulder</span>
      <span class="proc-tag">74177 · CT Abdomen &amp; Pelvis</span>
      <span class="proc-tag">74160 · CT Abdomen</span>
      <span class="proc-tag">72193 · CT Pelvis</span>
      <span class="proc-tag">871 · Complex Cardiac Procedure</span>
      <span class="proc-tag">872 · Cardiac Support</span>
      <span class="proc-tag">291 · Inpatient Psych</span>
      <span class="proc-tag">292 · Detox</span>
      <span class="proc-tag">310 · Medical Rehab</span>
      <span class="proc-tag">392 · Bone Marrow Transplant</span>
      <span class="proc-tag">690 · Kidney Procedure</span>
      <span class="proc-tag">641 · Misc Surgery</span>
      <span class="proc-tag">603 · Radiation Therapy</span>
      <span class="proc-tag">+ 23 additional CPT codes</span>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <a class="footer-back" href="/">← Return to Portfolio</a>
  <p>Data sourced from CMS Hospital Price Transparency Rule (45 CFR Part 180) · Public domain hospital pricing files</p>
  <!-- <p style="margin-top:8px;">Built with Python · pandas · Power BI · DAX</p> -->
</footer>

 
