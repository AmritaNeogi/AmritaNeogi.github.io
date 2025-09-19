---
layout: single
title:
permalink: /Projects/
date: 2023-09-02
categories: pages
toc: false
toc_label: "Projects"
toc_icon: "columns"
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699;
    --ink:#1f2937;
    --muted:#6b7280;
    --card:#ffffff;
    --line:#e5e7eb;
    --ring:rgba(51,102,153,0.12);
  }
  .projects-wrap{
    font-family:'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    max-width: 880px;               /* centered, not too wide */
    margin: 0 auto;
    color: var(--ink);
  }
  .projects-wrap h1{
    color: var(--brand);
    margin: .25rem 0 .75rem;
    font-size: clamp(24px, 3vw, 30px);
  }
  .intro{
    margin: 0 0 .9rem;
    color: var(--muted);
    font-size: 15.5px;
  }

  /* Collapsible cards */
  details.project{
    border: 1px solid var(--line);
    border-radius: 12px;
    background: var(--card);
    box-shadow: 0 1px 0 var(--ring);
    margin: 10px 0;
    overflow: clip;
  }
  /* Horizontal summary row */
  .project > summary{
    list-style:none;
    cursor:pointer;
    display:flex;
    align-items:center;
    gap: 12px;
    padding: 12px 14px;
    outline:none;
  }
  .project > summary::-webkit-details-marker{ display:none; }
  .pill{
    font-size:12px; font-weight:600;
    color: var(--brand); background: #f1f5f9;
    padding: 4px 8px; border-radius: 999px;
    border: 1px solid #dbe2ea;
  }
  .title{
    font-weight: 600;
    font-size: 16px;
    color: var(--ink);
  }
  .meta{
    margin-left:auto;
    display:flex; gap:10px; align-items:center;
    color: var(--muted);
    font-size: 13px;
  }
  .meta .gh, .meta .ext{
    text-decoration:none;
    border:1px solid var(--brand);
    color: var(--brand);
    padding: 5px 8px; border-radius:8px;
    font-weight:600; font-size:13px;
  }
  .meta .gh:hover, .meta .ext:hover{ background: var(--brand); color:#fff; }

  /* Expanded content */
  .content{
    display:grid;
    grid-template-columns: 1fr;
    gap: 12px;
    border-top:1px solid var(--line);
    padding: 12px 14px 14px;
    font-size: 15px; line-height:1.55;
  }
  @media (min-width: 760px){
    .content{ grid-template-columns: 280px 1fr; } /* image | text */
  }
  .thumb{
    width:100%; height:auto; border-radius:10px; border:1px solid var(--line);
  }
  .bullets{ margin:.25rem 0 0; padding-left: 18px; }
  .bullets li{ margin:.2rem 0; }
  .links{
    display:flex; gap:10px; flex-wrap:wrap; margin-top:.5rem;
  }
  .btn{
    display:inline-block; text-decoration:none; font-weight:600;
    padding:7px 10px; border-radius:9px; font-size:14px;
  }
  .btn.primary{ background:var(--brand); color:#fff; }
  .btn.ghost{ border:1px solid var(--brand); color:var(--brand); }
</style>

<div class="projects-wrap">
  <h1>Projects</h1>
  <p class="intro">
    Click a card to expand. Each project includes a quick summary, screenshots, and links to the repository and (where relevant) a short case study.
  </p>

  <!-- PROJECT 1 -->
  <details class="project" id="phenophase">
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
        Built a reproducible pipeline to detect leaf phenophase from PhenoCam images and predict SOS/EOS across sites.
        <ul class="bullets">
          <li>ResNet-50 classifier + GAN augmentation for rare phases</li>
          <li>Multi-site generalization (beyond single-camera tuning)</li>
          <li>Outputs calendar-level SOS/EOS with confidence bands</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/SOS_EOS.png" target="_blank">View SOS/EOS plot</a>
          <a class="btn ghost" href="/assets/images/GAN.png" target="_blank">GAN architecture</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 2 -->
  <details class="project" id="airflow-youtube">
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
        Automated channel-level ETL using YouTube Data API → transform → S3/Snowflake targets, orchestrated with Airflow.
        <ul class="bullets">
          <li>Config-driven DAGs, retries, logging, and schema checks</li>
          <li>Batch & incremental loads with idempotent upserts</li>
          <li>Downstream dashboards for content and growth analytics</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/youtube.png" target="_blank">Pipeline overview</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 3 -->
  <details class="project" id="snowflake-housing">
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
        Scraped 60k+ listings (Bright Data), translated/standardized fields, and modeled price drivers in Snowflake.
        <ul class="bullets">
          <li>Flattened JSON → 40% faster queries; geocoded lat/long → address</li>
          <li>Answered 11 business questions for price sensitivity</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/overview_house.png" target="_blank">Schema overview</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 4 -->
  <details class="project" id="breast-cancer">
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
        Compared classical and deep models for early detection on tabular features.
        <ul class="bullets">
          <li>Logistic Regression: 92.9% acc; Neural Network (Keras): 97.3% acc</li>
          <li>SMOTE to handle class imbalance, calibrated probabilities</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/overview_breastCancer.png" target="_blank">Model summary</a>
          <a class="btn ghost" href="/assets/images/NN_model_accuracy_Loss.png" target="_blank">Training curves</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 5 -->
  <details class="project" id="uber">
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
        End-to-end pipeline from ingestion to BI with interactive Looker dashboard.
        <ul class="bullets">
          <li>Mage ETL → BigQuery; KPI queries returning in seconds</li>
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
  <details class="project" id="fraud">
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
          <li>Best model ~99% accuracy; improved ~10% after rebalancing</li>
          <li>Explained precision/recall trade-offs for ops usage</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/final_summary.png" target="_blank">Results snapshot</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 7 -->
  <details class="project" id="salary">
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
          <li>MSE driven down from 91.2% to 6.3% with feature scaling & step tuning</li>
        </ul>
        <div class="links">
          <a class="btn ghost" href="/assets/images/summary1.png" target="_blank">Summary</a>
          <a class="btn ghost" href="/assets/images/gradient%20descent.png" target="_blank">GD visualization</a>
        </div>
      </div>
    </div>
  </details>

  <!-- PROJECT 8 -->
  <details class="project" id="cnn-classifier">
    <summary>
      <span class="pill">Deep Learning</span>
      <span class="title">Image Classifier with CNN (PyTorch)</span>
      <span class="meta">
        <span>Dec&nbsp;2022</span>
        <a class="gh" href="https://github.com/ISTA421INFO521/final-project-AmritaNeogi" target="_blank" rel="noopener">GitHub</a>
      </span>
    </summary>
    <div class="content">
      <img class="thumb" src="/assets/images/image_classifier.png" alt="Image classifier">
      <div>
        Large-scale image classification with a clean training/eval loop and 91.21% accuracy.
      </div>
    </div>
  </details>
</div>

<script>
  // Optional: keep only one project open at a time
  document.querySelectorAll('details.project').forEach((d) => {
    d.addEventListener('toggle', () => {
      if (d.open) {
        document.querySelectorAll('details.project').forEach(o => { if (o !== d) o.removeAttribute('open'); });
      }
    });
  });
</script>
