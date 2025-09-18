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

<!-- Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

<!-- Page Styles (inline for easy drop-in) -->
<style>
  :root {
    --brand:#336699;
    --ink:#1f2937;
    --muted:#6b7280;
    --bg:#f8fafc;
    --card:#ffffff;
    --ring:rgba(51,102,153,0.15);
  }
  * { box-sizing: border-box; }
  body, .page, .post {
    font-family: 'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color: var(--ink);
  }
  .hero { padding: 1.25rem 0 0.75rem; }
  .hero h1 {
    margin: 0 0 0.5rem;
    font-size: clamp(28px, 4vw, 40px);
    line-height: 1.15;
    color: var(--brand);
    letter-spacing: -0.5px;
  }
  .hero p.lede {
    margin: 0.25rem 0 0;
    font-size: clamp(16px, 2.25vw, 18px);
    line-height: 1.6;
    color: var(--ink);
  }
  .story {
    margin: 1.25rem 0 0.75rem;
    padding: 1rem 1rem;
    background: var(--bg);
    border: 1px solid #e5e7eb;
    border-radius: 12px;
  }
  .proof {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
    margin: 0.75rem 0 0;
    padding: 0;
    list-style: none;
  }
  .proof li {
    background: var(--card);
    border: 1px solid #e5e7eb;
    border-radius: 12px;
    padding: 10px 12px;
  }
  .proof b { color: var(--brand); }
  @media (min-width: 760px) {
    .proof { grid-template-columns: repeat(3, 1fr); }
  }
  .edu {
    margin: 1.25rem 0 0.25rem;
  }
  .edu h2 {
    color: var(--brand);
    margin-bottom: 0.6rem;
    font-size: clamp(22px, 3vw, 28px);
  }
  .edu-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 14px;
  }
  @media (min-width: 680px) {
    .edu-grid { grid-template-columns: 1fr 1fr; }
  }
  .edu-card {
    display: grid;
    grid-template-columns: 40px 1fr;
    gap: 12px;
    align-items: center;
    background: var(--card);
    border: 1px solid #e5e7eb;
    border-radius: 14px;
    padding: 12px;
    box-shadow: 0 1px 0 var(--ring);
  }
  .edu-card img {
    height: 32px; width: 32px; object-fit: contain;
    border-radius: 4px;
  }
  .edu-title { font-weight: 700; }
  .edu-meta {
    display: flex; gap: 10px; flex-wrap: wrap;
    color: var(--muted); font-size: 14px;
  }
  .cta {
    margin-top: 0.8rem; display: flex; gap: 10px; flex-wrap: wrap;
  }
  .btn {
    display: inline-block;
    padding: 8px 12px;
    border-radius: 10px;
    text-decoration: none;
    font-weight: 600;
    font-size: 14.5px;
  }
  .btn.primary { background: var(--brand); color: #fff; }
  .btn.ghost { border: 1px solid var(--brand); color: var(--brand); background: #fff; }
</style>

<section class="hero">
  <h1>Hello there!</h1>
  <p class="lede">
    I’m a data scientist focused on making messy health data usable—clean pipelines, clear metrics, and results people can act on.
  </p>
</section>

<section class="story">
  <p style="margin:0;">
    A recent meeting started with three dashboards and no agreement. I combined provider data, county context, and outcomes into one
    reproducible pipeline—and one honest chart. The debate ended, and the team aligned on the first fix. That’s my north star:
    <b>reliable data, simple communication, practical action</b>.
  </p>
  <ul class="proof">
    <li><b>500k+</b> multi-site EHR/Medicaid rows standardized into an OMOP-style model</li>
    <li><b>~60%</b> reduction in prep time via streamlined ETL & automated geocoding</li>
    <li><b>+25%</b> improvement in clinical-text extraction accuracy with LLM-assisted QA</li>
  </ul>
  <div class="cta">
    <a class="btn primary" href="/projects">See projects →</a>
    <a class="btn ghost" href="/resume.pdf">Download resume →</a>
    <a class="btn ghost" href="/contact">Get in touch →</a>
  </div>
</section>

<section class="edu">
  <h2><strong>Education</strong></h2>
  <div class="edu-grid">
    <div class="edu-card">
      <img src="/assets/images/logo/University_of_Arizona_logo.jpg" alt="University of Arizona logo">
      <div>
        <div class="edu-title">Master of Science, Data Science</div>
        <div class="edu-meta">
          <span>Tucson, AZ</span>
          <span>Dec 2023</span>
          <span>GPA: 4.0/4.0</span>
        </div>
        <div style="margin-top:4px; font-size:14.5px;">
          Focus: reproducible pipelines (Python/R/SQL), causal inference, ML, privacy-aware analytics.
        </div>
      </div>
    </div>

    <div class="edu-card">
      <img src="/assets/images/logo/UEM_logo.png" alt="University of Engineering and Management logo">
      <div>
        <div class="edu-title">Bachelor of Technology, Electrical Engineering</div>
        <div class="edu-meta">
          <span>Jaipur, India</span>
          <span>May 2017</span>
          <span>GPA: 7.66/10 (magna cum laude)</span>
        </div>
        <div style="margin-top:4px; font-size:14.5px;">
          Foundations in systems thinking and computation; transitioned to data science.
        </div>
      </div>
    </div>
  </div>
</section>

<section style="margin-top:1rem;">
  <p style="margin:0; color:var(--muted);">
    Thanks for visiting—feel free to explore and connect.
  </p>
</section>
