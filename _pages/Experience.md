---
layout: single
title:
permalink: /Experience/
date: 2023-09-02
categories: pages
author_profile: false
sidebar: false
classes: wide
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#fff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
    --bg:#f8fafc;
  }

  /* ===== Hard override Minimal Mistakes shell on layout:single ===== */
  @media (min-width: 1024px){
    /* 1) kill the left sidebar column and flex layout */
    .layout--single .sidebar,
    .layout--single .page__sidebar{ display:none !important; }
    .layout--single .page{ display:block !important; max-width:none !important; width:100% !important; }

    /* 2) remove inner paddings/margins that create the left gap */
    .layout--single .page__inner-wrap{ padding-left:0 !important; padding-right:0 !important; }
    .layout--single .page__content{
      max-width:none !important;
      width:100% !important;
      margin:0 !important;
      padding:0 !important;
    }
  }

  /* ===== Page layout pinned LEFT with a small gutter ===== */
  .exp-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    width:100%;
    /* small left gutter so borders never kiss the viewport */
    padding-left: clamp(12px, 2vw, 24px);
    padding-right: clamp(12px, 2vw, 24px);
    box-sizing:border-box;
    color:var(--ink);
  }

  h1.page-title{
    color:var(--brand);
    margin:.25rem 0 .5rem;
    font-size: clamp(26px, 3.2vw, 34px);
    font-weight: 800;
  }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

  /* sticky jump links (optional) */
  .jump{ position:sticky; top:0; z-index:1; background:var(--bg); padding:8px 0; border-bottom:1px solid var(--line); }
  .pills{ display:flex; gap:8px; flex-wrap:wrap; }
  .pill-link{
    text-decoration:none; color:var(--brand); border:1px solid var(--brand);
    background:#fff; padding:6px 10px; border-radius:999px; font-weight:600; font-size:13px;
    white-space:nowrap;
  }

  /* ===== Wider role cards (left aligned) ===== */
  .roles{ max-width:none; width:min(1400px, 100%); }  /* make rows wider; never exceed page */
  details.role{
    border:1px solid var(--line); border-radius:14px; background:var(--card);
    box-shadow:0 1px 0 var(--ring);
    margin:.8rem 0;
    overflow:hidden;
    width:100%;
  }
  .role > summary{
    list-style:none; cursor:pointer; outline:none;
    display:grid; grid-template-columns: 46px 1fr auto;
    gap:12px; align-items:center; padding:12px 16px;
  }
  .role > summary::-webkit-details-marker{ display:none; }
  .logo{ width:46px; height:46px; border-radius:8px; border:1px solid var(--line); object-fit:cover; background:#fff; }
  .head{ display:flex; flex-direction:column; gap:2px; min-width:0; }
  .title{ font-weight:800; font-size:16.5px; color:var(--ink); }
  .org{ color:var(--muted); font-size:13.5px; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
  .dates{ color:var(--muted); font-size:13.5px; white-space:nowrap; }

  /* Expanded content — 2 equal columns, never overflow */
  .content{
    border-top:1px solid var(--line);
    display:grid; grid-template-columns: minmax(0,1fr) minmax(0,1fr);
    gap:16px; padding:12px 16px 14px;
    font-size:15px; line-height:1.6;
    overflow-wrap:anywhere; box-sizing:border-box; width:100%;
  }
  @media (max-width: 860px){ .content{ grid-template-columns: 1fr; } }

  .highlights, .full{
    background:#fff; border:1px dashed #e9edf3; border-radius:10px; padding:10px 12px;
  }
  .highlights h4, .full h4{ margin:.1rem 0 .35rem; color:var(--brand); font-size:14.5px; }
  ul.tight{ margin:.2rem 0 0; padding-left:16px; }
  ul.tight li{ margin:.2rem 0; }
  .tagrow{ display:flex; gap:6px; flex-wrap:wrap; margin-top:.5rem; }
  .tag{ font-size:12px; color:#0f172a; background:#eef3f8; border:1px solid #dbe2ea; padding:3px 8px; border-radius:999px; }
  .backtop{ text-align:right; margin-top:.3rem; }
  .backtop a{ font-size:12.5px; color:var(--brand); text-decoration:none; }
</style>

<div class="exp-wrap" id="top">
  <h1 class="page-title">Experience</h1>
  <p class="page-sub">Click a role to expand. Summaries first; full responsibilities inside each card.</p>

  <!-- optional jump navigation -->
  <nav class="jump" aria-label="Jump navigation">
    <div class="pills">
      <a class="pill-link" href="#arid-dsm">Data Science Manager — ARID Lab</a>
      <a class="pill-link" href="#arid-gra">Graduate Research Assistant — UArizona</a>
      <a class="pill-link" href="#tcs-sde">Software Development Engineer — TCS</a>
    </div>
  </nav>

  <div class="roles">
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
            <li>Lead multi-site health-data pipelines: onboarding, standardization (OMOP-style), and QA.</li>
            <li>Cut prep time and raised reliability via documented processing standards with CB2.</li>
            <li>Partner with clinicians/biostatisticians; communicate results in decision-ready formats.</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Python/R/SQL</span><span class="tag">EHR/Medicaid</span><span class="tag">OMOP</span>
            <span class="tag">Causal Inference</span><span class="tag">PHI/PII</span><span class="tag">Airflow-style orchestration</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li><b>Pipeline management:</b> onboard clinical sites; integrate feeds; maintain reproducible ingestion/standardization/validation flows.</li>
            <li><b>Process optimization:</b> define CB2 protocols; streamline extraction/cleaning/consolidation; track SLAs.</li>
            <li><b>Data quality & compliance:</b> enforce CDM mappings; profiling/audits; HIPAA-aligned PHI/PII handling.</li>
            <li><b>Stakeholder coordination:</b> align deliverables across internal/external partners.</li>
            <li><b>Continuous improvement:</b> document standards; mentor students on testing & reproducibility.</li>
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
            <li>Built analytical databases in REDCap; standardized multi-source data → <i>~15% faster prep</i>.</li>
            <li>Python pipelines (MariaDB→Postgres) mapped to OMOP; secure transfers with audit logs.</li>
            <li>Linked MTurk/REDCap outputs; R analyses reduced post-survey processing by <i>~20%</i>.</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Python</span><span class="tag">R</span><span class="tag">SQL</span>
            <span class="tag">REDCap</span><span class="tag">Amazon Athena</span><span class="tag">OMOP</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li>Standardized data to analytical REDCap projects with reproducible metadata.</li>
            <li>Optimized database programs for low-latency queries and reliable downstream modeling.</li>
            <li>Cleaning & linkage with full change logs for reproducibility.</li>
            <li>Secure pipelines (MariaDB→PostgreSQL) adhering to OMOP tables and transfer policies.</li>
            <li>Statistical tests/logistic models to profile care patterns and engagement drivers.</li>
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
            <li>Performance-tuned long CI/CD jobs; delivered <i>~50%</i> faster runs and higher reliability.</li>
            <li>Led a 12-member ETL team; enforced code reviews, migration discipline, quality gates.</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Informatica PowerCenter</span><span class="tag">Teradata/SQL</span><span class="tag">Unix/Shell</span>
            <span class="tag">PL/SQL</span><span class="tag">CI/CD</span><span class="tag">AWS</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li>Developed complex mappings/worklets with reusable patterns → faster deployments.</li>
            <li>Unix shell & PL/SQL validation suites; automated integrity checks for large feeds.</li>
            <li>Optimized source/target/mapping/session layers → lower runtime and infra costs.</li>
            <li>Managed migration across Dev/Test/UAT/Prod; maintained auditability and rollback plans.</li>
            <li>Drove JIRA tracking, reviews, mentorship; fewer defects and better predictability.</li>
            <li>Delivered retrofit integrating 2.5M customer records with ~30% perf gain.</li>
          </ul>
        </div>
      </div>
      <div class="backtop"><a href="#top">Back to top ↑</a></div>
    </details>
  </div>
</div>
