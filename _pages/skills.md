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

    /* make left edge line up with “Home” in the masthead */
    --masthead-left: 24px;        /* tweak to 20–28px if you need a pixel-perfect line-up */
    --wrap-max: 1200px;           /* container max width on wide screens */
  }

  /* ========= OVERRIDES: remove all theme centering + left padding on THIS PAGE ========= */
  @media (min-width: 900px){
    .layout--single .sidebar,
    .layout--single .page__sidebar{ display:none !important; }

    .layout--single .page{ display:block !important; max-width:none !important; }
    .layout--single .page__inner-wrap{ padding-left:0 !important; padding-right:0 !important; }

    .layout--single .initial-content,
    .layout--single .page,
    .layout--single .page__content,
    .layout--single .archive{
      max-width:none !important;
      width:100% !important;
      margin:0 !important;
      padding:0 !important;
    }
  }

  /* ========= Left-aligned page wrapper ========= */
  .skills-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    color:var(--ink);
    margin-left: var(--masthead-left);
    margin-right: 16px;
    width: min(var(--wrap-max), calc(100vw - var(--masthead-left) - 16px));
    box-sizing:border-box;
  }

  h1.page-title{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

  /* Top pills + filter */
  .topbar{
    position:sticky; top:0; z-index:1; background:var(--bg);
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
    font-size:14px; width:180px; background:#fff;
  }

  /* ===== Collapsible Cards ===== */
  details.card{
    background:var(--card);
    border:1px solid var(--line);
    border-radius:14px;
    box-shadow:0 1px 0 var(--ring);
    margin:.7rem 0;
    overflow:hidden;
  }
  .card > summary{
    list-style:none; cursor:pointer; outline:none;
    display:flex; justify-content:space-between; align-items:center;
    gap:12px; padding:12px 14px; background:#fff;
  }
  .card > summary::-webkit-details-marker{ display:none; }
  .card-title{ font-weight:700; color:var(--brand); font-size:16px; }
  .card-sub{ color:var(--muted); font-size:13.5px; }
  .card-body{ padding:12px 14px 14px; border-top:1px solid var(--line); }

  /* Tiny chevron indicator */
  .card summary .chev{
    margin-left:10px; font-size:14px; color:var(--muted);
    transition: transform .18s ease;
  }
  details.card[open] summary .chev{ transform: rotate(180deg); }

  /* Grid inside cards */
  .grid{ display:grid; gap:10px; grid-template-columns: repeat(1, minmax(0,1fr)); }
  @media (min-width:760px){ .grid{ grid-template-columns: repeat(2, minmax(0,1fr)); } }
  @media (min-width:980px){ .grid{ grid-template-columns: repeat(3, minmax(0,1fr)); } }

  /* Groups within a card */
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
  }

  /* Hide helper when using filter */
  .hidden-by-filter{ display:none !important; }
</style>

<div class="skills-wrap">
  <h1 class="page-title">Skills</h1>
  <p class="page-sub">A compact overview of languages, platforms, analytics, and soft skills I use most. Filter or jump to a section.</p>

  <div class="topbar">
    <div class="pills">
      <a class="pill-link" href="#prog">Programming</a>
      <a class="pill-link" href="#tools">Tools & Platforms</a>
      <a class="pill-link" href="#ds">Data Science & Analytics</a>
      <a class="pill-link" href="#soft">Soft Skills</a>
    </div>
    <div class="filter" aria-label="Skill filter">
      <input id="skillFilter" type="search" placeholder="Filter skills…">
    </div>
  </div>

  <!-- PROGRAMMING (collapsible) -->
  <details class="card" id="prog" open>
    <summary>
      <span class="card-title">Programming Languages</span>
      <span class="card-sub">Daily drivers & working knowledge <span class="chev">▾</span></span>
    </summary>
    <div class="card-body">
      <div class="badges">
        <span class="badge">Python</span>
        <span class="badge">R</span>
        <span class="badge">SQL</span>
        <span class="badge">NoSQL</span>
      </div>
    </div>
  </details>

  <!-- TOOLS & PLATFORMS (collapsible) -->
  <details class="card" id="tools" open>
    <summary>
      <span class="card-title">Tools & Platforms</span>
      <span class="card-sub">Data, orchestration, BI, cloud, security <span class="chev">▾</span></span>
    </summary>
    <div class="card-body">
      <div class="grid">
        <div class="group">
          <h4>Databases</h4>
          <div class="badges">
            <span class="badge">MySQL</span><span class="badge">PostgreSQL</span>
            <span class="badge">Teradata</span><span class="badge">Snowflake</span>
            <span class="badge">Google&nbsp;BigQuery</span>
          </div>
        </div>
        <div class="group">
          <h4>Notebooks & Dev</h4>
          <div class="badges">
            <span class="badge">Jupyter</span><span class="badge">Git</span><span class="badge">CI/CD</span>
          </div>
        </div>
        <div class="group">
          <h4>ETL & Orchestration</h4>
          <div class="badges">
            <span class="badge">Informatica PowerCenter</span><span class="badge">Apache Airflow</span>
            <span class="badge">Apache Kafka</span>
          </div>
        </div>
        <div class="group">
          <h4>Visualization & BI</h4>
          <div class="badges">
            <span class="badge">Tableau</span><span class="badge">Power BI</span>
            <span class="badge">Looker Studio</span><span class="badge">Plotly</span>
            <span class="badge">Seaborn</span><span class="badge">Excel</span>
          </div>
        </div>
        <div class="group">
          <h4>Cloud</h4>
          <div class="badges">
            <span class="badge">AWS (Athena, S3)</span><span class="badge">Google Cloud Platform</span>
          </div>
        </div>
        <div class="group">
          <h4>Data Models & Tools</h4>
          <div class="badges">
            <span class="badge">OMOP / OHDSI</span><span class="badge">WhiteRabbit</span>
          </div>
        </div>
        <div class="group">
          <h4>Security & Workflow</h4>
          <div class="badges">
            <span class="badge">Protegrity</span><span class="badge">JIRA</span>
            <span class="badge">Amazon MTurk</span>
          </div>
        </div>
      </div>
    </div>
  </details>

  <!-- DATA SCIENCE & ANALYTICS (collapsible) -->
  <details class="card" id="ds" open>
    <summary>
      <span class="card-title">Data Science & Analytics</span>
      <span class="card-sub">Modeling, evaluation, experimentation <span class="chev">▾</span></span>
    </summary>
    <div class="card-body">
      <div class="group" style="margin-bottom:10px;">
        <h4 style="margin:.1rem 0 .35rem;">Featured: ML & Analytics</h4>
        <div class="badges">
          <span class="badge">Classification</span><span class="badge">Regression</span>
          <span class="badge">Clustering</span><span class="badge">Time-Series</span>
          <span class="badge">Trend Analysis</span><span class="badge">Causal Inference</span>
          <span class="badge">Deep Learning (CNN/RNN/LSTM)</span>
          <span class="badge">Anomaly Detection</span><span class="badge">Summary Statistics</span>
          <span class="badge">Data Quality &amp; Validation</span>
        </div>
      </div>
      <div class="grid">
        <div class="group">
          <h4>Core</h4>
          <div class="badges">
            <span class="badge">Data Wrangling</span><span class="badge">EDA</span>
            <span class="badge">Feature Engineering</span><span class="badge">A/B Testing</span>
          </div>
        </div>
        <div class="group">
          <h4>Models</h4>
          <div class="badges">
            <span class="badge">Decision Trees</span><span class="badge">Random Forest</span>
            <span class="badge">SVM</span><span class="badge">Naïve Bayes</span>
          </div>
        </div>
        <div class="group">
          <h4>Optimization & Tuning</h4>
          <div class="badges">
            <span class="badge">Gradient Descent</span><span class="badge">Grid Search</span>
            <span class="badge">PCA</span><span class="badge">One-Hot Encoding</span>
          </div>
        </div>
        <div class="group">
          <h4>Business & Strategy</h4>
          <div class="badges">
            <span class="badge">RFM Segmentation</span><span class="badge">Strategic Planning</span>
            <span class="badge">Decision Making</span><span class="badge">Excel Analysis</span>
          </div>
        </div>
      </div>
    </div>
  </details>

  <!-- SOFT SKILLS (collapsible) -->
  <details class="card" id="soft" open>
    <summary>
      <span class="card-title">Soft Skills</span>
      <span class="card-sub">How I like to work <span class="chev">▾</span></span>
    </summary>
    <div class="card-body">
      <div class="badges">
        <span class="badge">Leadership</span><span class="badge">Time Management</span>
        <span class="badge">Task Management</span><span class="badge">Data Management</span>
        <span class="badge">Critical Thinking</span><span class="badge">Problem Solving</span>
        <span class="badge">Clear Communication</span>
      </div>
    </div>
  </details>
</div>

<script>
  // Simple client-side filter (matches text of badges and headings)
  const input = document.getElementById('skillFilter');
  if (input){
    input.addEventListener('input', () => {
      const q = input.value.trim().toLowerCase();
      document.querySelectorAll('.card').forEach(card => {
        const text = card.innerText.toLowerCase();
        card.classList.toggle('hidden-by-filter', !(q === '' || text.includes(q)));
      });
    });
  }

  // (Optional) keep only one section open at a time — enable if you want accordion behavior:
  // document.querySelectorAll('details.card').forEach(d => {
  //   d.addEventListener('toggle', () => {
  //     if (d.open) document.querySelectorAll('details.card').forEach(o => { if (o !== d) o.removeAttribute('open'); });
  //   });
  // });
</script>
