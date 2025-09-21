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

    /* Control the OUTER shell and the inner content width for THIS PAGE */
    --site-max: 1400px;     /* widen the theme’s page container */
    --content-max: 1280px;  /* inner content column for your cards */
  }

  /* ===== Make the Minimal Mistakes shell wider on this page ===== */
  @media (min-width:1200px){
    /* widen outer wrappers the theme uses */
    .masthead__inner-wrap,
    .initial-content,
    .page,
    .archive,
    .page__inner-wrap,
    .page__content{
      max-width: var(--site-max) !important;
      margin-left:auto; margin-right:auto;
    }

    /* ensure there's no sidebar column reserved */
    .layout--single .sidebar,
    .layout--single .page__sidebar{ display:none !important; }
  }

  /* ===== Your inner container ===== */
  .wrap{
    font-family:'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    max-width: min(var(--content-max), 96vw);
    margin: 0 auto;
    color: var(--ink);
  }

  h1.section-title{
    color: var(--brand);
    margin: .25rem 0 .4rem;
    font-size: clamp(24px, 3vw, 30px);
  }
  p.section-sub{
    margin: 0 0 .9rem;
    color: var(--muted);
    font-size: 14.5px;
  }

  /* ===== Card grid ===== */
  .cards{ display:grid; gap:16px; }
  @media (min-width:1000px){
    .cards{ grid-template-columns: repeat(3, 1fr); }   /* 3-up on desktop */
  }
  @media (min-width:1600px){
    .cards{ grid-template-columns: repeat(4, 1fr); }   /* 4-up on very wide */
  }

  /* ===== Collapsible cards ===== */
  details.card{
    border: 1px solid var(--line);
    border-radius: 12px;
    background: var(--card);
    box-shadow: 0 1px 0 var(--ring);
    overflow: clip;
  }
  .card + .card{ margin-top: 10px; }
  @media (min-width:1000px){ .card + .card{ margin-top: 0; } }

  /* Summary row */
  .card > summary{
    list-style:none; cursor:pointer;
    display:flex; align-items:center; gap:12px; flex-wrap:wrap;
    padding: 12px 14px; outline:none;
  }
  .card > summary::-webkit-details-marker{ display:none; }

  .pill{
    font-size:12px; font-weight:600;
    color: var(--brand); background:#eef3f8;
    padding: 4px 10px; border-radius:999px;
    border:1px solid #dbe2ea; white-space: nowrap;
  }
  .title{ font-weight:600; font-size:16px; color:var(--ink); }
  .meta{
    margin-left:auto; display:flex; gap:10px; align-items:center;
    color:var(--muted); font-size:13px;
  }
  .meta .gh{
    text-decoration:none; border:1px solid var(--brand); color:var(--brand);
    padding: 5px 8px; border-radius:8px; font-weight:600; font-size:13px;
  }
  .meta .gh:hover{ background: var(--brand); color:#fff; }

  /* Expanded content */
  .content{
    display:grid; grid-template-columns: 1fr; gap: 12px;
    border-top:1px solid var(--line); padding: 12px 14px 14px;
    font-size:15px; line-height:1.55;
  }
  @media (min-width:860px){
    .content{ grid-template-columns: 320px 1fr; }   /* image | text */
  }

  .thumb{
    width:100%; aspect-ratio:16/10; object-fit:cover;
    border-radius:10px; border:1px solid var(--line); background:var(--bg);
  }

  .bullets{ margin:.25rem 0 0; padding-left:18px; }
  .bullets li{ margin:.2rem 0; }
  .links{ display:flex; gap:10px; flex-wrap:wrap; margin-top:.5rem; }
  .btn{ display:inline-block; text-decoration:none; font-weight:600;
        padding:7px 10px; border-radius:9px; font-size:14px; }
  .btn.ghost{ border:1px solid var(--brand); color:var(--brand); }

  .divider{ height:1px; background:var(--line); margin:1.1rem 0 .8rem; }
</style>

<div class="wrap">

  <!-- ===================== PROJECTS ===================== -->
  <h1 class="section-title">Projects</h1>
  <p class="section-sub">Browse selected personal projects. Click a card to view a short summary, visuals, and links.</p>

  <div class="cards">
    <!-- PROJECT 1 -->
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
          Detect leaf phenophase from PhenoCam images and forecast SOS/EOS across sites with augmentation for rare phases.
          <ul class="bullets">
            <li>ResNet-50 classifier; GANs for data scarcity</li>
            <li>Cross-site generalization beyond single camera tuning</li>
            <li>Calendar-level SOS/EOS with confidence bands</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/SOS_EOS.png" target="_blank">SOS/EOS plot</a>
            <a class="btn ghost" href="/assets/images/GAN.png" target="_blank">GAN architecture</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 2 -->
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
          Config-driven ETL from YouTube API to S3/Snowflake with Airflow orchestration.
          <ul class="bullets">
            <li>Incremental loads, retries, schema checks, logs</li>
            <li>Idempotent upserts; downstream content analytics</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/youtube.png" target="_blank">Pipeline overview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 3 -->
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
          60k+ listings scraped and standardized; modeled price drivers and sensitivity.
          <ul class="bullets">
            <li>Flattened JSON → ~40% faster queries; full geocoding</li>
            <li>Answered 11 key business questions</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/overview_house.png" target="_blank">Schema overview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 4 -->
    <details class="card" id="breast-cancer">
      <summary>
        <span class="pill">ML</span>
        <span class="title">Breast Cancer Prediction (LR vs. NN)</span>
        <span class="meta">
          <span>Oct&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Breast_Cancer_Prediction" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/breast_cancer.png" alt="Breast cancer project">
        <div>
          Compare classical and deep approaches for early detection on tabular features.
          <ul class="bullets">
            <li>LR 92.9% acc; Keras NN 97.3% acc</li>
            <li>SMOTE for imbalance; calibrated probabilities</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/overview_breastCancer.png" target="_blank">Model summary</a>
            <a class="btn ghost" href="/assets/images/NN_model_accuracy_Loss.png" target="_blank">Training curves</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 5 -->
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
          End-to-end pipeline to BI with KPI queries returning in seconds.
          <ul class="bullets">
            <li>Stakeholder dashboard for demand peaks & supply gaps</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="https://lookerstudio.google.com/s/s-nnQQB79Kw" target="_blank" rel="noopener">Dashboard</a>
            <a class="btn ghost" href="/assets/images/uber_dashboard.jpg" target="_blank">Dashboard preview</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 6 -->
    <details class="card" id="fraud">
      <summary>
        <span class="pill">ML</span>
        <span class="title">Credit Card Fraud Detection</span>
        <span class="meta">
          <span>Aug&nbsp;2023</span>
          <a class="gh" href="https://github.com/AmritaNeogi/Data-Science-Project-Credit-Card-Fraud-Detection" target="_blank" rel="noopener">GitHub</a>
        </span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/credit_card.jpeg" alt="Fraud detection">
        <div>
          Imbalanced classification with SMOTE and model comparison (DT, LR, RF, NB).
          <ul class="bullets">
            <li>Best model ~99% accuracy; +~10% after rebalancing</li>
          </ul>
          <div class="links">
            <a class="btn ghost" href="/assets/images/final_summary.png" target="_blank">Results snapshot</a>
          </div>
        </div>
      </div>
    </details>

    <!-- PROJECT 7 -->
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
          From baseline to tuned GD with strong MSE reduction and clear diagnostics.
          <ul class="bullets">
            <li>MSE reduced from 91.2% → 6.3% with scaling & step tuning</li>
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
    <!-- RESEARCH 1 -->
    <details class="card" id="insurance-infant">
      <summary>
        <span class="pill">Causal Inference</span>
        <span class="title">Insurance at Birth & Infant Outcomes (EHR, multi-site)</span>
        <span class="meta"><span>Sep&nbsp;2025</span></span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/research_placeholder_1.png" alt="Insurance & infant outcomes (placeholder)">
        <div>
          Causal/logistic modeling to assess payer-type effects on infant survival using multi-site EHR.
          <ul class="bullets">
            <li>Disparities: uninsured/self-pay highest risk; Medicaid ~10% survival gain; private ~70% strongest protection</li>
            <li>Reproducible pipelines for subgroup analyses and equity-focused reporting</li>
          </ul>
        </div>
      </div>
    </details>

    <!-- RESEARCH 2 -->
    <details class="card" id="utilization-guidelines">
      <summary>
        <span class="pill">Health Analytics</span>
        <span class="title">Healthcare Utilization & Guideline Adherence</span>
        <span class="meta"><span>Aug&nbsp;2025</span></span>
      </summary>
      <div class="content">
        <img class="thumb" src="/assets/images/research_placeholder_2.png" alt="Utilization & adherence (placeholder)">
        <div>
          ML/statistical models on 50k+ records to evaluate compliance and long-horizon utilization patterns.
          <ul class="bullets">
            <li>Identified 3 distinct utilization patterns + top 5 predictors of continuous care</li>
            <li>Analyzed 10-year trajectories across pediatric/adult cohorts; equity-focused insights and scalable sequence models</li>
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
