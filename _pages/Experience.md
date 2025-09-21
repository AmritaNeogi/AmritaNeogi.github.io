---
layout: single
title:
permalink: /Experience/
date: 2023-09-02
categories: pages
author_profile: false   # no author sidebar on this page
sidebar: false
classes: wide
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#fff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
    --bg:#f8fafc;

    /* working widths */
    --wrap-max: 1140px;     /* inner content width */
  }

  /* ============ FLUSH-LEFT LAYOUT (kills theme’s left gutter) ============ */
  .page--flush .page__inner-wrap{ padding-left:0 !important; }
  .page--flush .page__content{ margin-left:0 !important; }
  @media (min-width:1024px){
    .page--flush .sidebar,
    .page--flush .page__sidebar{ display:none !important; }
    .page--flush .page{ display:flex !important; }
    .page--flush .page__content{ flex:1 1 auto !important; }
  }

  /* ============ Page wrapper ============ */
  .exp-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    width:100%;
    max-width: var(--wrap-max);
    margin-left:0;          /* << flush to the left */
    margin-right:auto;
    padding:0 12px;         /* small right gutter so borders don’t kiss edge */
    color:var(--ink);
    box-sizing:border-box;
  }
  .exp-wrap h1{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  .exp-wrap .sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

  /* jump nav */
  .jump{ position:sticky; top:0; z-index:1; background:var(--bg); padding:8px 0; margin-bottom:.6rem; border-bottom:1px solid var(--line); }
  .pills{ display:flex; gap:8px; flex-wrap:wrap; }
  .pill-link{
    text-decoration:none; color:var(--brand); border:1px solid var(--brand);
    background:#fff; padding:6px 10px; border-radius:999px; font-weight:600; font-size:13px;
  }

  /* role cards */
  details.role{
    border:1px solid var(--line); border-radius:14px; background:var(--card);
    box-shadow:0 1px 0 var(--ring); margin:.7rem 0; overflow:hidden;
  }
  .role > summary{
    list-style:none; cursor:pointer; outline:none;
    display:grid; grid-template-columns: 44px 1fr auto; gap:12px; align-items:center;
    padding:12px 14px;
  }
  .role > summary::-webkit-details-marker{ display:none; }
  .logo{ width:44px; height:44px; border-radius:8px; border:1px solid var(--line); object-fit:cover; background:#fff; }
  .head{ display:flex; flex-direction:column; gap:2px; }
  .title{ font-weight:700; font-size:16px; color:var(--ink); }
  .org{ color:var(--muted); font-size:13.5px; }
  .dates{ color:var(--muted); font-size:13.5px; white-space:nowrap; }

  /* expanded content */
  .content{
    border-top:1px solid var(--line);
    display:grid; grid-template-columns: minmax(0,1fr) minmax(0,1fr);
    gap:16px; padding:12px 16px 14px; font-size:14.75px; line-height:1.6;
    overflow-wrap:anywhere; box-sizing:border-box;
  }
  @media (max-width:860px){ .content{ grid-template-columns:1fr; } }

  .highlights, .full{
    background:#fff; border:1px dashed #e9edf3; border-radius:10px; padding:10px 12px; margin:0;
  }
  .highlights h4, .full h4{ margin:.1rem 0 .35rem; color:var(--brand); font-size:14.5px; }
  ul.tight{ margin:.2rem 0 0; padding-left:16px; }
  ul.tight li{ margin:.2rem 0; }
  .tagrow{ display:flex; gap:6px; flex-wrap:wrap; margin-top:.5rem; }
  .tag{ font-size:12px; color:#0f172a; background:#eef3f8; border:1px solid #dbe2ea; padding:3px 8px; border-radius:999px; }
  .backtop{ text-align:right; margin:.3rem 0 .2rem; }
  .backtop a{ font-size:12.5px; color:var(--brand); text-decoration:none; }
</style>

<div class="exp-wrap page--flush" id="top">
  <h1>Experience</h1>
  <p class="sub">Click a role to expand. Summaries first; full responsibilities inside each card.</p>

  <!-- Jump navigation -->
  <nav class="jump" aria-label="Jump navigation">
    <div class="pills">
      <a class="pill-link" href="#arid-dsm">Data Science Manager — ARID Lab</a>
      <a class="pill-link" href="#arid-gra">Graduate Research Assistant — UArizona</a>
      <a class="pill-link" href="#tcs-sde">Software Development Engineer — TCS</a>
    </div>
  </nav>

  <!-- Role 1 -->
  <details class="role" id="arid-dsm" open>
    <summary>
      <img class="logo" src="/assets/images/logo/arid.jpg" alt="ARID Lab logo">
      <div class="head">
        <div class="title">Data Science Manager</div>
        <div class="org">ARID Lab, Dept. of Pediatrics, University of Arizona — Tucson, AZ</div>
      </div>
      <div class="dates">Mar 2024 – Present</div>
    </summary>
    <div class="content">
      <div class="highlights">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Lead multi-site health-data pipelines: onboarding, standardization (OMOP-style), QA.</li>
          <li>Cut prep time and raised data reliability via processing standards (CB2).</li>
          <li>Partner with clinicians/biostatisticians; deliver decision-ready results.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Python/R/SQL</span><span class="tag">EHR/Medicaid</span><span class="tag">OMOP</span>
          <span class="tag">Causal Inference</span><span class="tag">PHI/PII</span><span class="tag">Orchestration</span>
        </div>
      </div>
      <div class="full">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li><b>Pipeline management:</b> onboard sites; integrate feeds; maintain reproducible ingestion/standardization/validation flows.</li>
          <li><b>Process optimization:</b> define CB2 protocols; streamline extraction, cleaning, consolidation; track SLAs.</li>
          <li><b>Data quality & compliance:</b> OHDSI/CDM mappings; profiling/audits; HIPAA-aligned PHI/PII handling.</li>
          <li><b>Stakeholder coordination:</b> lead touchpoints; align deliverables across partners.</li>
          <li><b>Continuous improvement:</b> evaluate methods; document standards; mentor on testing & reproducibility.</li>
        </ul>
      </div>
    </div>
    <div class="backtop"><a href="#top">Back to top ↑</a></div>
  </details>

  <!-- Role 2 -->
  <details class="role" id="arid-gra">
    <summary>
      <img class="logo" src="/assets/images/logo/arid.jpg" alt="University of Arizona logo">
      <div class="head">
        <div class="title">Graduate Research Assistant</div>
        <div class="org">University of Arizona — Dept. of Pediatrics (ARID Lab)</div>
      </div>
      <div class="dates">Feb 2023 – Dec 2023</div>
    </summary>
    <div class="content">
      <div class="highlights">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Built analytical databases in REDCap; standardized multi-source data → ~15% faster prep.</li>
          <li>Authored Python pipelines (MariaDB→Postgres) mapped to OMOP with secure transfers.</li>
          <li>Linked MTurk/REDCap survey outputs; R analyses cut post-survey processing by ~20%.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Python</span><span class="tag">R</span><span class="tag">SQL</span>
          <span class="tag">REDCap</span><span class="tag">Amazon Athena</span><span class="tag">OMOP</span>
        </div>
      </div>
      <div class="full">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li>Extracted/standardized data to analytical REDCap projects with reproducible metadata.</li>
          <li>Optimized database programs for low-latency queries and reliable modeling.</li>
          <li>Executed rigorous cleaning & linkage with full change logs.</li>
          <li>Built secure pipelines (MariaDB→PostgreSQL) adhering to OMOP tables.</li>
          <li>Ran statistical tests/logistic models to profile care patterns and engagement drivers.</li>
        </ul>
      </div>
    </div>
    <div class="backtop"><a href="#top">Back to top ↑</a></div>
  </details>

  <!-- Role 3 -->
  <details class="role" id="tcs-sde">
    <summary>
      <img class="logo" src="/assets/images/logo/TCS_Logo.jpg" alt="TCS logo">
      <div class="head">
        <div class="title">Software Development Engineer (ETL Developer)</div>
        <div class="org">Tata Consultancy Services — Financial Services (EDW/Teradata/Mainframe)</div>
      </div>
      <div class="dates">Mar 2018 – Jul 2022</div>
    </summary>
    <div class="content">
      <div class="highlights">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Built/maintained PowerCenter 9.x pipelines across mainframe, flat files, Teradata, EDW.</li>
          <li>Performance-tuned long CI/CD jobs → ~50% faster; improved reliability.</li>
          <li>Led 12-member ETL team; code reviews, migration discipline, quality gates.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Informatica PowerCenter</span><span class="tag">Teradata/SQL</span><span class="tag">Unix/Shell</span>
          <span class="tag">PL/SQL</span><span class="tag">CI/CD</span><span class="tag">AWS</span>
        </div>
      </div>
      <div class="full">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li>Developed complex mappings/worklets with reusable patterns → lower deployment time.</li>
          <li>Wrote Unix & PL/SQL validation suites; automated integrity checks for large feeds.</li>
          <li>Optimized source/target/mapping/session layers → runtime & cost reductions.</li>
          <li>Managed migration across Dev/Test/UAT/Prod; maintained auditability & rollback plans.</li>
          <li>Drove JIRA tracking, reviews, mentorship; improved delivery predictability.</li>
          <li>Delivered retrofit integrating 2.5M customer records with ~30% perf gain.</li>
        </ul>
      </div>
    </div>
    <div class="backtop"><a href="#top">Back to top ↑</a></div>
  </details>
</div>

<script>
/* open only one role at a time */
document.querySelectorAll('details.role').forEach(d => {
  d.addEventListener('toggle', () => {
    if (d.open) document.querySelectorAll('details.role').forEach(o => { if (o!==d) o.removeAttribute('open'); });
  });
});
</script>
