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

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#fff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
    --bg:#f8fafc;
  }

  /* ===== Hard override Minimal Mistakes shell on layout:single ===== */
  @media (min-width: 1024px){
    .layout--single .sidebar,
    .layout--single .page__sidebar{ display:none !important; }
    .layout--single .page{ display:block !important; max-width:none !important; width:100% !important; }
    .layout--single .page__inner-wrap{ padding-left:0 !important; padding-right:0 !important; }
    .layout--single .page__content{
      max-width:none !important;
      width:100% !important;
      margin:0 !important;
      padding:0 !important;
    }
  }

  .exp-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    width:100%;
    padding-left: clamp(12px, 2vw, 24px);
    padding-right: clamp(12px, 2vw, 24px);
    box-sizing:border-box;
    color:var(--ink);
    max-width: 1600px;
    margin: 0 auto;
    padding-top: 2rem;
    padding-bottom: 2rem;
  }

  h1.page-title{
    color:var(--brand);
    margin:.25rem 0 .5rem;
    font-size: clamp(26px, 3.2vw, 34px);
    font-weight: 800;
  }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .8rem; }

  .jump{ position:sticky; top:0; z-index:1; background:var(--bg); padding:8px 0; border-bottom:1px solid var(--line); margin-bottom: 1rem; }
  .pills{ display:flex; gap:8px; flex-wrap:wrap; }
  .pill-link{
    text-decoration:none; color:var(--brand); border:1px solid var(--brand);
    background:#fff; padding:6px 10px; border-radius:999px; font-weight:600; font-size:13px;
    white-space:nowrap;
    transition: all 0.2s;
  }
  .pill-link:hover {
    background: var(--brand);
    color: white;
  }

  .roles{ max-width:none; width:100%; }
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
    transition: background 0.2s;
  }
  .role > summary:hover {
    background: #fafbfc;
  }
  .role > summary::-webkit-details-marker{ display:none; }
  .logo{ width:46px; height:46px; border-radius:8px; border:1px solid var(--line); object-fit:cover; background:#fff; }
  .head{ display:flex; flex-direction:column; gap:2px; min-width:0; }
  .title{ font-weight:800; font-size:16.5px; color:var(--ink); }
  .org{ color:var(--muted); font-size:13.5px; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
  .dates{ color:var(--muted); font-size:13.5px; white-space:nowrap; }

  .content{
    border-top:1px solid var(--line);
    display:grid; grid-template-columns: minmax(0,1fr) minmax(0,1fr);
    gap:16px; padding:12px 14px;
    font-size:15px; line-height:1.6;
    overflow-wrap:anywhere; box-sizing:border-box; width:100%;
  }
  @media (max-width: 860px){ .content{ grid-template-columns: 1fr; } }

  .highlights, .full{
    background:#fff; border:1px dashed #e9edf3; border-radius:10px; padding:10px 12px;
    margin: 0;
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
  }
  .highlights h4, .full h4{ margin:.1rem 0 .35rem; color:var(--brand); font-size:14.5px; }
  ul.tight{ margin:.2rem 0 0; padding-left:16px; }
  ul.tight li{ margin:.2rem 0; }
  .tagrow{ display:flex; gap:6px; flex-wrap:wrap; margin-top:.5rem; }
  .tag{ font-size:12px; color:#0f172a; background:#eef3f8; border:1px solid #dbe2ea; padding:3px 8px; border-radius:999px; }
  .backtop{ text-align:right; margin-top:.3rem; padding: 8px 16px; }
  .backtop a{ font-size:12.5px; color:var(--brand); text-decoration:none; }
  .backtop a:hover { text-decoration: underline; }

  .content > *{
    min-width:0;
    overflow-wrap: anywhere;
  }
</style>

<div class="exp-wrap" id="top">
  <h1 class="page-title">Experience</h1>
  <p class="page-sub">Click a role to expand. Summaries first; full responsibilities inside each card.</p>

  <nav class="jump" aria-label="Jump navigation">
    <div class="pills">
      <a class="pill-link" href="#arid-ds">Data Scientist — ARID Lab</a>
      <a class="pill-link" href="#arid-gra">Graduate Research Assistant — UArizona</a>
      <a class="pill-link" href="#tcs-sde">Software Development Engineer — TCS</a>
    </div>
  </nav>

  <div class="roles">
    <!-- Role 1: Data Science Manager -->
    <details class="role" id="arid-ds" open>
      <summary>
        <img class="logo" src="/assets/images/logo/arid.jpg" alt="ARID Lab logo">
        <div class="head">
          <div class="title">Data Science Manager</div>
          <div class="org">ARID Lab, University of Arizona — Tucson, AZ</div>
        </div>
        <div class="dates">Feb 2024 – Oct 2025</div>
      </summary>

      <div class="content">
        <div class="highlights">
          <h4>Highlights</h4>
          <ul class="tight">
            <li>Built and deployed ML models (XGBoost, survival analysis, ClinicalBERT NLP) on 500K+ healthcare records achieving 83% AUROC and 25% accuracy improvement in clinical data extraction</li>
            <li>Designed end-to-end ETL pipelines integrating multi-source databases into Snowflake, reducing data prep time by 60% through automated validation and metadata standardization</li>
            <li>Led A/B testing and experimentation frameworks for model optimization, delivering 20% lift in precision through threshold tuning and statistical analysis</li>
            <li>Orchestrated production ML workflows on AWS (SageMaker/S3) with automated monitoring, feature engineering, and experiment tracking</li>
            <li>Mentored 3 analysts on data integration, model validation, and research methodology best practices</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Python/R/SQL</span><span class="tag">XGBoost/ClinicalBERT</span>
            <span class="tag">AWS SageMaker/S3</span><span class="tag">Snowflake</span>
            <span class="tag">A/B Testing</span><span class="tag">ETL Pipelines</span>
            <span class="tag">Survival Analysis</span><span class="tag">NLP</span>
            <span class="tag">Tableau/Power BI</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li><b>Machine Learning Development:</b> Designed and deployed supervised learning models (XGBoost, logistic regression, Cox survival) for real-time and batch prediction systems; conducted hyperparameter optimization and cross-validation to achieve 83% AUROC</li>
            <li><b>NLP Pipeline Engineering:</b> Built scalable ClinicalBERT pipeline processing unstructured clinical notes with distributed text processing, automated validation, and rule-based audits; improved extraction accuracy 25% and reduced manual review by 80%</li>
            <li><b>Experimentation & Optimization:</b> Designed and executed A/B tests for model threshold optimization; performed statistical significance testing and causal inference analysis to measure business impact</li>
            <li><b>Data Engineering:</b> Architected ETL workflows integrating 500K+ records from multiple source systems using Python, SQL, and Airflow-style orchestration; implemented data quality checks, deduplication, schema validation, and complete lineage tracking</li>
            <li><b>MLOps & Production Systems:</b> Built end-to-end ML serving framework on AWS with automated ingestion, feature engineering, model monitoring, and experiment tracking; reduced data preparation latency by 60%</li>
            <li><b>Analytics & Reporting:</b> Developed interactive dashboards (Tableau/Power BI) for stakeholder decision-making; delivered technical reports translating complex model outputs into actionable business insights</li>
            <li><b>Data Governance & Compliance:</b> Established data quality standards, validation protocols, and HIPAA-compliant audit controls ensuring reliable, reproducible analytics</li>
            <li><b>Program Evaluation:</b> Led multi-site evaluation studies using causal inference, survival analysis, and clustering to quantify treatment effects and outcome disparities across patient cohorts</li>
            <li><b>Collaboration & Leadership:</b> Partnered with clinical teams and policy stakeholders to translate research questions into analytical frameworks; mentored junior analysts on statistical methods and data engineering best practices</li>
          </ul>
        </div>
      </div>
      <div class="backtop"><a href="#top">Back to top ↑</a></div>
    </details>

    <!-- Role 2: Graduate Research Assistant -->
    <details class="role" id="arid-gra">
      <summary>
        <img class="logo" src="/assets/images/logo/arid.jpg" alt="University of Arizona logo">
        <div class="head">
          <div class="title">Graduate Research Assistant</div>
          <div class="org">University of Arizona — Department of Pediatrics</div>
        </div>
        <div class="dates">Nov 2022 – Dec 2023</div>
      </summary>

      <div class="content">
        <div class="highlights">
          <h4>Highlights</h4>
          <ul class="tight">
            <li>Built anomaly detection and time-series forecasting pipelines for population health surveillance with backtesting and statistical validation</li>
            <li>Designed HIPAA-compliant PostgreSQL databases with optimized indexing and partitioning, reducing query latency by 80%</li>
            <li>Automated REDCap and survey platform ingestion with validation checks, improving data completeness by 25% and shortening reporting cycles by 70%</li>
            <li>Developed standardized feature tables enabling reproducible modeling and experimentation workflows</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Python/R/SQL</span><span class="tag">PostgreSQL</span>
            <span class="tag">REDCap</span><span class="tag">Airflow</span>
            <span class="tag">Time-Series Forecasting</span><span class="tag">Anomaly Detection</span>
            <span class="tag">Data Validation</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li><b>Predictive Modeling:</b> Built anomaly detection and time-series forecasting models for epidemiological surveillance; implemented backtesting, cross-validation, and statistical significance tests to ensure model robustness</li>
            <li><b>Database Engineering:</b> Designed and optimized multi-site PostgreSQL databases on Linux infrastructure; implemented indexing strategies, range partitioning, and query optimization reducing latency by 80%</li>
            <li><b>Data Pipeline Automation:</b> Created automated ingestion workflows for survey platforms (REDCap, Amazon MTurk) with validation, deduplication, schema checks, and audit logging; improved completeness 25% and reduced reporting time 70%</li>
            <li><b>Feature Engineering:</b> Standardized feature table creation for downstream modeling; established reproducible data preparation workflows supporting experimentation and analysis</li>
            <li><b>Data Quality & Validation:</b> Implemented comprehensive validation protocols including completeness checks, range validation, and logical consistency rules ensuring high-quality analytical datasets</li>
            <li><b>Visualization & Reporting:</b> Published KPI dashboards and analytical results to Tableau/Power BI enabling operational decision-making by public health teams</li>
            <li><b>Research Support:</b> Conducted statistical analyses (logistic regression, trend analysis) on population-level datasets; delivered baseline summaries and technical documentation for research teams</li>
            <li><b>Compliance & Security:</b> Maintained HIPAA-compliant data handling with access controls, encryption, and complete audit trails for sensitive health information</li>
          </ul>
        </div>
      </div>
      <div class="backtop"><a href="#top">Back to top ↑</a></div>
    </details>

    <!-- Role 3: Software Development Engineer -->
    <details class="role" id="tcs-sde">
      <summary>
        <img class="logo" src="/assets/images/logo/TCS_Logo.jpg" alt="TCS logo">
        <div class="head">
          <div class="title">Software Development Engineer</div>
          <div class="org">Tata Consultancy Services — Mumbai, India</div>
        </div>
        <div class="dates">Mar 2018 – Jul 2022</div>
      </summary>

      <div class="content">
        <div class="highlights">
          <h4>Highlights</h4>
          <ul class="tight">
            <li>Re-engineered PCI-compliant ETL from Informatica to distributed PySpark processing 3M+ daily transactions; led 12-member team ensuring security compliance and audit trails</li>
            <li>Built and deployed fraud detection ML pipelines on 10M+ transactions reducing false positives by 20% through experimentation and threshold optimization</li>
            <li>Automated CI/CD for ETL and ML deployments with data quality validation and rollback capabilities, improving release cadence by 25%</li>
            <li>Established enterprise data governance standards and automated quality monitoring improving data reliability by 25%</li>
          </ul>
          <div class="tagrow">
            <span class="tag">Python/SQL/PySpark</span><span class="tag">Informatica PowerCenter</span>
            <span class="tag">Teradata/AWS</span><span class="tag">ML Deployment</span>
            <span class="tag">CI/CD</span><span class="tag">Data Governance</span>
            <span class="tag">Unix/Linux</span>
          </div>
        </div>

        <div class="full">
          <h4>Scope & Responsibilities</h4>
          <ul class="tight">
            <li><b>Large-Scale Data Engineering:</b> Re-architected ETL pipelines from Informatica PowerCenter to distributed PySpark on Unix/Linux infrastructure processing 3M+ daily banking transactions; ensured PCI compliance with Protegrity tokenization for PII protection</li>
            <li><b>Machine Learning in Production:</b> Designed and deployed fraud detection models using Python and SQL on 10M+ transactions; reduced false positives by 20% through iterative experimentation, feature engineering, and threshold optimization</li>
            <li><b>Team Leadership:</b> Led cross-functional team of 12 engineers managing end-to-end ETL development lifecycle; established code review standards, testing protocols, and quality gates</li>
            <li><b>DevOps & Automation:</b> Built automated CI/CD pipelines for ETL and ML model deployments across mainframe and enterprise data warehouse systems; implemented data quality validation, automated testing, and rollback procedures improving release reliability by 25%</li>
            <li><b>Data Governance:</b> Established enterprise-wide data quality standards including validation rules, audit controls, and quality metrics; implemented automated monitoring ensuring consistent data reliability across production systems</li>
            <li><b>Performance Optimization:</b> Tuned complex SQL queries and ETL workflows reducing processing time by 50%; optimized resource utilization and infrastructure costs through query refactoring and job parallelization</li>
            <li><b>Analytics & Forecasting:</b> Built statistical models for revenue forecasting and trend analysis; delivered executive reports on multi-year fraud patterns supporting strategic decision-making</li>
            <li><b>Compliance & Security:</b> Maintained complete audit trails for financial data processing; ensured regulatory compliance with automated validation checks and PII tokenization protocols</li>
            <li><b>Migration Management:</b> Orchestrated complex data migrations across Dev/Test/UAT/Production environments; managed 2.5M customer record integration achieving 30% performance improvement</li>
          </ul>
        </div>
      </div>
      <div class="backtop"><a href="#top">Back to top ↑</a></div>
    </details>
  </div>
</div>