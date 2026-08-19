---
layout: default
permalink: /projects/ihd-ky1/
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
    margin-bottom: 2.5rem;
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
    margin: 0!important;
    /* max-width: 34ch; */
  }

  .masthead__meta {
    font-size: var(--size-caption);
    color: var(--color-muted);
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
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
    padding: 1.1rem 1.4rem;
    margin: 0 0 1.5rem;
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
    color: var(--color-primary);
    font-size: var(--size-caption);
    text-transform: uppercase;
    letter-spacing: 0.03em;
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
    <p class="placeholder">[Executive summary content goes here.]</p>
  </section>

  <!-- BACKGROUND AND OVERVIEW ================================= -->
  <section id="background">
    <div class="section__header">
      <!-- <span class="section__index">02</span> -->
      <h2 class="section__title">Background and Overview</h2>
    </div>
    <p class="placeholder">[Background content goes here.]</p>
  </section>

  <!-- DATA STRUCTURE OVERVIEW ================================= -->
  <section id="data-structure">
    <div class="section__header">
      <!-- <span class="section__index">03</span> -->
      <h2 class="section__title">Data Structure Overview</h2>
    </div>
    <p class="placeholder">[Data structure overview goes here — table styling below is ready to use.]</p>

    <table>
      <thead>
        <tr><th>Attribute</th><th>Detail</th></tr>
      </thead>
      <tbody>
        <tr><td class="placeholder">[Field]</td><td class="placeholder">[Value]</td></tr>
        <tr><td class="placeholder">[Field]</td><td class="placeholder">[Value]</td></tr>
      </tbody>
    </table>
  </section>

  <!-- INSIGHTS AND DEEP DIVE =================================== -->
  <section id="insights">
    <div class="section__header">
      <span class="section__index">04</span>
      <h2 class="section__title">Insights &amp; Deep Dive</h2>
    </div>

    <div class="callout placeholder">
      what is this
    </div>

    <h3>[Subsection heading]</h3>
    <p class="placeholder">[Subsection content goes here.]</p>

    <ul>
      <li class="placeholder">[Bullet point placeholder]</li>
      <li class="placeholder">[Bullet point placeholder]</li>
      <li class="placeholder">[Bullet point placeholder]</li>
    </ul>

    <div class="figure">
      <div class="figure__frame">[Chart / image placeholder]</div>
      <p class="figure__caption placeholder">[Figure caption goes here.]</p>
    </div>
  </section>

  <!-- RECOMMENDATIONS ========================================== -->
  <section id="recommendations">
    <div class="section__header">
      <span class="section__index">05</span>
      <h2 class="section__title">Recommendations</h2>
    </div>
    <ol>
      <li class="placeholder">[Recommendation placeholder]</li>
      <li class="placeholder">[Recommendation placeholder]</li>
    </ol>
  </section>

  <!-- CAVEATS AND ASSUMPTIONS ================================== -->
  <section id="caveats">
    <div class="section__header">
      <span class="section__index">06</span>
      <h2 class="section__title">Caveats &amp; Assumptions</h2>
    </div>
    <ul>
      <li class="placeholder">[Caveat placeholder]</li>
      <li class="placeholder">[Caveat placeholder]</li>
    </ul>
  </section>
  </main>
<body>
  <!-- FOOTER ==================================================== -->
  <footer class="page__footer">
    <p class="placeholder">[Source citations / prepared-by line goes here.]</p>
  </footer>





<nav>
  <div class="nav-inner">
    <a class="back-btn" href="/">← Back to Home</a>
  </div>
</nav>