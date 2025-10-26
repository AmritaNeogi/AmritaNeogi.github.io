---
layout: single
title:
permalink: /Projects/
date: 2023-09-02
categories: pages
toc: false
toc_label: "Projects"
toc_icon: "columns"
author_profile: false
sidebar: false
classes: wide
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280; --card:#ffffff;
    --line:#e5e7eb; --ring:rgba(51,102,153,0.12); --bg:#f8fafc;
  }

  /* ===== Hard override Minimal Mistakes shell on layout:single ===== */
  @media (min-width: 1024px){
    .layout--single .sidebar,
    .layout--single .page__sidebar{ display:none !important; }
    .layout--single .page{ display:block !important; max-width:none !important; width:100% !important; }
    .layout--single .page__inner-wrap{ padding-left:0 !important; padding-right:0 !important; }
    .layout--single .page__content{
      max-width:none !important;
      width:100% !important;
      margin:0 !important;
      padding:0 !important;
    }
  }

  /* ===== Page layout pinned LEFT with a small gutter (matching Experience) ===== */
  .projects-page{
    font-family:'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color:var(--ink);
    width:100%;
    padding-left: clamp(12px, 2vw, 24px);
    padding-right: clamp(12px, 2vw, 24px);
    box-sizing: border-box;
  }
  
  h1.section-title{ 
    color:var(--brand); 
    margin:.25rem 0 .5rem; 
    font-size:clamp(26px, 3.2vw, 34px); 
    font-weight: 800;
  }
  p.section-sub{ margin:0 0 .8rem; color:var(--muted); font-size:14.5px; }

  /* ===== Single-column list of cards (wider like Experience) ===== */
  .cards{
    display:grid; 
    gap:18px;
    grid-template-columns: 1fr;
    max-width:none; 
    width:min(1400px, 100%);  /* match Experience width */
  }

  /* ===== Card styles ===== */
  details.card{
    border:1px solid var(--line);
    border-radius:14px;
    background:var(--card);
    box-shadow:0 1px 0 var(--ring);
    overflow:hidden;
    margin:.8rem 0;
    width:100%;
  }
  
  .card > summary{
    list-style:none; cursor:pointer;
    display:flex; align-items:center; gap:12px; flex-wrap:wrap;
    padding:12px 16px; outline:none;
  }
  .card > summary::-webkit-details-marker{ display:none; }

  .pill{
    font-size:12px; font-weight:600;
    color:var(--brand); background:#eef3f8;
    padding:4px 10px; border-radius:999px;
    border:1px solid #dbe2ea; white-space:nowrap;
    flex-shrink: 0;
  }
  
  .title{ 
    font-weight:800; 
    font-size:16.5px; 
    color:var(--ink);
    flex: 1 1 auto;
    min-width: 0;
  }
  
  .meta{
    margin-left:auto; display:flex; gap:10px; align-items:center;
    color:var(--muted); font-size:13.5px;
    flex-shrink: 0;
    white-space:nowrap;
  }
  .meta .gh{
    text-decoration:none; border:1px solid var(--brand); color:var(--brand);
    padding:5px 8px; border-radius:8px; font-weight:600; font-size:13px;
  }
  .meta .gh:hover{ background:var(--brand); color:#fff; }

  /* ===== Inside each card ===== */
  .content{
    display:grid; 
    gap:16px;
    grid-template-columns: minmax(0,1fr) minmax(0,1fr);
    border-top:1px solid var(--line);
    padding:12px 16px 14px;
    font-size:15px; line-height:1.6;
    overflow-wrap:anywhere; 
    box-sizing:border-box; 
    width:100%;
  }
  @media (max-width: 860px){
    .content{ grid-template-columns: 1fr; }
  }

  .thumb{
    width:100%;
    aspect-ratio:16/9; 
    object-fit:cover;
    border-radius:10px; 
    border:1px solid var(--line); 
    background:var(--bg);
  }

  .bullets{ margin:.35rem 0 0; padding-left:18px; }
  .bullets li{ margin:.22rem 0; }
  .links{ display:flex; gap:10px; flex-wrap:wrap; margin-top:.6rem; }
  .btn{ 
    display:inline-block; 
    text-decoration:none; 
    font-weight:600;
    padding:7px 10px; 
    border-radius:9px; 
    font-size:14px; 
  }
  .btn.ghost{ border:1px solid var(--brand); color:var(--brand); }
  .btn.ghost:hover{ background:var(--brand); color:#fff; }

  .divider{ height:1px; background:var(--line); margin:1.2rem 0 .9rem; }
</style>

<div class="projects-page">

  <!-- ===================== PROJECTS ===================== -->
  <h1 class="section-title">Projects</h1>
  <p class="section-sub">Browse selected projects. Click a card to view a short summary, visuals, and links.</p>

  <div class="cards">

    <!-- GDPR / CCPA risk pipeline -->
    <details class="card" id="gdpr-pipeline">
      <summary>
        <span class="pill">Data Engineering · ML</span>
        <span class="title">Regulatory Risk Pipeline (Airflow · BigQuery · T5 · LSTM)</span>
        <span class="meta">
          <span>Jul&nbsp;2025</span>
          <a class="gh" href="https://github.com/AmritaNeogi/GDPR-CCPA-Risk-Pipeline-with-Airflow" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/gdpr_pic.png" alt="Regulatory risk ETL and ML pipeline">
        <div>
          Automated daily ingestion of GDPR/CCPA updates into a governed dataset with model-driven risk signals for compliance teams.
          <ul class="bullets">
            <li>Developed Airflow pipeline ingesting daily regulatory updates into BigQuery with data validation, audit logging, and lineage tracking.</li>
            <li>Fine-tuned T5 model to classify policy changes across multiple categories and built LSTM/Prophet models forecasting regulatory trends with under 15% error.</li>
            <li>Reduced manual monitoring effort by 75% through automated risk dashboards, experiment tracking, and CI/CD deployment with rollback capabilities.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/gdpr.png" target="_blank">Schema overview</a>
          </div>
          <div class="links">
            <a class="btn ghost" href="https://github.com/AmritaNeogi/GDPR-CCPA-Risk-Pipeline-with-Airflow" target="_blank" rel="noopener">Repository</a>
          </div>
        </div>
      </div>
    </details>

    <!-- Phenophase CV -->
    <details class="card" id="phenophase">
      <summary>
        <span class="pill">Computer Vision</span>
        <span class="title">Phenophase Image Analysis (ResNet-50 + GANs)</span>
        <span class="meta">
          <span>Dec&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/PhenoCam-Image-Analysis-Using-CNN" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/leaf.png" alt="Phenology project">
        <div>
          Built computer vision pipeline to classify plant leaf stages and forecast seasonal timing patterns across field sites.
          <ul class="bullets">
            <li>Trained deep learning model (ResNet-50) to classify leaf development phases, using data augmentation to address class imbalance.</li>
            <li>Validated model performance across multiple field sites to ensure predictions worked in different environmental conditions.</li>
            <li>Automated model evaluation and report generation to deliver results and performance metrics to research teams.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/SOS_EOS.png" target="_blank">SOS/EOS plot</a>
            <a class="btn ghost" href="/assets/images/GAN.png" target="_blank">GAN architecture</a>
          </div>
        </div>
      </div>
    </details>

    <!-- Airflow YouTube -->
    <details class="card" id="airflow-youtube">
      <summary>
        <span class="pill">Data Engineering</span>
        <span class="title">YouTube Data Pipeline with Apache Airflow</span>
        <span class="meta">
          <span>Oct&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/YouTube_Data_Pipieline_Using_Airflow" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/youTube_pic.png" alt="YouTube pipeline">
        <div>
          Developed automated pipeline to collect YouTube channel data and prepare it for business analytics.
          <ul class="bullets">
            <li>Built data extraction process from YouTube API with automated error handling and incremental updates to reduce processing time.</li>
            <li>Designed data loading system that prevented duplicates and maintained data quality through validation checks.</li>
            <li>Created structured data tables enabling content performance analysis and channel growth metrics for stakeholders.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/youtube.png" target="_blank">Pipeline overview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- Snowflake housing -->
    <details class="card" id="snowflake-housing">
      <summary>
        <span class="pill">Analytics</span>
        <span class="title">House Price Profiler on Snowflake</span>
        <span class="meta">
          <span>Oct&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Data_Analytics_Project-Housing_Price_Profiler" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/snowflake.png" alt="Housing profiler">
        <div>
          Cleaned and standardized 60,000+ Otodom listings to analyze pricing patterns and market drivers.
          <ul class="bullets">
            <li>Transformed nested JSON data into structured tables, improving query performance by 40% and enabling faster analysis.</li>
            <li>Enriched dataset with geocoding and engineered features to support price sensitivity and demand modeling.</li>
            <li>Delivered business insights through SQL analysis and visualizations answering key pricing and market questions.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/overview_house.png" target="_blank">Schema overview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- Uber analytics -->
    <details class="card" id="uber">
      <summary>
        <span class="pill">Data Engineering & Business Intelligence</span>
        <span class="title">Uber Data Analytics (GCS · Mage · BigQuery · Looker)</span>
        <span class="meta">
          <span>Aug&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Uber_data_Analytics" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/uber.png" alt="Uber analytics">
        <div>
          Built end-to-end data pipeline delivering ride-sharing demand and supply analytics through interactive dashboards.
          <ul class="bullets">
            <li>Designed optimized BigQuery tables with partitioning and clustering strategies enabling sub-second query performance.</li>
            <li>Created Looker Studio dashboard providing real-time visibility into demand patterns, supply gaps, and operational metrics.</li>
            <li>Delivered stakeholder-ready views tracking peak demand periods, driver availability, and incentive program effectiveness.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="https://lookerstudio.google.com/s/s-nnQQB79Kw" target="_blank" rel="noopener">Dashboard</a>
            <a class="btn ghost" href="/assets/images/uber_dashboard.jpg" target="_blank">Dashboard preview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- Salary regression -->
    <details class="card" id="salary">
      <summary>
        <span class="pill">Regression</span>
        <span class="title">Salary Prediction (Gradient Descent)</span>
        <span class="meta">
          <span>Jul&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Data-Science-Project-Salary-Prediction" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/salary.png" alt="Salary prediction">
        <div>
          Implemented and optimized gradient descent algorithm to predict housing prices with significant error reduction.
          <ul class="bullets">
            <li>Reduced prediction error from 91.2% to 6.3% through data scaling, feature selection, and learning rate optimization.</li>
            <li>Built diagnostic tools to visualize learning rate impact and monitor model convergence during training.</li>
            <li>Demonstrated systematic approach to model tuning with documented performance improvements at each optimization step.</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/summary1.png" target="_blank">Summary</a>
            <a class="btn ghost" href="/assets/images/gradient%20descent.png" target="_blank">GD visualization</a>
          </div>
        </div>
      </div>
    </details>

  </div><!-- /.cards -->

  <div class="divider"></div>

  <!-- ===================== RESEARCH ===================== -->
  <h1 class="section-title">Research</h1>
  <p class="section-sub">Work in progress from the ARID Lab at the University of Arizona. Click to view a brief, non-confidential summary.</p>

  <div class="cards">
    <details class="card" id="insurance-infant">
      <summary>
        <span class="pill">Causal Inference</span>
        <span class="title">Insurance at Birth & Infant Outcomes (EHR, multi-site)</span>
        <span class="meta"><span>Sep&nbsp;2025</span></span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/infant.png" alt="Insurance & infant outcomes">
        <div>
          Evaluated how payer type and care access influence infant survival using real-world multi-site EHR data and causal inference modeling.
          <ul class="bullets">
            <li>Built a large-scale cohort from CDC's CHD STAR surveillance system spanning 7 states, harmonizing EHR, claims, and vital statistics data with complex ICD-9/10 coding algorithms to classify 114K infants by CHD severity, insurance status, and 50+ clinical/demographic variables</li>
            <li>Applied multivariate logistic regression adjusting for confounders (CHD severity, socioeconomic status, geography, clinical factors) to reveal that uninsured infants had 2.65x increased odds of infant mortality (95% CI: 1.74-3.92, p < 0.001) compared to privately insured infants</li>
            <li>Identified critical disparities showing publicly insured infants had 11-21% increased odds of organ dysfunction morbidities (neurologic, respiratory, sepsis) despite similar survival, while uninsured infants exhibited paradoxical survival bias with highest mortality but lowest documented morbidity rates</li>
            </ul>
        <div class="links">
            <a class="btn ghost" href="/assets/images/mort_forest_plot.png" target="_blank" rel="noopener">Risk Factors (Forest Plot)</a>
            <a class="btn ghost" href="/assets/images/mort_morbidity_by_insurance.png" target="_blank" rel="noopener">Morbidity Patterns</a>
            <a class="btn ghost" href="/assets/images/mort_demographics_stacked.png" target="_blank" rel="noopener">Population Demographics</a>
            <a class="btn ghost" href="/assets/images/mort_rates_by_insurance.png" target="_blank" rel="noopener">Mortality Rates</a>
        </div>
        </div>
    </div>
    </details>

    <details class="card" id="utilization-guidelines">
    <summary>
        <span class="pill">Health Analytics</span>
        <span class="title">Healthcare Utilization &amp; Guideline Adherence</span>
        <span class="meta"><span>Aug&nbsp;2025</span></span>
    </summary>
    <div class="content">
        <!-- Main thumbnail (choose any of the four) -->
        <img class="thumb" src="/assets/images/hcu.png" alt="Guideline adherence by group">
        <div>
        Evaluated how closely patients with congenital heart disease received care aligned with AHA/ACC guidance, and which factors drove staying in care or returning after gaps.
        <ul class="bullets">
            <li>Built a 10-year, multi-site CHD cohort (50K+ records) harmonizing claims, encounters, and EHR data.</li>
            <li>Applied clustering and regression to identify utilization patterns and predictors of adherence.</li>
            <li>Delivered dashboards and policy briefs highlighting three care profiles and high-risk subgroups.</li>
        </ul>

        <!-- Plot links row (small buttons) -->
        <div class="links">
            <a class="btn ghost" href="/assets/images/hcu_adherence_by_group.png" target="_blank" rel="noopener">Adherence by Group</a>
            <a class="btn ghost" href="/assets/images/hcu_gap_hist.png" target="_blank" rel="noopener">Care Gaps</a>
            <a class="btn ghost" href="/assets/images/hcu_return_km.png" target="_blank" rel="noopener">Return-to-Care (KM)</a>
            <a class="btn ghost" href="/assets/images/hcu_feature_importance.png" target="_blank" rel="noopener">Predictors (OR)</a>
        </div>
        </div>
    </div>
    </details>

  </div><!-- /.cards -->

</div>
<head>
<style>
  /* Make ONLY the two research thumbnails fit nicely */
  #insurance-infant img.thumb,
  #utilization-guidelines img.thumb{
    width: 100%;
    aspect-ratio: 16 / 9;   /* consistent frame */
    height: auto;
    object-fit: contain;
    background: #f6f7fb; /* soft backdrop for letterbox space */
    padding: 8px;        /* optional */
    object-position: center; /* keep the center in view */
    border-radius: 12px;     /* optional: match your card style */
    display: block;
  }

  /* If any crop looks off-center, you can nudge it per-card:
  #insurance-infant img.thumb{ object-position: 40% 50%; }
  */
</style>
</head>

<script>
  // Keep only one card open per grid
  document.querySelectorAll('.cards').forEach((grid) => {
    grid.querySelectorAll('details.card').forEach((d) => {
      d.addEventListener('toggle', () => {
        if (d.open) grid.querySelectorAll('details.card').forEach(o => { if (o !== d) o.removeAttribute('open'); });
      });
    });
  });
</script>