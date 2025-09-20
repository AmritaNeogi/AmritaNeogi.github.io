---
permalink: /
title:
subtitle: "Welcome to my website!"
excerpt: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root { --brand:#336699; --ink:#1f2937; --muted:#6b7280; --ring:rgba(51,102,153,0.12); }
  .landing { 
    font-family:'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    max-width: 720px;
    margin: 0 auto; 
  }
  .landing h1 { color:var(--brand); font-size:clamp(24px, 3vw, 30px); margin:0 0 .25rem; }
  .landing .lede { color:var(--ink); font-size:clamp(15px, 2vw, 16px); line-height:1.55; margin:0 0 .75rem; }

  .story {
    margin:.75rem 0 1rem; padding:.75rem .8rem;
    border:1px solid #e5e7eb; border-radius:12px; box-shadow:0 1px 0 var(--ring);
    font-size:15px; line-height:1.55;
  }
  .proof {
    display:grid; grid-template-columns:repeat(2, minmax(0,1fr)); gap:8px;
    list-style:none; padding:0; margin:.6rem 0 0;
  }
  @media (min-width:860px){ .proof{ grid-template-columns:repeat(3, minmax(0,1fr)); } }
  .proof li{ border:1px solid #e5e7eb; border-radius:10px; padding:8px 10px; background:#fff; font-size:14px; }
  .proof b{ color:var(--brand); }

  .cta{ display:flex; gap:8px; flex-wrap:wrap; margin-top:.6rem; }
  .btn{ display:inline-block; padding:7px 10px; border-radius:9px; text-decoration:none; font-weight:600; font-size:14px; }
  .btn.primary{ background:var(--brand); color:#fff; }
  .btn.ghost{ border:1px solid var(--brand); color:var(--brand); background:#fff; }

  .edu { margin:1rem 0 .3rem; }
  .edu h2{ color:var(--brand); font-size:20px; margin:0 0 .5rem; }
  .edu-grid{ display:grid; gap:12px; grid-template-columns:repeat(1, minmax(260px, 1fr)); }
  @media (min-width:760px){ .edu-grid{ grid-template-columns:repeat(2, minmax(300px, 1fr)); } }
  .edu-card{
    display:grid; grid-template-columns:36px 1fr; gap:10px; align-items:flex-start;
    border:1px solid #e5e7eb; border-radius:12px; padding:10px 12px; background:#fff; box-shadow:0 1px 0 var(--ring);
  }
  .edu-card img{ height:28px; width:28px; object-fit:contain; border-radius:4px; }

  /* Collapsible details */
  .edu-details { width:100%; }
  .edu-details summary {
    list-style:none; cursor:pointer;
    display:flex; align-items:center; justify-content:space-between; gap:10px;
    outline:none;
  }
  .edu-details summary::-webkit-details-marker { display:none; }
  .edu-title{ font-weight:600; font-size:15px; }
  .edu-quick{ color:var(--muted); font-size:13px; display:flex; gap:8px; flex-wrap:wrap; }
  .caret{ display:inline-block; font-weight:800; line-height:1; color:var(--brand); transform:rotate(0deg); transition:transform .18s ease; margin-left:6px; }
  .edu-details[open] .caret{ transform:rotate(90deg); }

  .edu-content{
    margin-top:8px; padding-top:8px; border-top:1px dashed #e5e7eb;
    display:grid; gap:12px; grid-template-columns: 1.3fr 1fr;
  }
  @media (max-width:700px){ .edu-content{ grid-template-columns:1fr; } }

  .subhead{ font-weight:600; font-size:13px; color:#374151; margin-bottom:4px; }
  .courses-list{ margin:0; padding-left:18px; line-height:1.5; font-size:13px; }
  .meta{ font-size:13px; color:#374151; }
  .meta dl{ margin:0; }
  .meta dt{ color:var(--muted); font-weight:500; }
  .meta dd{ margin:0 0 8px; font-weight:600; }

  .foot{ color:var(--muted); font-size:14px; margin-top:.8rem; }

  /* Roadmap (horizontal stepper) */
  .road{ margin:1.2rem 0 .6rem; }
  .road h2{ color:var(--brand); font-size:20px; margin:0 0 .5rem; }

  .rm{ border:1px solid #e5e7eb; border-radius:12px; background:#fff; box-shadow:0 1px 0 var(--ring); padding:10px 12px; }
  .rm input[type="radio"]{ position:absolute; left:-9999px; }
  .rm-strip{ position:relative; display:flex; gap:10px; align-items:center; overflow:auto; scroll-snap-type:x mandatory; padding-bottom:8px; }
  .rm-track{ position:absolute; left:0; right:0; height:2px; background:#e5e7eb; top:22px; }
  .rm-node{
    position:relative; z-index:1; scroll-snap-align:start;
    display:flex; align-items:center; gap:8px;
    white-space:nowrap; font-size:14px; font-weight:600; color:#374151;
    padding:6px 10px; border:1px solid #e5e7eb; border-radius:999px; background:#fff;
    transition:transform .12s ease, box-shadow .12s ease, border-color .12s ease;
  }
  .rm-node::before{
    content:""; position:absolute; left:12px; top:18px; width:10px; height:10px;
    background:#fff; border:2px solid var(--muted); border-radius:50%;
  }
  #rm1:checked ~ .rm-strip label[for="rm1"],
  #rm2:checked ~ .rm-strip label[for="rm2"],
  #rm3:checked ~ .rm-strip label[for="rm3"],
  #rm4:checked ~ .rm-strip label[for="rm4"],
  #rm5:checked ~ .rm-strip label[for="rm5"]{
    border-color:var(--brand); color:var(--brand);
    box-shadow:0 0 0 4px var(--ring); transform:translateY(-1px);
  }
  #rm1:checked ~ .rm-strip label[for="rm1"]::before,
  #rm2:checked ~ .rm-strip label[for="rm2"]::before,
  #rm3:checked ~ .rm-strip label[for="rm3"]::before,
  #rm4:checked ~ .rm-strip label[for="rm4"]::before,
  #rm5:checked ~ .rm-strip label[for="rm5"]::before{ border-color:var(--brand); background:#fff; }

  .rm-panels{ margin-top:10px; }
  .rm-panel{ display:none; font-size:14px; line-height:1.55; color:#374151; }
  #rm1:checked ~ .rm-panels .p1,
  #rm2:checked ~ .rm-panels .p2,
  #rm3:checked ~ .rm-panels .p3,
  #rm4:checked ~ .rm-panels .p4,
  #rm5:checked ~ .rm-panels .p5{ display:block; }

  .rm-panel .tag{ display:inline-block; font-size:12px; font-weight:600; color:var(--brand);
    border:1px solid var(--brand); border-radius:999px; padding:2px 6px; margin-right:6px; }
</style>

<div class="landing">
  <h1>Hello there!</h1>
  <p class="lede">I’m a data scientist focused on making messy health data usable—clean pipelines, clear metrics, and results people can act on.</p>

  <section class="story">
    A recent meeting started with three dashboards and no agreement. I combined provider data, county context, and outcomes into one
    reproducible pipeline—and one honest chart. The debate ended, and the team aligned on the first fix. That’s my north star:
    <b>reliable data, simple communication, practical action</b>.

    <ul class="proof">
      <li><b>500k+</b> multi-site EHR/Medicaid rows standardized into an OMOP-style model</li>
      <li><b>~60%</b> reduction in prep time via streamlined ETL & automated geocoding</li>
      <li><b>+25%</b> improvement in clinical-text extraction accuracy with LLM-assisted QA</li>
    </ul>

    <div class="cta">
      <!-- <a class="btn primary" href="{{ '/projects/' | relative_url }}">See projects →</a> -->
      <a class="btn ghost" href="{{ '/assets/docs/Resume_Neogi.pdf' | relative_url }}" download target="_blank" rel="noopener">Download resume →</a>
      <a class="btn ghost" href="mailto:neogiamrita111@gmail.com?subject=Hello&body=Hi%20Amrita%2C">Get in touch →</a>
    </div>
  </section>

  <!-- Education: collapsible, two-column details -->
  <section class="edu">
    <h2><strong>Education</strong></h2>

    <div class="edu-grid">
      <!-- MS Data Science -->
      <div class="edu-card">
        <img src="/assets/images/logo/University_of_Arizona_logo.jpg" alt="University of Arizona logo">
        <details class="edu-details" open>
          <summary>
            <span class="edu-title">Master of Science, Data Science</span>
            <span class="edu-quick"><span>Tucson, AZ</span> · <span>Dec 2023</span> · <span>GPA: 4.0/4.0</span> <span class="caret">›</span></span>
          </summary>
          <div class="edu-content">
            <div>
              <div class="subhead">Selected courses</div>
              <ul class="courses-list">
                <li>Machine Learning & Predictive Modeling</li>
                <li>Causal Inference & Experimental Design</li>
                <li>Databases (SQL, BigQuery) & Data Engineering</li>
                <li>Cloud & Workflow Orchestration (Airflow)</li>
                <li>NLP for Clinical Text</li>
                <li>Statistical Computing with R/Python</li>
              </ul>
            </div>
            <div class="meta">
              <dl>
                <dt>Focus</dt><dd>Reproducible pipelines (Python/R/SQL), privacy-aware analytics</dd>
                <dt>Capstone</dt><dd>Clinical ETL → OMOP-style model, geocoding automation</dd>
                <dt>Recognition</dt><dd>GPA 4.0/4.0</dd>
              </dl>
            </div>
          </div>
        </details>
      </div>

      <!-- B.Tech Electrical Engineering -->
      <div class="edu-card">
        <img src="/assets/images/logo/UEM_logo.png" alt="University of Engineering and Management logo">
        <details class="edu-details">
          <summary>
            <span class="edu-title">Bachelor of Technology, Electrical Engineering</span>
            <span class="edu-quick"><span>Jaipur, India</span> · <span>May 2017</span> · <span>GPA: 7.66/10 (magna cum laude)</span> <span class="caret">›</span></span>
          </summary>
          <div class="edu-content">
            <div>
              <div class="subhead">Representative courses</div>
              <ul class="courses-list">
                <li>Signals & Systems; Control Theory</li>
                <li>Digital Logic & Microprocessors</li>
                <li>Power Systems & Machines</li>
                <li>Numerical Methods; Probability & Stats</li>
                <li>Programming (C/C++), MATLAB</li>
              </ul>
            </div>
            <div class="meta">
              <dl>
                <dt>Theme</dt><dd>Systems thinking → transition to data science</dd>
                <dt>Honors</dt><dd>Magna cum laude</dd>
              </dl>
            </div>
          </div>
        </details>
      </div>
    </div>
  </section>

  <!-- Career Roadmap: playful, keyboard-accessible stepper -->
  <section class="road" aria-labelledby="roadmap-title">
    <h2 id="roadmap-title"><strong>Career Roadmap</strong></h2>
    <div class="rm">
      <!-- State radios -->
      <input type="radio" name="rm" id="rm1" checked>
      <input type="radio" name="rm" id="rm2">
      <input type="radio" name="rm" id="rm3">
      <input type="radio" name="rm" id="rm4">
      <input type="radio" name="rm" id="rm5">

      <!-- Clickable steps -->
      <div class="rm-strip" role="tablist" aria-label="Career steps">
        <div class="rm-track" aria-hidden="true"></div>

        <label class="rm-node" for="rm1" role="tab" aria-controls="panel-1">🎓 B.Tech — Electrical Eng.</label>
        <label class="rm-node" for="rm2" role="tab" aria-controls="panel-2">💻 SDE — TCS</label>
        <label class="rm-node" for="rm3" role="tab" aria-controls="panel-3">📊 M.S. — Data Science</label>
        <label class="rm-node" for="rm4" role="tab" aria-controls="panel-4">🔬 Graduate Research Asst.</label>
        <label class="rm-node" for="rm5" role="tab" aria-controls="panel-5">🏥 ARID Lab — DS/Analyst</label>
      </div>

      <!-- Panels -->
      <div class="rm-panels">
        <div id="panel-1" class="rm-panel p1">
          <span class="tag">Foundation</span> Systems thinking, control, and computation. This set the discipline for how I approach messy data and complex pipelines today.
        </div>
        <div id="panel-2" class="rm-panel p2">
          <span class="tag">Engineering</span> Built enterprise ETL and data products at scale (Teradata/Informatica → Python/Unix). Learned reliability, SLAs, and clear handoffs.
        </div>
        <div id="panel-3" class="rm-panel p3">
          <span class="tag">Analysis</span> Formal training in ML, causal inference, and data engineering. Focused on reproducible Python/R/SQL workflows and privacy-aware analytics.
        </div>
        <div id="panel-4" class="rm-panel p4">
          <span class="tag">Research</span> Prototyped pipelines, experiments, and dashboards that made results more actionable for teams (without over-promising).
        </div>
        <div id="panel-5" class="rm-panel p5">
          <span class="tag">Impact</span> Standardized 500k+ EHR/Medicaid rows to an OMOP-style model, automated geocoding, and shipped dashboards that informed care decisions.
        </div>
      </div>
    </div>
  </section>

  <p class="foot">Thanks for visiting—feel free to explore and connect.</p>
</div>

<!-- Optional: one-open-at-a-time behavior for the education accordion -->
<script>
  document.addEventListener('click', (e) => {
    const det = e.target.closest('.edu-details');
    if (!det) return;
    document.querySelectorAll('.edu-details').forEach(d => { if (d !== det) d.open = false; });
  });
</script>
