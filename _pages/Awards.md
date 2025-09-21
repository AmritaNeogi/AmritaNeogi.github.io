---
layout: single
classes: wide
title:
permalink: /Awards/
date: 2023-09-02
categories: pages
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280;
    --card:#ffffff; --line:#e5e7eb; --ring:rgba(51,102,153,.12);
    --bg:#f8fafc;

    /* align left edge with the “Home” label in the masthead */
    --masthead-left: 24px;      /* nudge +/- a couple px if you want perfect alignment */
    --wrap-max: 1200px;         /* wider container on large screens */
  }

  /* ===== Kill Minimal Mistakes’ centered shell JUST on this page ===== */
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

  /* ===== Left-aligned wrapper ===== */
  .awards-wrap{
    font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    color:var(--ink);
    margin-left: var(--masthead-left);                 /* ← stick to the left, under “Home” */
    margin-right: 16px;
    width: min(var(--wrap-max), calc(100vw - var(--masthead-left) - 16px));
    box-sizing: border-box;
  }

  h1.page-title{ color:var(--brand); margin:.25rem 0 .6rem; font-size:clamp(24px,3vw,30px); }
  p.page-sub{ color:var(--muted); font-size:14.5px; margin:0 0 .9rem; }

  /* Section headers */
  .section{ margin:.8rem 0; }
  .section h2{ color:var(--brand); font-size:18px; margin:.2rem 0 .5rem; }
  .section-sub{ color:var(--muted); font-size:14.5px; margin:-.25rem 0 .6rem; }

  /* Cards */
  .card{
    background:var(--card); border:1px solid var(--line); border-radius:14px;
    box-shadow:0 1px 0 var(--ring); margin:.6rem 0; overflow:hidden;
  }
  .card-head{
    display:flex; justify-content:space-between; align-items:center;
    gap:10px; padding:12px 14px; background:#fff;
  }
  .title{ font-weight:700; font-size:16px; color:var(--ink); }
  .meta{ color:var(--muted); font-size:13.5px; white-space:nowrap; }
  .card-body{ padding:12px 14px 14px; border-top:1px solid var(--line); font-size:15px; line-height:1.55; }

  /* Certifications grid */
  .grid{ display:grid; gap:10px; grid-template-columns:repeat(1, minmax(0,1fr)); }
  @media (min-width:760px){ .grid{ grid-template-columns:repeat(2, minmax(0,1fr)); } }

  .btn{
    display:inline-block; text-decoration:none; font-weight:600; font-size:14px;
    padding:7px 10px; border-radius:9px; border:1px solid var(--brand); color:var(--brand); background:#fff;
  }
  .btn:hover{ background:var(--brand); color:#fff; }

  /* Collapsible award cards */
  details.award{
    border:1px solid var(--line); border-radius:14px; background:#fff;
    box-shadow:0 1px 0 var(--ring); margin:.6rem 0; overflow:hidden;
  }
  .award > summary{
    list-style:none; cursor:pointer; outline:none;
    display:grid; grid-template-columns: 1fr auto; align-items:center;
    gap:12px; padding:12px 14px;
  }
  .award > summary::-webkit-details-marker{ display:none; }
  .award .summary-title{ display:flex; flex-direction:column; gap:2px; }
  .award .summary-title .role{ font-weight:700; color:var(--ink); font-size:16px; }
  .award .summary-title .org{ color:var(--muted); font-size:13.5px; }
  .award .dates{ color:var(--muted); font-size:13.5px; white-space:nowrap; }

  .award-body{
    border-top:1px solid var(--line);
    padding:12px 14px 14px;
    display:grid; gap:12px; grid-template-columns:1fr;
    box-sizing:border-box; overflow-wrap:anywhere;        /* prevent text spill on narrow viewports */
  }
  @media (min-width:860px){ .award-body{ grid-template-columns: 1fr 320px; } }

  .desc{ font-size:15px; line-height:1.6; }
  .image-wrap{
    display:flex; align-items:center; justify-content:center;
    background:var(--bg); border:1px solid var(--line); border-radius:12px; padding:8px;
  }
  .image-wrap img{ width:100%; height:auto; border-radius:8px; }

  /* Small list */
  ul.tight{ margin:.25rem 0 0; padding-left:18px; }
  ul.tight li{ margin:.2rem 0; }
</style>

<div class="awards-wrap">
  <h1 class="page-title">Accomplishments</h1>
  <p class="page-sub">Selected certifications, scholarships, and awards.</p>

  <!-- ================= CERTIFICATIONS ================ -->
  <section class="section" id="certs">
    <h2>Certifications</h2>
    <p class="section-sub">Credential links open in a new tab.</p>

    <div class="grid">
      <!-- Google Data Analytics -->
      <article class="card">
        <div class="card-head">
          <div class="title">Google Data Analytics (Coursera)</div>
          <div class="meta">June 2023</div>
        </div>
        <div class="card-body">
          Foundational analytics certificate covering cleaning, visualization, SQL, spreadsheets, and stakeholder-ready insights.
          <div style="margin-top:.6rem;">
            <a class="btn" href="https://www.coursera.org/account/accomplishments/specialization/certificate/EMEK5BC3QWPA" target="_blank" rel="noopener">View certificate →</a>
          </div>
        </div>
      </article>

      <!-- Google Project Management -->
      <article class="card">
        <div class="card-head">
          <div class="title">Google Project Management (Coursera)</div>
          <div class="meta">July 2023</div>
        </div>
        <div class="card-body">
          Agile methods, sprint planning, risk tracking, and stakeholder communication for delivery at pace.
          <div style="margin-top:.6rem;">
            <a class="btn" href="https://www.coursera.org/account/accomplishments/specialization/certificate/UCSV3HVH4LQL" target="_blank" rel="noopener">View certificate →</a>
          </div>
        </div>
      </article>
    </div>
  </section>

  <!-- ============== SCHOLARSHIP & AWARDS ============== -->
  <section class="section" id="awards">
    <h2>Scholarship & Awards</h2>

    <!-- UArizona Dept of Pediatrics -->
    <details class="award" open>
      <summary>
        <div class="summary-title">
          <div class="role">Dept. of Pediatrics, University of Arizona</div>
          <div class="org">Scholarship: 0.5 FTE with Full Tuition Remission</div>
        </div>
        <div class="dates">Feb 2023 &middot; Aug 2023</div>
      </summary>
      <div class="award-body">
        <div class="desc">
          Supported graduate research and teaching with tuition fully remitted at 0.5 FTE. Recognized for strong academic performance and research contributions.
          <ul class="tight">
            <li>Graduate appointment supporting data pipelines and analytics for ARID Lab.</li>
            <li>Collaborative work with clinicians and biostatisticians on population-health projects.</li>
          </ul>
        </div>
      </div>
    </details>

    <!-- TCS Contextual Master Award -->
    <details class="award">
      <summary>
        <div class="summary-title">
          <div class="role">Contextual Master Award</div>
          <div class="org">Tata Consultancy Services (Financial Services)</div>
        </div>
        <div class="dates">Mar 2022</div>
      </summary>
      <div class="award-body">
        <div class="desc">
          Recognition for leading a critical retrofit during a major client merger, improving performance and data security.
          <ul class="tight">
            <li>Promoted to Senior ETL Developer with a 14% salary increase and ₹20,000 bonus.</li>
            <li>Resolved production issues and cut code execution time by ~30% using Protegrity expertise.</li>
            <li>Strengthened client trust; contributed to reduced annual IT budget and smoother integration.</li>
          </ul>
        </div>
        <div class="image-wrap">
          <img src="/assets/images/contexual_master.PNG" alt="TCS Contextual Master Award certificate">
        </div>
      </div>
    </details>

    <!-- NEN Champions Runners-Up -->
    <details class="award">
      <summary>
        <div class="summary-title">
          <div class="role">NEN Champions — Runners-Up</div>
          <div class="org">National Entrepreneurship Network (Wadhwani Foundation)</div>
        </div>
        <div class="dates">Mar 2016</div>
      </summary>
      <div class="award-body">
        <div class="desc">
          Recognized for contributions to entrepreneurship education and innovation initiatives.
          <ul class="tight">
            <li>Organized campus programs and workshops to promote early-stage venture skills.</li>
            <li>Coordinated student teams and community mentors for sustained engagement.</li>
          </ul>
        </div>
      </div>
    </details>
  </section>
</div>
