---
layout: single
title:
permalink: /skills/
date: 2023-09-02
categories: pages
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#ffffff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
    --bg:#f8fafc; --wrap-max: 1000px;
  }

  .skills-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    width:100%; max-width:min(100%, var(--wrap-max));
    margin-inline:auto; padding-inline:12px; box-sizing:border-box;
    color:var(--ink);
  }

  h1.page-title{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .9rem; }

  /* Card grid */
  .grid{
    display:grid; gap:12px;
    grid-template-columns: repeat(1, minmax(0, 1fr));
  }
  @media (min-width:740px){ .grid{ grid-template-columns: repeat(2, minmax(0,1fr)); } }
  @media (min-width:980px){ .grid{ grid-template-columns: repeat(3, minmax(0,1fr)); } }

  /* Card */
  .card{
    background:var(--card); border:1px solid var(--line); border-radius:14px;
    box-shadow:0 1px 0 var(--ring); overflow:hidden;
    display:flex; flex-direction:column; min-height: 180px;
  }
  .card-head{
    display:flex; align-items:center; gap:10px;
    padding:12px 14px; background:#fff; border-bottom:1px solid var(--line);
  }
  .icon{
    width:34px; height:34px; border-radius:8px; border:1px solid var(--line);
    display:flex; align-items:center; justify-content:center; background:#fff; font-weight:700; color:var(--brand);
  }
  .title{ font-weight:700; font-size:16px; color:var(--ink); }
  .sub{ color:var(--muted); font-size:13px; margin-left:auto; }

  .card-body{ padding:12px 14px; }
  .badges{ display:flex; flex-wrap:wrap; gap:8px; }
  .badge{
    padding:6px 10px; font-size:13px; font-weight:600;
    background:#eef3f8; color:#0f172a; border:1px solid #dbe2ea; border-radius:999px;
  }

  /* “Show more” collapsible */
  details.more{ margin-top:.6rem; }
  details.more > summary{
    list-style:none; cursor:pointer; color:var(--brand); font-weight:600; font-size:13px;
  }
  details.more > summary::-webkit-details-marker{ display:none; }
  .more-body{
    margin-top:.5rem; padding:.6rem .6rem; border:1px dashed #e9edf3; border-radius:10px; background:#fff;
    font-size:13.5px; color:#374151;
  }
</style>

<div class="skills-wrap">
  <h1 class="page-title">Skills</h1>
  <p class="page-sub">A quick, visual snapshot. Click “Show more” if you’d like the longer list—otherwise it stays minimal.</p>

  <div class="grid">
    <!-- Programming -->
    <section class="card">
      <div class="card-head">
        <div class="icon">λ</div>
        <div class="title">Programming</div>
        <div class="sub">core stack</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Python</span>
          <span class="badge">R</span>
          <span class="badge">SQL</span>
          <span class="badge">NoSQL</span>
          <span class="badge">HTML/CSS</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Comfortable with Core Java; daily development in Jupyter & VS Code. Strong data-frame work (pandas/dplyr), tidy SQL and tested utilities.
          </div>
        </details>
      </div>
    </section>

    <!-- Data Engineering -->
    <section class="card">
      <div class="card-head">
        <div class="icon">⛓</div>
        <div class="title">Data Engineering</div>
        <div class="sub">pipelines</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Airflow</span>
          <span class="badge">Informatica</span>
          <span class="badge">Kafka</span>
          <span class="badge">ETL/ELT</span>
          <span class="badge">Data Quality</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Source→target mappings, idempotent upserts, audit logs, and reproducible ingestion/standardization flows (OMOP/OHDSI).
          </div>
        </details>
      </div>
    </section>

    <!-- Analytics & ML -->
    <section class="card">
      <div class="card-head">
        <div class="icon">∑</div>
        <div class="title">Analytics & ML</div>
        <div class="sub">modeling</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Regression</span>
          <span class="badge">Classification</span>
          <span class="badge">Clustering</span>
          <span class="badge">Causal Inference</span>
          <span class="badge">A/B Testing</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Trees/Forest, SVM, Naïve Bayes; feature engineering (PCA/OHE); tuning (GD, grid search); calibrated probabilities and practical metrics.
          </div>
        </details>
      </div>
    </section>

    <!-- Databases -->
    <section class="card">
      <div class="card-head">
        <div class="icon">DB</div>
        <div class="title">Databases</div>
        <div class="sub">SQL & warehouses</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">PostgreSQL</span>
          <span class="badge">MySQL</span>
          <span class="badge">Teradata</span>
          <span class="badge">Snowflake</span>
          <span class="badge">BigQuery</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Schema design, performance-minded queries, flattening semi-structured data, and secure access patterns.
          </div>
        </details>
      </div>
    </section>

    <!-- BI & Viz -->
    <section class="card">
      <div class="card-head">
        <div class="icon">📊</div>
        <div class="title">BI & Visualization</div>
        <div class="sub">dashboards</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Tableau</span>
          <span class="badge">Looker Studio</span>
          <span class="badge">Plotly</span>
          <span class="badge">Seaborn</span>
          <span class="badge">Excel</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            One-question dashboards, annotated visuals, and QA workflows that keep charts honest.
          </div>
        </details>
      </div>
    </section>

    <!-- Cloud & Security -->
    <section class="card">
      <div class="card-head">
        <div class="icon">☁︎</div>
        <div class="title">Cloud & Security</div>
        <div class="sub">infra</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">AWS (Athena, S3)</span>
          <span class="badge">GCP</span>
          <span class="badge">OMOP / OHDSI</span>
          <span class="badge">WhiteRabbit</span>
          <span class="badge">Protegrity</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Privacy-aware analytics, PHI/PII handling, and audit-friendly workflows in clinical data contexts.
          </div>
        </details>
      </div>
    </section>

    <!-- Collaboration -->
    <section class="card">
      <div class="card-head">
        <div class="icon">⚑</div>
        <div class="title">Collaboration</div>
        <div class="sub">how I work</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Leadership</span>
          <span class="badge">Time/Task Mgmt</span>
          <span class="badge">Clear Communication</span>
          <span class="badge">Problem Solving</span>
          <span class="badge">JIRA</span>
        </div>
        <details class="more">
          <summary>Show more</summary>
          <div class="more-body">
            Document-first habits, readable code, and structured updates that de-risk handoffs.
          </div>
        </details>
      </div>
    </section>
  </div>
</div>
