---
layout: single
title:
permalink: /Projects/
date: 2023-09-02
categories: pages
toc: false
toc_label: "Projects"
toc_icon: "columns"
author_profile: false
sidebar: false
classes: wide
---

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">

<style>
  :root{
    --brand:#336699; --ink:#1f2937; --muted:#6b7280; --card:#ffffff;
    --line:#e5e7eb; --ring:rgba(51,102,153,0.12); --bg:#f8fafc;

    /* wide targets */
    --site-max: 1440px;
    --content-max: 1280px;
  }

  /* ========= KILL THE THEME'S LEFT GUTTER ON THIS PAGE ========= */
  @media (min-width: 768px){
    /* MM puts padding on these wrappers; zero it */
    .layout--single .initial-content,
    .layout--single .page__inner-wrap{ padding-left:0 !important; }

    /* content column often floats with a reserved left column → disable */
    .layout--single .page__content{
      float:none !important;
      width:100% !important;
      max-width:none !important;
      margin:0 !important;
      padding-left:0 !important; padding-right:0 !important;
    }
  }

  /* ========= FULL-BLEED EDGE WRAPPER (starts at viewport’s hard left) ========= */
  .edge {
    width: 100vw;                          /* span full viewport width */
    margin-left: calc(50% - 50vw);         /* pull to the very left edge */
  }

  /* Your inner content block (no centering margin-left) */
  .wrap{
    font-family:'Inter', system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    color: var(--ink);
    max-width: min(var(--content-max), 96vw);
    margin: 0;                             /* <- NO auto-centering */
    padding: 0 16px 0 0;                   /* tiny right padding; left = 0 to be flush */
  }

  h1.section-title{ color:var(--brand); margin:.25rem 0 .4rem; font-size:clamp(24px,3vw,30px); }
  p.section-sub{ margin:0 0 .9rem; color:var(--muted); font-size:14.5px; }

  /* Card grid */
  .cards{ display:grid; gap:16px; }
  @media (min-width:1000px){ .cards{ grid-template-columns: repeat(3, 1fr); } }   /* desktop: 3-up */
  @media (min-width:1600px){ .cards{ grid-template-columns: repeat(4, 1fr); } }   /* very wide: 4-up */

  /* Cards */
  details.card{ border:1px solid var(--line); border-radius:12px; background:var(--card); box-shadow:0 1px 0 var(--ring); overflow:clip; }
  .card + .card{ margin-top:10px; }
  @media (min-width:1000px){ .card + .card{ margin-top:0; } }

  .card > summary{ list-style:none; cursor:pointer; display:flex; align-items:center; gap:12px; flex-wrap:wrap; padding:12px 14px; outline:none; }
  .card > summary::-webkit-details-marker{ display:none; }

  .pill{ font-size:12px; font-weight:600; color:var(--brand); background:#eef3f8; padding:4px 10px; border-radius:999px; border:1px solid #dbe2ea; white-space:nowrap; }
  .title{ font-weight:600; font-size:16px; color:var(--ink); }
  .meta{ margin-left:auto; display:flex; gap:10px; align-items:center; color:var(--muted); font-size:13px; }
  .meta .gh{ text-decoration:none; border:1px solid var(--brand); color:var(--brand); padding:5px 8px; border-radius:8px; font-weight:600; font-size:13px; }
  .meta .gh:hover{ background:var(--brand); color:#fff; }

  .content{ display:grid; grid-template-columns:1fr; gap:12px; border-top:1px solid var(--line); padding:12px 14px 14px; font-size:15px; line-height:1.55; }
  @media (min-width:860px){ .content{ grid-template-columns:320px 1fr; } }

  .thumb{ width:100%; aspect-ratio:16/10; object-fit:cover; border-radius:10px; border:1px solid var(--line); background:var(--bg); }

  .bullets{ margin:.25rem 0 0; padding-left:18px; }
  .bullets li{ margin:.2rem 0; }
  .links{ display:flex; gap:10px; flex-wrap:wrap; margin-top:.5rem; }
  .btn{ display:inline-block; text-decoration:none; font-weight:600; padding:7px 10px; border-radius:9px; font-size:14px; }
  .btn.ghost{ border:1px solid var(--brand); color:var(--brand); }

  .divider{ height:1px; background:var(--line); margin:1.1rem 0 .8rem; }
</style>

<!-- FULL-BLEED WRAPPER so the heading/cards start at hard left -->
<div class="edge">
  <div class="wrap">

    <!-- ===================== PROJECTS ===================== -->
    <h1 class="section-title">Projects</h1>
    <p class="section-sub">Browse selected personal projects. Click a card to view a short summary, visuals, and links.</p>

    <div class="cards">
      <!-- === keep your existing project cards; one example shown === -->
      <details class="card" id="phenophase">
        <summary>
          <span class="pill">Computer Vision</span>
          <span class="title">Phenophase Image Analysis (ResNet-50 + GANs)</span>
          <span class="meta"><span>Dec&nbsp;2023</span>
            <a class="gh" href="https://github.com/AmritaNeogi/PhenoCam-Image-Analysis-Using-CNN" target="_blank" rel="noopener">GitHub</a>
          </span>
        </summary>
        <div class="content">
          <img class="thumb" src="/assets/images/decidousForest.jpg" alt="Phenology project">
          <div>
            Detect leaf phenophase from PhenoCam images and forecast SOS/EOS across sites with augmentation for rare phases.
            <ul class="bullets">
              <li>ResNet-50 classifier; GANs for data scarcity</li>
              <li>Cross-site generalization beyond single camera tuning</li>
              <li>Calendar-level SOS/EOS with confidence bands</li>
            </ul>
            <div class="links">
              <a class="btn ghost" href="/assets/images/SOS_EOS.png" target="_blank">SOS/EOS plot</a>
              <a class="btn ghost" href="/assets/images/GAN.png" target="_blank">GAN architecture</a>
            </div>
          </div>
        </div>
      </details>

      <!-- Paste the rest of your project <details class="card">…</details> blocks here -->
      <!-- PROJECT 2 … PROJECT 7 ... (unchanged) -->
    </div><!-- /.cards -->

    <div class="divider"></div>

    <!-- ===================== RESEARCH ===================== -->
    <h1 class="section-title">Research</h1>
    <p class="section-sub">Work in progress from the ARID Lab at the University of Arizona. Click to view a brief, non-confidential summary.</p>

    <div class="cards">
      <!-- your research cards unchanged -->
    </div>

  </div>
</div>

<script>
  // Keep only one card open per grid
  document.querySelectorAll('.cards').forEach((grid) => {
    grid.querySelectorAll('details.card').forEach((d) => {
      d.addEventListener('toggle', () => {
        if (d.open) grid.querySelectorAll('details.card').forEach(o => { if (o !== d) o.removeAttribute('open'); });
      });
    });
  });
</script>
