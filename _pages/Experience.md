---
layout: single
title:
permalink: /Experience/
date: 2023-09-02
categories: pages
author_profile: false
sidebar: false
classes: exp-flush  # << key: lets us target just this page
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#fff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
  }

  /* ====== KILL THE LEFT GUTTER + CENTERING (THIS PAGE ONLY) ====== */
  .exp-flush .page__inner-wrap,
  .exp-flush .page__content{
    max-width: none !important;
    width: 100% !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
    padding-left: 0 !important;
    padding-right: 0 !important;
  }
  .exp-flush .sidebar,
  .exp-flush .page__sidebar{ display:none !important; }

  /* ====== Simple page styles ====== */
  .exp-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    color:var(--ink);
    width:100%;
    /* optional: add a tiny right gutter so borders don’t kiss browser edge */
    padding-right:12px; box-sizing:border-box;
  }
  h1.page-title{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

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
  .org,.dates{ color:var(--muted); font-size:13.5px; }
  .dates{ white-space:nowrap; }

  .content{
    border-top:1px solid var(--line);
    display:grid; grid-template-columns: minmax(0,1fr) minmax(0,1fr);
    gap:16px; padding:12px 16px 14px; font-size:14.75px; line-height:1.6;
  }
  @media (max-width:860px){ .content{ grid-template-columns:1fr; } }

  .box{ border:1px dashed #e9edf3; border-radius:10px; padding:10px 12px; }
  .box h4{ margin:.1rem 0 .35rem; color:var(--brand); font-size:14.5px; }
  ul.tight{ margin:.2rem 0 0; padding-left:16px; }
  ul.tight li{ margin:.2rem 0; }
  .tagrow{ display:flex; gap:6px; flex-wrap:wrap; margin-top:.5rem; }
  .tag{ font-size:12px; color:#0f172a; background:#eef3f8; border:1px solid #dbe2ea; padding:3px 8px; border-radius:999px; }
</style>

<div class="exp-wrap">
  <h1 class="page-title">Experience</h1>
  <p class="page-sub">Click a role to expand. Summaries first; full responsibilities inside each card.</p>

  <!-- Role 1 -->
  <details class="role" open>
    <summary>
      <img class="logo" src="/assets/images/logo/arid.jpg" alt="ARID Lab">
      <div class="head">
        <div class="title">Data Science Manager</div>
        <div class="org">ARID Lab, Dept. of Pediatrics, University of Arizona — Tucson, AZ</div>
      </div>
      <div class="dates">Mar 2024 – Present</div>
    </summary>
    <div class="content">
      <div class="box">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Lead multi-site health-data pipelines: onboarding, OMOP-style standardization, QA.</li>
          <li>Raised reliability and cut prep time via documented CB2 processing standards.</li>
          <li>Partner with clinicians/biostats; deliver decision-ready results.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Python/R/SQL</span><span class="tag">EHR/Medicaid</span><span class="tag">OMOP</span>
          <span class="tag">Causal Inference</span><span class="tag">PHI/PII</span><span class="tag">Orchestration</span>
        </div>
      </div>
      <div class="box">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li><b>Pipeline mgmt:</b> onboard sites; integrate feeds; maintain reproducible ingestion/standardization/validation flows.</li>
          <li><b>Optimization:</b> define CB2 protocols; streamline cleaning & consolidation; track SLAs.</li>
          <li><b>Quality & compliance:</b> OHDSI/CDM mappings; profiling/audits; HIPAA-aligned PHI/PII handling.</li>
          <li><b>Stakeholders:</b> lead touchpoints; align deliverables across partners; mentor on testing & reproducibility.</li>
        </ul>
      </div>
    </div>
  </details>

  <!-- Role 2 -->
  <details class="role">
    <summary>
      <img class="logo" src="/assets/images/logo/arid.jpg" alt="UArizona">
      <div class="head">
        <div class="title">Graduate Research Assistant</div>
        <div class="org">University of Arizona — Dept. of Pediatrics (ARID Lab)</div>
      </div>
      <div class="dates">Feb 2023 – Dec 2023</div>
    </summary>
    <div class="content">
      <div class="box">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Standardized multi-source data in REDCap → ~15% faster prep.</li>
          <li>Python pipelines (MariaDB→Postgres) mapped to OMOP with secure transfers.</li>
          <li>Linked MTurk/REDCap; R analyses cut post-survey processing ~20%.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Python</span><span class="tag">R</span><span class="tag">SQL</span>
          <span class="tag">REDCap</span><span class="tag">Amazon Athena</span><span class="tag">OMOP</span>
        </div>
      </div>
      <div class="box">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li>Extracted/standardized data to analytical REDCap with reproducible metadata.</li>
          <li>Optimized DB programs for low-latency queries & reliable modeling.</li>
          <li>Rigorous cleaning/linkage with full change logs.</li>
          <li>Secure MariaDB→PostgreSQL pipelines adhering to OMOP tables.</li>
        </ul>
      </div>
    </div>
  </details>

  <!-- Role 3 -->
  <details class="role">
    <summary>
      <img class="logo" src="/assets/images/logo/TCS_Logo.jpg" alt="TCS">
      <div class="head">
        <div class="title">Software Development Engineer (ETL Developer)</div>
        <div class="org">Tata Consultancy Services — Financial Services (EDW/Teradata/Mainframe)</div>
      </div>
      <div class="dates">Mar 2018 – Jul 2022</div>
    </summary>
    <div class="content">
      <div class="box">
        <h4>Highlights</h4>
        <ul class="tight">
          <li>Built/maintained PowerCenter 9.x pipelines (mainframe, flat files, Teradata, EDW).</li>
          <li>Perf-tuned CI/CD jobs → ~50% faster; improved reliability.</li>
          <li>Led 12-member ETL team; code reviews, migration discipline, quality gates.</li>
        </ul>
        <div class="tagrow">
          <span class="tag">Informatica PowerCenter</span><span class="tag">Teradata/SQL</span><span class="tag">Unix/Shell</span>
          <span class="tag">PL/SQL</span><span class="tag">CI/CD</span><span class="tag">AWS</span>
        </div>
      </div>
      <div class="box">
        <h4>Scope & Responsibilities</h4>
        <ul class="tight">
          <li>Reusable mappings/worklets → faster deployments and fewer defects.</li>
          <li>Unix & PL/SQL validation suites; automated integrity checks.</li>
          <li>Optimized source/target/mapping/session layers → runtime & cost down.</li>
          <li>Managed Dev/Test/UAT/Prod migrations with full auditability.</li>
        </ul>
      </div>
    </div>
  </details>
</div>

<script>
/* only one card open at a time */
document.querySelectorAll('details.role').forEach(d => {
  d.addEventListener('toggle', () => {
    if (d.open) document.querySelectorAll('details.role').forEach(o => { if (o!==d) o.removeAttribute('open'); });
  });
});
</script>
