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
    max-width: 720px;      /* CENTER & NARROWER */
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
  .edu-grid{
    display:grid; gap:12px;
    grid-template-columns:repeat(1, minmax(260px, 1fr));   /* NOT CRAMPED */
  }
  @media (min-width:760px){ .edu-grid{ grid-template-columns:repeat(2, minmax(300px, 1fr)); } }
  .edu-card{
    display:grid; grid-template-columns:36px 1fr; gap:10px; align-items:center;
    border:1px solid #e5e7eb; border-radius:12px; padding:10px 12px; background:#fff; box-shadow:0 1px 0 var(--ring);
  }
  .edu-card img{ height:28px; width:28px; object-fit:contain; border-radius:4px; }
  .edu-title{ font-weight:600; font-size:15px; }
  .edu-meta{ color:var(--muted); font-size:13px; display:flex; gap:8px; flex-wrap:wrap; }
  .edu-desc{ font-size:13.5px; margin-top:3px; color:#374151; }
  .foot{ color:var(--muted); font-size:14px; margin-top:.8rem; }
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
      <!-- Update to your existing projects page -->
      <a class="btn primary" href="{{ '/projects/' | relative_url }}">See projects →</a>

      <!-- Resume + Email wired below (see notes) -->
      <a class="btn ghost" href="{{ '/assets/docs/Resume_Neogi.pdf' | relative_url }}" download target="_blank" rel="noopener">Download resume →</a>
      <a class="btn ghost" href="mailto:neogiamrita111@gmail.com?subject=Hello&body=Hi%20Amrita%2C">Get in touch →</a>
    </div>
  </section>

  <section class="edu">
    <h2><strong>Education</strong></h2>

    <div class="edu-grid">
      <div class="edu-card">
        <img src="/assets/images/logo/University_of_Arizona_logo.jpg" alt="University of Arizona logo">
        <div>
          <div class="edu-title">Master of Science, Data Science</div>
          <div class="edu-meta"><span>Tucson, AZ</span><span>Dec 2023</span><span>GPA: 4.0/4.0</span></div>
          <div class="edu-desc">Focus: reproducible pipelines (Python/R/SQL), causal inference, ML, privacy-aware analytics.</div>
        </div>
      </div>

      <div class="edu-card">
        <img src="/assets/images/logo/UEM_logo.png" alt="University of Engineering and Management logo">
        <div>
          <div class="edu-title">Bachelor of Technology, Electrical Engineering</div>
          <div class="edu-meta"><span>Jaipur, India</span><span>May 2017</span><span>GPA: 7.66/10 (magna cum laude)</span></div>
          <div class="edu-desc">Foundations in systems thinking and computation; transitioned to data science.</div>
        </div>
      </div>
    </div>
  </section>

  <p class="foot">Thanks for visiting—feel free to explore and connect.</p>
</div>
