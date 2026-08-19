---
layout: default
permalink: /projects/ihd-ky/
---

<style>

  /* ============================================================
     DESIGN TOKENS
     ============================================================ */
  :root {
    /* Color */
    --color-bg:        #FAFAF8;   /* paper white */
    --color-surface:   #F2F1EC;   /* slightly recessed panel */
    --color-ink:       #1A1D1F;   /* primary text, near-black */
    --color-primary:   #1F4B5C;   /* deep teal-navy — headers, structure */
    --color-secondary: #8A6A3B;   /* muted ochre — emphasis, markers */
    --color-muted:     #6B7280;   /* slate gray — subtitle, captions */
    --color-line:      #DADDD9;   /* hairline dividers */

    /* Type */
     --font-display: 'Fraunces', Georgia, serif;
    --font-body:     'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    /* Scale */
    --size-title:     2.75rem;
    --size-subtitle:  1.25rem;
    --size-h2:        1.05rem;
    --size-body:      1.0625rem;
    --size-caption:   0.875rem;

    /* Layout */
    --content-width: 720px;
    --space-section: 4rem;
  }

  /* ============================================================
     RESET / BASE
     ============================================================ */
  * { box-sizing: border-box; }

  html { -webkit-font-smoothing: antialiased; scroll-behavior: smooth; }

  body {
    margin: 0;
    /* background: var(--color-bg); */
    color: var(--color-ink);
    font-family: var(--font-body);
    font-size: var(--size-body);
    line-height: 1.65;
  }

  a { color: var(--color-primary); }
  a:focus-visible,
  button:focus-visible { outline: 2px solid var(--color-secondary); outline-offset: 3px; }


  /* ============================================================
     PAGE FRAME
     ============================================================ */
  .page {
    max-width: var(--content-width);
    margin: 0 auto;
    padding: 1rem 2rem;
  }

  /* ============================================================
     MASTHEAD — title + subtitle
     ============================================================ */
  .masthead {
    margin-bottom: 2rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid var(--color-line);
  }

  .masthead__eyebrow {
    font-family: var(--font-body);
    font-size: var(--size-caption);
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--color-secondary);
    margin: 0 0 1rem;
  }

  .masthead__title {
    font-family: var(--font-display);
    font-weight: 500;
    font-size: var(--size-title);
    line-height: 1.12;
    letter-spacing: -0.01em;
    color: var(--color-primary);
    margin: 0 0 0.85rem;
  }

  .masthead__subtitle {
    font-family: var(--font-display);
    font-style: italic;
    font-weight: 400;
    font-size: var(--size-subtitle);
    line-height: 1.5;
    color: var(--color-muted);
    margin: 0 0 1.5rem;
    /* max-width: 34ch; */
  }

  .masthead__meta {
    font-size: var(--size-caption);
    color: var(--color-muted);
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrapš
  }

  .masthead__meta span { white-space: nowrap; }

  /* ============================================================
     SECTIONS — Executive Summary, Background, etc.
     ============================================================ */
  section {
    margin-bottom: var(--space-section);
  }

  .section__header {
    display: flex;
    align-items: baseline;
    gap: 0.85rem;
    margin-bottom: .5rem;
    padding-bottom: 0.75rem;
  
  }

  .section__index {
    font-family: var(--font-body);
    font-size: var(--size-caption);
    font-weight: 600;
    color: var(--color-secondary);
    letter-spacing: 0.04em;
    flex-shrink: 0;
  }

  .section__title {
    font-family: var(--font-body);
    font-weight: 700!important;
    font-size: 1.5rem;
    letter-spacing: 0.02em;
    text-transform: uppercase;
    color: var(--color-primary);
    margin: 0!important;
  }

  /* Optional sub-heads within a section (e.g. "Regional Contrast") */
  .section h3 {
    font-family: var(--font-body);
    font-weight: 600;
    font-size: 1rem;
    color: var(--color-ink);
    margin: 1.75rem 0 0.75rem;
  }

  /* ============================================================
     BODY TEXT — paragraphs, bullets, callouts
     ============================================================ */
  section p {
    margin: 0 0 1.1rem;
    color: var(--color-ink);
  }

  section p.placeholder,
  section li.placeholder {
    color: var(--color-muted);
    font-style: italic;
  }
.text{
    color: #2d3037;
}
.mb-1{
    margin-bottom:.5rem!important;
}
  section ul,
  section ol {
    margin: 0 0 1.25rem;
    padding-left: 1.4rem;
  }

  section li {
    margin-bottom: 0.55rem;
    padding-left: 0.3rem;
  }

  section ul li::marker {
    color: var(--color-secondary);
  }

  section strong {
    font-weight: 600;
    color: var(--color-primary);
  }

  /* Callout / stat highlight block — for a pulled figure or key stat */
  .callout {
    background: var(--color-surface);
    border-left: 3px solid #FF6B35;
    padding: 1rem;
    margin: 0 0 .5rem;
    font-size: 0.98rem;
    color: var(--color-ink);
  }

  /* Simple data table shell, matched to the same palette */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 0 0 1.5rem;
    font-size: 0.95rem;
  }

  th, td {
    text-align: left;
    padding: 0.6rem 0.8rem;
    border-bottom: 1px solid var(--color-line);
  }

  th {
    font-weight: 600;

    font-size: var(--size-caption);
    text-transform: uppercase;
    letter-spacing: 0.03em;
    background: #0F919B;
    color: white;
  }

  /* Figure / chart placeholder */
  .figure {
    margin: 1.5rem 0 2rem;
  }

  .figure__frame {
    background: var(--color-surface);
    border: 1px dashed var(--color-line);
    aspect-ratio: 16 / 9;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--color-muted);
    font-size: var(--size-caption);
    text-align: center;
    padding: 1rem;
  }

  .figure__caption {
    font-size: var(--size-caption);
    color: var(--color-muted);
    margin-top: 0.6rem;
  }

  /* ============================================================
     FOOTER
     ============================================================ */
  .page__footer {
    margin-top: var(--space-section);
    padding-top: 1.5rem;
    border-top: 1px solid var(--color-line);
    font-size: var(--size-caption);
    color: var(--color-muted);
  }
  .back-btn{
    font-size:13px;
  }
.link{
    font-size:14px
}
  /* ============================================================
     RESPONSIVE
     ============================================================ */
  @media (max-width: 640px) {
    :root {
      --size-title: 2rem;
      --size-subtitle: 1.05rem;
      --space-section: 3rem;
    }
    .page { padding: 3rem 1.25rem 5rem; }
  }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
  }

</style>

<body>

<nav>
  <div class="nav-inner">
    <a class="back-btn" href="/">← Back to Home</a>
  </div>
</nav>
<main class="page">

  <!-- MASTHEAD ================================================ -->
  <header class="masthead">
    <p class="masthead__eyebrow"><!-- e.g. Policy Brief --></p>
    <h1 class="masthead__title">How Economic Hardship Fuels Kentucky’s Highest Heart Disease Death Rate</h1>
    <p class="masthead__subtitle">A County-Level Analysis of Ischemic Heart Disease Mortality in Kentucky</p>
    <div class="masthead__meta">
      <span><!-- Prepared for --></span>
      <span><!-- Date --></span>
      <span><!-- Data source --></span>
    </div>
  </header>

  <!-- EXECUTIVE SUMMARY ======================================= -->
  <section id="executive-summary">
    <div class="section__header">
      <!-- <span class="section__index">01</span> -->
      <h2 class="section__title">Executive Summary</h2>
    </div>
    <p class="text">
    Heart disease remains one of Kentucky’s deadliest challenges, but statewide averages mask a profound regional divide. An analysis of CDC mortality data from 2019 through 2024 reveals a statewide average of 125.8 deaths per 100,000 residents, already well above the national benchmark. Yet this burden is heavily concentrated in Eastern Kentucky, in Breathitt County, the rate surges to 369.9, roughly triple the state average and 2.5 times the national rate.
   
 </p>

<p class="text mb-1"> The data reveals that local economic conditions, serves as the primary driver of these outcomes:</p>

      <ul>
      <li class="text">Household income dictates risk: Counties where the bottom 20% of households earn the lowest incomes experience the highest mortality rates across the state.
      </li>
      <li class="text"> Local income inequality widens the gap: Communities with the largest divides between high and low earners suffer significantly worse cardiovascular outcomes.
      </li>
      <li class="text">Clinical headcount alone does not lower mortality: Counties with similar primary care physician counts span the entire spectrum of outcomes, showing that provider density alone has virtually no correlation with death rates.
      </li>
    </ul>

 <p class="text">
    Because healthcare access alone cannot close this gap, lowering heart disease deaths will require targeted economic support and preventive care in Kentucky’s most financially distressed communities.
    </p>
    <div class="figure">
    <div class="figure__frame">
    <img src="/images/ihd/comparison.png" alt="State vs nation " />
    </div>
    <p class="figure__caption placeholder">Heart Disease Mortality:Kentucky vs National Trends </p>
</div>
  </section>

  <!-- BACKGROUND AND OVERVIEW ================================= -->
  <section id="background">
    <div class="section__header">
      <!-- <span class="section__index">02</span> -->
      <h2 class="section__title">Background and Overview</h2>
    </div>
    <p class="text">Heart disease remains the leading cause of death in the United States, and Kentucky consistently ranks among the states with the highest cardiovascular mortality nationally. However, state-level rankings obscure substantial within-state variation. Rural Appalachian counties in Eastern Kentucky report mortality rates more than double national figures, while several urban and suburban counties perform on par with or better than national benchmarks.
This report examines county-level ischemic heart disease mortality across Kentucky to:
</p>
<ul>
<li class='text'> Quantify the scale of geographic disparity within the state.</li>
<li class='text'> Identify the regions and counties bearing the greatest burden. </li>
<li class='text'> Provide a data-driven basis for targeted public health policy and resource allocation.</li>
</ul>
  </section>

  <!-- DATA STRUCTURE OVERVIEW ================================= -->
  <section id="data-structure">
    <div class="section__header">
      <!-- <span class="section__index">03</span> -->
      <h2 class="section__title">Data Structure Overview</h2>
    </div>
    <!-- <p class="placeholder">[Data structure overview goes here — table styling below is ready to use.]</p> -->

<table>
<thead>
<tr><th>Attribute</th><th>Detail</th></tr>
</thead>
<tbody>
<tr><td class="placeholder">Mortality Source</td><td class="placeholder">CDC WONDER, Underlying Cause of Death (ICD-10 codes I20–I25), 2019–2024</td></tr>
<tr><td class="placeholder">Socioeconomic Source</td><td class="placeholder">County Health Rankings 2025</td></tr>
<tr><td class="placeholder">Geographic Scope</td><td class="placeholder">All 120 Kentucky counties</td></tr>
<tr><td class="placeholder">Primary Metric</td><td class="placeholder">Crude ischemic heart disease mortality rate per 100,000</td></tr>
<tr><td class="placeholder">Socioeconomic Variables</td><td class="placeholder">20th percentile household income, primary care physician (PCP) rate per 100,000</td></tr>
<tr><td class="placeholder">Join Key</td> <td class="placeholder">County FIPS code (all 120 counties matched across sources)</td></tr>


<tr><td class="placeholder">Suppression Status</td><td class="placeholder">All 120 Kentucky counties met the CDC WONDER reporting threshold of >=10 deaths, yielding complete county-level data with 0% suppression</td></tr>
</tbody>
</table>

</section>

  <!-- INSIGHTS AND DEEP DIVE =================================== -->
  <section id="insights">
    <div class="section__header">
      <!-- <span class="section__index">04</span> -->
      <h2 class="section__title">Insights &amp; Deep Dive</h2>
    </div>

  


<ul>
    <li class="text"><b>Statewide Performance:</b> Kentucky's pooled crude mortality rate stands at 125.8 per 100,000 residents, confirming cardiovascular disease as a statewide public health priority that is heavily elevated by regional pockets of extreme risk.</li>
    <li class="text"><b>The Appalachian Burden:</b> Eastern Kentucky counties including Breathitt, Perry, Bell, Wolfe, and Whitley report mortality rates between 300 and 370 per 100,000. Breathitt County records the state's highest rate at 369.9 deaths per 100,000.</li>
<div class="callout placeholder"><b>Eastern KY (Appalachia):</b> Highest burden statewide (300–370 deaths per 100k)</div>
<div class="callout placeholder"> <b>Central KY:</b> Moderate burden, tracking near the statewide average</div>
<div class="callout placeholder"><b> Western KY:</b> Mixed outcomes with isolated high-burden counties</div>
<div class="callout placeholder"><b>Urban / Suburban (Jefferson, Fayette, Shelby, Madison):</b> Lowest burden statewide (down to 41.0 deaths per 100k)</div>

<li class="text"><b>Geographic Disparities Across the State:</b> A statewide choropleth map reveals a consistent east-to-west mortality divide, demonstrating that the disease burden is geographically concentrated rather than randomly distributed.</li>

<div class="figure">
    <div class="figure__frame">
    <img src="/images/ihd/map.png" alt="Choropleth map of Kentucky" />
    </div>
    <p class="figure__caption placeholder">County-level choropleth map illustrating the geographic concentration of heart disease deaths across Kentucky.</p>
</div>
<li class="text"><b>Magnitude of Disparity: </b> The spread between the highest-burden county (Breathitt, 369.9 per 100k) and the lowest-burden county (Madison, 41.0 per 100k) represents a ninefold difference within the state.
</li>
<div class="figure">
    <div class="figure__frame">
    <img src="/images/ihd/top10.png" alt="top-10" />
    </div>
    <p class="figure__caption placeholder">Top 10 Kentucky Counties with the Highest Crude Heart Disease Mortality Rates</p>
</div>
<li class="text"><b>Income as the Primary Risk Factor: </b>Counties where the bottom 20% of households earn the least experience substantially higher crude mortality rates. As the 20th percentile income rises from roughly $12,000 to over $50,000, death rates fall from over 250 per 100,000 down to under 100 per 100,000. Nearly all counties with death rates above 200 per 100,000 have bottom-tier incomes below $25,000.
</li>

<div class="figure">
    <div class="figure__frame">
    <img src="/images/ihd/scatter-income.png" alt="statistical link between poverty and mortality  " />
    </div>
    <p class="figure__caption placeholder">Scatter plot comparing county-level heart disease mortality against local poverty rates  </p>
</div>

<li class="text"><b>Physician Count Shows No Meaningful Impact:</b>  Primary care provider availability shows virtually no relationship with county death rates. Counties with similar numbers of physicians experience completely different mortality outcomes, demonstrating that clinical capacity alone does not offset local economic distress.	</li>
</ul>
<div class="figure">
    <div class="figure__frame">
    <img src="/images/ihd/scatter-ph.png" alt="statistical link between poverty and mortality  " />
    </div>
    <p class="figure__caption placeholder">Scatter plot comparing county-level heart disease mortality against primary care physician availability </p>
</div>
  </section>

  <!-- RECOMMENDATIONS ========================================== -->
  <section id="recommendations">
    <div class="section__header">
      <!-- <span class="section__index">05</span> -->
      <h2 class="section__title">Recommendations</h2>
    </div>
    <ol>
       <li class="text"><b>Target economic investment where need is greatest:</b> Prioritize funding and economic development in high-risk, lower-income counties like Breathitt, Perry, Bell, Wolfe, and Whitley instead of distributing resources evenly statewide. Because household income predicts heart disease mortality far more than doctor availability, strengthening local economies in these hardest-hit areas will save more lives per dollar than clinic expansion alone.</li>
     <li class="text">  <b>Address internal inequality and upstream health risks:</b>Focus local economic policies on narrowing the wage divide between high and low earners within each county, while funding grassroots prevention for core risk factors like hypertension, smoking, and diabetes.</li>
   <li class="text">  <b> Pair practical healthcare access with economic support:</b> Continue investing in practical rural tools like mobile screenings and virtual cardiology, ensuring these clinical services are tied directly to local economic aid rather than relied upon as standalone fixes.</li>
      <li class="text">  <b> Unite regional leadership and track long-term progress:</b> Convene state health officials, regional development groups, economic planners, and local care providers into a single task force, supported by an annual public dashboard that tracks whether closing the economic gap reduces heart disease deaths over time. </li>
  
    </ol>
  </section>

  <!-- CAVEATS AND ASSUMPTIONS ================================== -->
<section id="caveats">
<div class="section__header">
    <!-- <span class="section__index">06</span> -->
    <h2 class="section__title">Caveats &amp; Assumptions</h2>
</div>
    <ul>
    <li class="text"><b>Differences in local age structure:</b> These figures reflect crude mortality rates rather than age-adjusted rates. Because Eastern Kentucky counties tend to have older populations, elevated rates may partly reflect an older demographic rather than health risks alone.
    </li>
    <li class="text"><b>Small county population swings: </b>  In counties with small populations, even minor fluctuations in annual deaths can produce visible percentage shifts. Combining seven years of data smooths out annual variance, but localized numbers should still be interpreted with care.
    </li>
    <!-- <li class="text"><b>Data completeness: </b> While CDC WONDER suppresses county records with fewer than 10 deaths, all 120 Kentucky counties recorded enough cases over the 2019–2024 aggregation period to avoid suppression.
    </li> -->
    <li class="text"><b>Correlation, not direct cause:</b> A strong statistical link between poverty and mortality demonstrates a clear pattern, but does not prove direct causation on its own.
    </li>
    <li class="text"><b>Multi-year aggregated view: </b> This analysis evaluates a six-year aggregated window to provide statistical stability, presenting an overall baseline rather than year-over-year directional shifts.
    </li>
</ul>

 
</section>
 <ul>
     <p class=""><b>Sources</b></p>
    <li class="link">  <a class="" href="https://wonder.cdc.gov/" target="_blank">
      CDC WONDER ↗
    </a>
    </li>
     <li class="link">  <a class="" href="https://www.countyhealthrankings.org/" target="_blank">
     County health ranking ↗
    </a>
    </li>
    </ul> 
</main>
<body>
  <!-- FOOTER ==================================================== -->

 <nav>
  <div class="nav-inner">
    <a class="back-btn" href="/">← Back to Home</a>
  </div>
</nav>






