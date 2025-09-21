---
layout: single
classes: wide
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
    --bg:#f8fafc;

    /* how wide you want the Skills content to run */
    --skills-max: 1180px;     /* bump to 1240/1280 if you want even wider */
  }

  /* ============ LEFT-LOCK the page (only this page) ============ */
  /* Pull the wrapper to the very-left edge of the viewport. Works regardless of theme container paddings. */
  .skills-leftlock{
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
    background: transparent;
  }
  /* Center our real content inside the left-locked strip */
  .skills-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    width: 100%;
    max-width: min(var(--skills-max), 96vw);
    margin: 0 auto;
    padding: 0 16px;                /* small gutter so borders never kiss the edge */
    box-sizing: border-box;
    color: var(--ink);
  }

  /* Also remove Minimal Mistakes’ inner padding/margins that can offset left edge */
  @media (min-width: 768px){
    .layout--single .page__inner-wrap{ padding-left:0 !important; padding-right:0 !important; }
    .layout--single .page__content{ margin-left:0 !important; margin-right:0 !important; padding:0 !important; }
  }

  h1.page-title{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

  /* Sticky top bar (pills + filter) */
  .topbar{
    position:sticky; top:0; z-index:3; background:var(--bg);
    border-bottom:1px solid var(--line); padding:8px 0; margin-bottom:.8rem;
    display:flex; flex-wrap:wrap; gap:8px; align-items:center;
  }
  .pills{ display:flex; gap:8px; flex-wrap:wrap; }
  .pill-link{
    text-decoration:none; color:var(--brand); border:1px solid var(--brand);
    background:#fff; padding:6px 10px; border-radius:999px; font-weight:600; font-size:13px;
  }
  .filter{ margin-left:auto; display:flex; align-items:center; gap:8px; }
  .filter input{
    padding:7px 10px; border:1px solid var(--line); border-radius:10px;
    font-size:14px; width:190px; background:#fff;
  }

  /* Cards */
  .card{
    background:var(--card); border:1px solid var(--line); border-radius:14px;
    box-shadow:0 1px 0 var(--ring); margin:.8rem 0; overflow:hidden;
  }
  .card-header{
    display:flex; justify-content:space-between; align-items:center;
    padding:12px 14px; background:#fff;
  }
  .card-title{ font-weight:700; color:var(--brand); font-size:16px; }
  .card-sub{ color:var(--muted); font-size:13.5px; }

  .card-body{
    padding:12px 14px 14px; border-top:1px solid var(--line);
    overflow-wrap:anywhere; /* prevent any clipping on long tokens */
  }

  /* Responsive grid inside cards */
  .grid{ display:grid; gap:12px; grid-template-columns: 1fr; }
  @media (min-width:760px){ .grid{ grid-template-columns: repeat(2, minmax(0,1fr)); } }
  @media (min-width:1100px){ .grid{ grid-template-columns: repeat(3, minmax(0,1fr)); } }

  /* Groups inside each card */
  .group{
    border:1px dashed #e9edf3; border-radius:10px; padding:10px 12px; background:#fff;
  }
  .group h4{ margin:.1rem 0 .4rem; font-size:14.5px; color:var(--ink); }

  /* Badges */
  .badges{ display:flex; flex-wrap:wrap; gap:8px; }
  .badge{
    display:inline-flex; align-items:center; gap:6px;
    padding:6px 10px; font-size:13px; font-weight:600;
    background:#eef3f8; color:#0f172a; border:1px solid #dbe2ea; border-radius:999px;
    white-space:nowrap;
  }

  /* When filtering */
  .hidden-by-filter{ display:none !important; }
</style>

<div class="skills-leftlock">
  <div class="skills-wrap" id="skills-top">
    <h1 class="page-title">Skills</h1>
    <p class="page-sub">A compact overview of languages, platforms, analytics, and soft skills I use most. Filter or jump to a section.</p>

    <div class="topbar">
      <div class="pills">
        <a class="pill-link" href="#prog">Programming</a>
        <a class="pill-link" href="#tools">Tools &amp; Platforms</a>
        <a class="pill-link" href="#ds">Data Science &amp; Analytics</a>
        <a class="pill-link" href="#soft">Soft Skills</a>
      </div>
      <div class="filter" aria-label="Skill filter">
        <input id="skillFilter" type="search" placeholder="Filter skills…">
      </div>
    </div>

    <!-- PROGRAMMING -->
    <section class="card" id="prog">
      <div class="card-header">
        <div class="card-title">Programming Languages</div>
        <div class="card-sub">Daily drivers &amp; working knowledge</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Python</span>
          <span class="badge">R</span>
          <span class="badge">SQL</span>
          <span class="badge">NoSQL</span>
        </div>
      </div>
    </section>

    <!-- TOOLS & PLATFORMS -->
    <section class="card" id="tools">
      <div class="card-header">
        <div class="card-title">Tools &amp; Platforms</div>
        <div class="card-sub">Data, orchestration, BI, cloud, security</div>
      </div>
      <div class="card-body">
        <div class="grid">
          <div class="group">
            <h4>Databases</h4>
            <div class="badges">
              <span class="badge">MySQL</span>
              <span class="badge">PostgreSQL</span>
              <span class="badge">Teradata</span>
              <span class="badge">Snowflake</span>
              <span class="badge">Google BigQuery</span>
            </div>
          </div>

          <div class="group">
            <h4>Notebooks &amp; Dev</h4>
            <div class="badges">
              <span class="badge">Jupyter</span>
              <span class="badge">Git</span>
              <span class="badge">CI/CD</span>
            </div>
          </div>

          <div class="group">
            <h4>ETL &amp; Orchestration</h4>
            <div class="badges">
              <span class="badge">Informatica PowerCenter</span>
              <span class="badge">Apache Airflow</span>
              <span class="badge">Apache Kafka</span>
            </div>
          </div>

          <div class="group">
            <h4>Visualization &amp; BI</h4>
            <div class="badges">
              <span class="badge">Tableau</span>
              <span class="badge">Power BI</span>
              <span class="badge">Looker Studio</span>
              <span class="badge">Plotly</span>
              <span class="badge">Seaborn</span>
              <span class="badge">Excel</span>
            </div>
          </div>

          <div class="group">
            <h4>Cloud</h4>
            <div class="badges">
              <span class="badge">AWS (Athena, S3)</span>
              <span class="badge">Google Cloud Platform</span>
            </div>
          </div>

          <div class="group">
            <h4>Data Models &amp; Tools</h4>
            <div class="badges">
              <span class="badge">OMOP / OHDSI</span>
              <span class="badge">WhiteRabbit</span>
            </div>
          </div>

          <div class="group">
            <h4>Security &amp; Workflow</h4>
            <div class="badges">
              <span class="badge">Protegrity</span>
              <span class="badge">JIRA</span>
              <span class="badge">Amazon MTurk</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- DATA SCIENCE & ANALYTICS -->
    <section class="card" id="ds">
      <div class="card-header">
        <div class="card-title">Data Science &amp; Analytics</div>
        <div class="card-sub">Modeling, evaluation, experimentation</div>
      </div>
      <div class="card-body">
        <div class="group" style="margin-bottom:10px;">
          <h4 style="margin:.1rem 0 .35rem;">Featured: ML &amp; Analytics</h4>
          <div class="badges">
            <span class="badge">Classification</span>
            <span class="badge">Regression</span>
            <span class="badge">Clustering</span>
            <span class="badge">Time-Series</span>
            <span class="badge">Trend Analysis</span>
            <span class="badge">Causal Inference</span>
            <span class="badge">Deep Learning (CNN/RNN/LSTM)</span>
            <span class="badge">Anomaly Detection</span>
            <span class="badge">Summary Statistics</span>
            <span class="badge">Data Quality &amp; Validation</span>
          </div>
        </div>

        <div class="grid">
          <div class="group">
            <h4>Core</h4>
            <div class="badges">
              <span class="badge">Data Wrangling</span>
              <span class="badge">EDA</span>
              <span class="badge">Feature Engineering</span>
              <span class="badge">A/B Testing</span>
            </div>
          </div>

          <div class="group">
            <h4>Models</h4>
            <div class="badges">
              <span class="badge">Decision Trees</span>
              <span class="badge">Random Forest</span>
              <span class="badge">SVM</span>
              <span class="badge">Naïve Bayes</span>
            </div>
          </div>

          <div class="group">
            <h4>Optimization &amp; Tuning</h4>
            <div class="badges">
              <span class="badge">Gradient Descent</span>
              <span class="badge">Grid Search</span>
              <span class="badge">PCA</span>
              <span class="badge">One-Hot Encoding</span>
            </div>
          </div>

          <div class="group">
            <h4>Business &amp; Strategy</h4>
            <div class="badges">
              <span class="badge">RFM Segmentation</span>
              <span class="badge">Strategic Planning</span>
              <span class="badge">Decision Making</span>
              <span class="badge">Excel Analysis</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SOFT SKILLS -->
    <section class="card" id="soft">
      <div class="card-header">
        <div class="card-title">Soft Skills</div>
        <div class="card-sub">How I like to work</div>
      </div>
      <div class="card-body">
        <div class="badges">
          <span class="badge">Leadership</span>
          <span class="badge">Time Management</span>
          <span class="badge">Task Management</span>
          <span class="badge">Data Management</span>
          <span class="badge">Critical Thinking</span>
          <span class="badge">Problem Solving</span>
          <span class="badge">Clear Communication</span>
        </div>
      </div>
    </section>
  </div>
</div>

<script>
  // Simple client-side filter (matches text of badges and headings)
  const input = document.getElementById('skillFilter');
  if (input){
    input.addEventListener('input', () => {
      const q = input.value.trim().toLowerCase();
      document.querySelectorAll('.card').forEach(card => {
        const text = card.innerText.toLowerCase();
        const hit = q === '' || text.includes(q);
        card.classList.toggle('hidden-by-filter', !hit);
      });
    });
  }
</script>
