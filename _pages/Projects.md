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
        <img class="thumb" src="/assets/images/gdpr.png" alt="Regulatory risk ETL and ML pipeline">
        <div>
          Automated daily ingestion of GDPR/CCPA updates into a governed dataset with model-driven risk signals for compliance teams.
          <ul class="bullets">
            <li>Airflow → BigQuery ETL with data standards, lineage, audit logs, validation gates</li>
            <li>Fine-tuned T5 for multi-label policy classification; LSTM/Prophet for trend forecasts</li>
            <li>Monitoring & experiment tracking; dashboards with ranked risks; forecast error &lt;15%</li>
            <li>~75% reduction in manual monitoring; CI/CD with rollback</li>
          </ul>
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
        <img class="thumb" src="/assets/images/decidousForest.jpg" alt="Phenology project">
        <div>
          Production-style CV pipeline to classify leaf phenophases and forecast SOS/EOS across sites.
          <ul class="bullets">
            <li>ResNet-50 with GAN augmentation for rare phases; calibrated probabilities</li>
            <li>Cross-site generalization; reproducible training with experiment tracking</li>
            <li>Automated evaluation & reporting artifacts for stakeholders</li>
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
        <img class="thumb" src="/assets/images/yt.jpg" alt="YouTube pipeline">
        <div>
          Config-driven ETL from YouTube API to S3/Snowflake with idempotent upserts and downstream analytics.
          <ul class="bullets">
            <li>Incremental loads, retries, schema & quality checks, structured logs</li>
            <li>Ready-to-query marts for content performance and growth KPIs</li>
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
        <img class="thumb" src="/assets/images/houese_price.jpg" alt="Housing profiler">
        <div>
          60k+ listings standardized into analytics tables; modeled price drivers and sensitivity for planning.
          <ul class="bullets">
            <li>Flattened JSON → ~40% faster queries; full geocoding & feature engineering</li>
            <li>Key business questions answered with clear visuals and SQL notebooks</li>
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
        <span class="pill">DE & BI</span>
        <span class="title">Uber Data Analytics (GCS · Mage · BigQuery · Looker)</span>
        <span class="meta">
          <span>Aug&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Uber_data_Analytics" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/uber-header.jpg" alt="Uber analytics">
        <div>
          End-to-end pipeline to BI for demand/supply insights with KPI queries that return in seconds.
          <ul class="bullets">
            <li>Partitioned & clustered BigQuery tables; fast Looker Studio dashboard</li>
            <li>Stakeholder views on peak demand, supply gaps, and driver incentives</li>
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
        <img class="thumb" src="/assets/images/salary_pred.jpg" alt="Salary prediction">
        <div>
          From baseline to tuned GD with diagnostics and measurable error reduction.
          <ul class="bullets">
            <li>MSE improved from 91.2% → 6.3% via scaling, feature selection, step tuning</li>
            <li>Clear learning-rate visualization & convergence criteria</li>
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
        <img class="thumb" src="/assets/images/research_placeholder_1.png" alt="Insurance & infant outcomes">
        <div>
          Causal/logistic modeling to assess payer-type effects on infant survival using multi-site EHR.
          <ul class="bullets">
            <li>Equity-focused subgroup analyses; reproducible pipelines and audit readiness</li>
          </ul>
        </div>
      </div>
    </details>

    <details class="card" id="utilization-guidelines">
      <summary>
        <span class="pill">Health Analytics</span>
        <span class="title">Healthcare Utilization & Guideline Adherence</span>
        <span class="meta"><span>Aug&nbsp;2025</span></span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/research_placeholder_2.png" alt="Utilization & adherence">
        <div>
          ML/statistical models on 50k+ records to evaluate compliance and long-horizon utilization patterns.
          <ul class="bullets">
            <li>Identified utilization profiles and top predictors; sequence modeling at scale</li>
          </ul>
        </div>
      </div>
    </details>
  </div><!-- /.cards -->

</div>

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