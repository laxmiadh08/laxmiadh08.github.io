---
layout: default
permalink: /
---

<style>
/*  DESIGN TOKENS (matches detail page) ─ */
:root {
  --navy:        #0A0F1E;
  --navy-mid:    #1E3A5F;
  --white:       #FFFFFF;
  --off-white:   #F8FAFC;
  --slate:       #64748B;
  --slate-light: #CBD5E1;
  --coral:       #FF6B35;
  --emerald:     #10B981;
  --text-dark:   #333333;
  --border:      #E5E7EB;
}

/*  RESET & BASE ─*/
*, *::before, *::after { box-sizing: border-box; }

body {
  font-family: Georgia, 'Times New Roman', serif ;
  background: var(--off-white);
  color: var(--text-dark);
  line-height: 1.7;
}

/*  HERO / INTRO ─*/
.home-hero {
  background: #fff;
  padding: 16px 0px;
  margin-bottom: 0;
  /* border:1px solid #d8d8d8; */
}
.project-name{
  display:none!important;
}

.home-hero-inner {
  /* max-width: 860px; */
  margin: 0 auto;
}

.home-eyebrow {
  font-size: .85rem;
  text-transform: uppercase;
  color: var(--coral);
  display: block;
  margin-bottom: 8px;
}

.home-name {
  font-family: system-ui, -apple-system, sans-serif !important;
  font-size: clamp(2.4rem, 6vw, 2.8rem) !important;
  font-weight: 900!important;
  color: var(--navy) !important;
  letter-spacing: -0.03em;
  line-height: 1.05;
  margin: 0 0 16px 0 !important;
}


.home-about {
  font-size: 1rem;
  color:#767676;
  line-height: 1.52;
  margin: 0 0 4px 0;
}

.home-tech-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  display:none;

}

.tech-pill {
  font-family: 'JetBrains Mono', 'Courier New', monospace;
  font-size: 0.73rem;
  background: rgb(249, 227, 205);
  border: 1px solid rgb(255, 167, 45);
  color: rgba(0, 0, 0, 0.65);
  padding: 5px 12px;
  border-radius: 4px;
}

/*  SECTION WRAPPER */
.home-section {
  max-width: 1100px;
  margin: 0 auto;
  padding: 24px 0px;
}

.section-title{
  font-size: 1.5rem;
  color:#333;
  font-weight:600;
  margin-bottom: 10px;
}

.section-title {
  font-size: 1.75rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color:#767676!important;
  margin: 0 0 32px 0;
}

/*  PROJECT GRID ─*/
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
  gap: 20px;
}
.project-card-link {
  display: inline-flex;
  align-items: center;
  gap: 5px;
  font-family: system-ui, -apple-system, sans-serif;
  font-size: 0.82rem;
  font-weight: 700;
  color: var(--coral);
  text-decoration: none!important;
  margin-top: 10px;
  transition: gap 0.15s;
}

.project-card-link:hover { gap: 8px; }

.project-card {
  background: var(--off-white);
  border: 1px solid #f7e9dc;
  border-left: 3px solid var(--coral);
  border-radius: 4px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: box-shadow 0.2s, transform 0.2s;
  text-decoration: none;
  color: inherit;
}

.project-card:hover {
  box-shadow: 0 8px 28px rgba(0,0,0,0.09);
  transform: translateY(-3px);
}

.project-card img {
  padding:8px;
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
  margin-bottom:4px !important;
}

.project-card-body {
  display: flex;
  flex-direction: column;
  flex: 1;
  gap: 8px;
  padding:4px 12px
}

.project-card-title {
  font-size: 1.5rem;
  font-weight: 700!important;
  color: #333333 !important;
  margin: 0 !important;
}

.project-card-desc {
  font-size: 0.9rem;
  color: #706c6c !important;
  line-height: 1.2;
  margin: 0;
  flex: 1;
  font-weight:400!important;
}

.project-card-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: 4px;
}

.tag {
  font-family: 'JetBrains Mono', 'Courier New', monospace;
  font-size: 0.68rem;
  background: var(--off-white);
  border: 1px solid var(--border);
  color: var(--text-dark);
  padding: 3px 9px;
  border-radius: 4px;
}



/*  EDUCATION */
.edu-section {
  background: var(--white);
  padding: 0;
}

.edu-inner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0px;
}

.edu-card {
  border: 1px solid rgb(114, 114, 114);
  /* border-left: 3px solid var(--coral); */
  border-radius: 10px;
  padding: 24px 28px;
  display: flex;
  align-items: flex-start;
  gap: 20px;
}

.edu-icon {
  font-size: 1.6rem;
  line-height: 1;
  flex-shrink: 0;
  margin-top: 2px;
}

.edu-degree {
  font-size: 1.05rem;
  font-weight: 800;
  color:#333;
  margin: 0px !important;
}

.edu-school {
  font-size: 1rem;
  color: #333;
  font-family: system-ui, sans-serif;
  margin: 0;
}

.edu-expected {
  display: inline-block;
  margin-top: 8px;
  font-size: 0.68rem;
  padding: 2px 9px;
  border-radius: 4px;
  background: #ffeae3;
  color: var(--coral);
  border: 1px solid #fd6106;
}

/*  CONNECT */
.connect-section {
  max-width: 1100px;
  margin: 0 auto;
  padding: 64px 32px 72px;
}

.connect-row {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-top: 10px;
  justify-content:end;
  
}

.connect-btn {
  font-family: system-ui, -apple-system, sans-serif;
  font-size: 0.88rem;
  font-weight: 700;
  padding: 6px 16px;
  border-radius: 7px;
  text-decoration: none;
  transition: opacity 0.18s, transform 0.18s;
  display: inline-flex;
  align-items: center;
  gap: 7px;
}

.connect-btn:hover {
  opacity: 0.88;
  transform: translateY(-1px);
}

.connect-btn.primary {
  background: var(--coral);
  color: var(--white);
}
  .connect-btn.primary-blue {
  background:#0e76a8;
  color: var(--white);
}

.connect-btn.secondary {
  background: var(--white);
  color: var(--text-dark);
  border: 1px solid var(--border);
}

/*  DIVIDER */
.divider {
  border: none;
  border-top: 1px solid var(--border);
  margin: 0;
}

/*  RESPONSIVE ─*/
@media (max-width: 600px) {
  .home-hero { padding: 60px 20px 52px; }
  .home-section, .edu-inner, .connect-section { padding-left: 20px; padding-right: 20px; }
  .project-grid { grid-template-columns: 1fr; }
  @media screen and (min-width: 64em) {
    .project-name {
        font-size: 0!important;
        display:none !important;

  }
}
}
</style>

<!--  HERO -->
<div class="home-hero">
  <div class="home-hero-inner">
    <span class="home-eyebrow">Data Analyst · Louisville, KY</span>
    <h1 class="home-name">Laxmi Adhikari </h1>
    <p class="home-about">
      I enjoy making sense of complex information and finding patterns. My background in business analysis, UX design, and business analytics has shaped a structured and detail-oriented approach to problem solving. Outside of analytics, hiking is my favorite way to disconnect and recharge.
    </p>

  <div class="connect-row">
    <a class="connect-btn primary-blue" href="https://www.linkedin.com/in/laxmiadh/" target="_blank">
      LinkedIn
    </a>
    <a class="connect-btn secondary" href="https://github.com/laxmiadh08" target="_blank">
      GitHub
    </a>
     <a class="connect-btn primary" href="/assets/Resume/Adhikari_Laxmi_Resume.pdf" target="_blank">
      Resume 
    </a>
  </div>
  
    <div class="home-tech-stack">
      <span class="tech-pill">Python</span>
      <span class="tech-pill">Power BI</span>
      <span class="tech-pill">DAX</span>
      <span class="tech-pill">SQL</span>
      <span class="tech-pill">Data Modeling</span>
      <span class="tech-pill">Star Schema</span>
      <span class="tech-pill">Excel</span>
    </div>
    
  </div>
</div>

<!--  PROJECTS ─-->
<div class="home-section">
  <span class="section-title">Featured Projects</span>
  <div class="project-grid">

    <!-- Project 1 — Healthcare Pricing -->


<a href="/projects/price" class="project-card-link">
  <div class="project-card">
    <!-- <img src="/images/price-transparency/thumb1.png" alt="Healthcare Pricing Dashboard"> -->

  <div class="project-card-body">
      <h3 class="project-card-title">Healthcare Pricing Disparities</h3>

   <p class="project-card-desc">
        Analyzed negotiated rates, cash prices, and gross charges across 3 major Louisville hospitals — uncovering payer negotiation gaps, and transparency failures.
      </p>

   <div class="project-card-tags">
        <span class="tag">Power BI</span>
        <span class="tag">Python</span>
        <span class="tag">Star Schema</span>
        <span class="tag">DAX</span>
      </div>
    <span class="project-card-view">
        View Project →
      </span>
    </div>
  </div>
</a>
 <a class="project-card-link" href="/projects/cdc">
    <!-- Project 2 — CDC Heart Disease -->
    <div class="project-card">
      <!-- <img src="/images/cdc/cdc-thumb.png" alt="Heart Disease Mortality Analysis"> -->
      <div class="project-card-body">
        <h3 class="project-card-title">County-Level Heart Disease Mortality</h3>
        <p class="project-card-desc">
          Analyzed county-level heart disease mortality disparities across Kentucky to identify high-burden regions and surface geographic patterns in public health outcomes.
        </p>
        <div class="project-card-tags">
          <span class="tag">Excel</span>
          <span class="tag">Datawrapper</span>
        </div>
       <span class="project-card-view">
        View Project →
      </span>
      </div>
    </div>
</a>
    <!-- Project 3 — placeholder -->
 <a class="project-card-link" href="https://github.com/laxmiadh08/Environment-Monitoring-App" target="_blank">
     <div class="project-card">
      <!-- <img src="/images/cdc/cdc-thumb.png" alt="Heart Disease Mortality Analysis"> -->
      <div class="project-card-body">
        <h3 class="project-card-title">Environmental Health Monitoring App</h3>
        <p class="project-card-desc">
        Built an end-to-end ETL pipeline for an environmental health app, integrating live weather and air quality data with health risk insights.
        </p>
        <div class="project-card-tags">
          <span class="tag">Python</span>
          <span class="tag">PostgreSQL</span>
           <span class="tag">Supabase</span>
        </div>
       <span class="project-card-view">
        View Project →
      </span>
      </div>
    </div>
</a>

  </div>
</div>

<!--  EDUCATION -->
<div class="edu-section">
  <div class="edu-inner">
    <h2 class="section-title" style=" margin-bottom:14px;">Education</h2>
    <div class="edu-card">
      <div class="edu-icon">🎓</div>
      <div>
        <p class="edu-degree">Master of Science in Business Analytics</p>
        <p class="edu-school">University of Louisville · Louisville, KY</p>
        <span class="edu-expected">Expected July 2026</span>
      </div>
    </div>
  </div>
</div>

<!--  CONNECT -->
<div class="connect-section">
  <span class="section-title">Contact</span>
  <!-- <h2 class="section-title">Let's Connect</h2> -->
  <div class="connect-row">
    <a class="connect-btn primary-blue" href="https://www.linkedin.com/in/laxmiadh/" target="_blank">
      LinkedIn
    </a>
    <a class="connect-btn secondary" href="https://github.com/laxmiadh08" target="_blank">
      GitHub
    </a>
     <a class="connect-btn secondary" href="/assets/Resume/Adhikari_Laxmi_Resume.pdf" target="_blank">
      Resume 
    </a>
  </div>
</div>
