---
layout: page
title: "Experience"
permalink: /experience/
---

<style>
  .page-content { max-width: 775px !important; }
  .page-content h1 { display: none; }

  .exp-label {
    font-size: 18px;
    font-weight: 800;
    letter-spacing: 3px;
    background: linear-gradient(to right, #5bc8af, #7c6ff7);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
    margin-bottom: 6px;
    display: inline-block;
  }
  .exp-intro {
    font-size: 1rem;
    color: #6b6b6b;
    max-width: 1000px;
    line-height: 1.5;
    margin: 0 0 1.5rem;
    text-align: justify;
  }

  /* ── Full-width breakout for wave timeline ───────── */
  .wave-wrap {
    width: 100vw;
    margin-left: calc(-50vw + 50%);
    padding: 0 40px;
    box-sizing: border-box;
    overflow-x: auto;
  }

  /* ── Wave timeline container ─────────────────────── */
  /*
     Layout reference (px from top of .wave-timeline):
       0   ┐
           │  above-card area (cards stacked here)
       280 ┤
           │  wave SVG starts (height: 240px)
           │     trough at SVG y=180  ⇒ timeline y = 280+180 = 460
           │     peak   at SVG y=60   ⇒ timeline y = 280+60  = 340
       520 ┤
           │  below-card area
       720 ┘
  */
  .wave-timeline {
    position: relative;
    width: 100%;
    min-width: 1300px;
    height: 720px;
    margin: -100px 0px 0px;
  }

  .wave-svg {
    position: absolute;
    top: 280px;
    left: 0;
    width: 100%;
    height: 240px;
    pointer-events: none;
    z-index: 1;
  }

  /* ── A single entry on the wave ──────────────────── */
  /* `left` and `top` are set inline per entry (in pixels/percent
     of the wave-timeline). The transform shifts the entry so its
     dot center lands exactly on the (left, top) reference point. */
  .wave-entry {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 480px;
    z-index: 2;
  }
  /* Above-entry: bottom of the entry (the dot) anchors to the point */
  .wave-above {
    transform: translate(-50%, calc(-100% + 7px));
  }
  /* Below-entry: top of the entry (the dot) anchors to the point */
  .wave-below {
    transform: translate(-50%, -7px);
  }

  /* ── Dot ─────────────────────────────────────────── */
  .we-dot {
    width: 14px;
    height: 14px;
    background: #7c6ff7;
    border-radius: 50%;
    border: 3px solid #f7f7f5;
    box-shadow: 0 0 0 2px #7c6ff7;
    flex-shrink: 0;
    z-index: 3;
  }

  /* ── Stem ────────────────────────────────────────── */
  .we-stem {
    width: 2px;
    height: 100px;
    background: #7c6ff7;
    flex-shrink: 0;
  }

  /* ── Date pill ───────────────────────────────────── */
  .tl-date {
    display: inline-flex;
    align-items: center;
    background: linear-gradient(90deg, #7c6ff7, #8b84f8);
    color: white;
    font-size: 11px;
    font-weight: 700;
    padding: 6px 16px;
    border-radius: 50px;
    white-space: nowrap;
    letter-spacing: 0.4px;
    box-shadow: 0 3px 10px rgba(124, 111, 247, 0.3);
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    z-index: 4;
  }
  /* Date sits on the OPPOSITE side of the dot from the card */
  .wave-above .tl-date {
    /* Above-card → date below the dot */
    top: calc(100% + 8px);
  }
  .wave-below .tl-date {
    /* Below-card → date above the dot */
    bottom: calc(100% + 8px);
  }

  /* ── Card ────────────────────────────────────────── */
  .tl-card {
    background: white;
    border-radius: 16px;
    padding: 22px 26px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.07), 0 1px 4px rgba(0,0,0,0.04);
    position: relative;
    overflow: hidden;
    width: 100%;
    box-sizing: border-box;
  }
  .tl-card-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 8px;
    margin-bottom: 3px;
  }
  .tl-card h3 {
    font-size: 0.95rem;
    font-weight: 700;
    color: #2c2c2c;
    margin: 0;
  }
  .tl-location {
    font-size: 0.8rem;
    color: #aaa;
    white-space: nowrap;
    flex-shrink: 0;
  }
  .tl-role {
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: #7c6ff7;
    display: block;
    margin-bottom: 10px;
  }
  .tl-desc {
    font-size: 0.78rem;
    color: #6b6b6b;
    line-height: 1.65;
    margin: 0;
    padding-left: 14px;
  }
  .tl-desc li { margin-bottom: 5px; }
  .tl-card-icon {
    position: absolute;
    right: -10px;
    bottom: -10px;
    font-size: 110px;
    opacity: 0.22;
    line-height: 1;
    pointer-events: none;
    user-select: none;
  }
  .tl-card-img-icon {
    position: absolute;
    right: -10px;
    bottom: -10px;
    width: 150px;
    height: 150px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
  }
  .tl-heal-card {
    position: absolute;
    right: -40px;
    bottom: -40px;
    width: 150px;
    height: 150px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
  }
   .tl-haas-card {
    position: absolute;
    right: 0px;
    bottom: -75px;
    width: 200px;
    height: 200px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
  }
</style>

<p class="exp-label">01 / Journey</p>
<p class="exp-intro">I've shipped AI products, defined requirements, run user feedback sessions, and written the pipelines that powered them, sometimes all in the same week. At Stanford, I built data infrastructure from scratch and had to sell it before it existed. That combination of knowing what to build and how to build it tends to follow me everywhere. Still not sure if that's a skill or a personality flaw.</p>

<div class="wave-wrap">
  <div class="wave-timeline">

    <!-- ── The wave line (SVG) ── -->
    <!-- viewBox 0 0 1000 240. Path uses three quadratic curves:
         (0,120)→(333,120) via control (166,240)  → trough at (166,180)
         (333,120)→(666,120) via control (500,0)  → peak   at (500,60)
         (666,120)→(1000,120) via control (833,240)→ trough at (833,180) -->
    <svg class="wave-svg" viewBox="0 0 1000 240" preserveAspectRatio="none">
      <defs>
        <linearGradient id="waveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="0%" stop-color="#5bc8af"/>
          <stop offset="100%" stop-color="#7c6ff7"/>
        </linearGradient>
      </defs>
      <path d="M 0 120 Q 166 320 333 120 Q 500 -80 666 120 Q 833 320 1000 120"
            stroke="url(#waveGrad)" stroke-width="3" fill="none" stroke-linecap="round"/>
    </svg>

    <!-- ── PwC: above the wave, dot at left trough (16.6%, y=460) ── -->
    <div class="wave-entry wave-above" style="left: 16.6%; top: 500px;">
      <div class="tl-card">
        <div class="tl-card-header">
          <h3>PricewaterhouseCoopers (PwC)</h3>
          <span class="tl-location">Kolkata, India</span>
        </div>
        <span class="tl-role">Associate, One Consulting – Emerging Tech</span>
        <ul class="tl-desc">
          <li>Deployed production RAG-based LLM product; launched MVP in 3 weeks, saving ~$180K annually.</li>
          <li>Owned backend dev and prompt engineering; designed agentic workflows across multiple LLM APIs.</li>
          <li>Drove user adoption via feedback sessions; shipped features improving output accuracy by ~40%.</li>
          <li>Authored PRDs and conducted competitive analysis across 20+ industries to validate GenAI use cases.</li>
        </ul>
        <img src="/assets/img/pwc.png" class="tl-card-img-icon" alt="">
      </div>
      <span class="tl-date">Jan 2023 — Aug 2024</span>
      <div class="we-stem"></div>
      <div class="we-dot"></div>
    </div>

    <!-- ── HEAL Lab: below the wave, dot at center peak (50%, y=340) ── -->
    <div class="wave-entry wave-below" style="left: 50%; top: 300px;">
      <div class="we-dot"></div>
      <div class="we-stem"></div>
      <span class="tl-date">Oct 2024 — May 2025</span>
      <div class="tl-card">
        <div class="tl-card-header">
          <h3>HEAL Lab, School of Medicine</h3>
          <span class="tl-location">Stanford, CA</span>
        </div>
        <span class="tl-role">Research Associate</span>
        <ul class="tl-desc">
          <li>Built NLP pipelines analyzing 500+ unstructured clinical records; reduced manual review effort at scale.</li>
          <li>Synthesized behavioral insights for interdisciplinary teams, informing improvements in care delivery workflows.</li>
        </ul>
        <img src="/assets/img/heal.png" class="tl-heal-card" alt="">
      </div>
    </div>

    <!-- ── Haas: above the wave, dot at right trough (83.3%, y=460) ── -->
    <div class="wave-entry wave-above" style="left: 83.3%; top: 500px;">
      <div class="tl-card">
        <div class="tl-card-header">
          <h3>Haas Center for Public Service</h3>
          <span class="tl-location">Stanford, CA</span>
        </div>
        <span class="tl-role">Data Analyst</span>
        <ul class="tl-desc">
          <li>Built SQL/Python pipelines and Tableau dashboards across 15 programs serving 1,500+ students.</li>
          <li>Applied crawl-walk-run model to drive adoption; secured stakeholder buy-in for program-wide migration.</li>
          <li>Developed Airtable matching system with Airflow orchestration; reduced manual effort across 1,500+ records.</li>
        </ul>
        <img src="/assets/img/haas.png" class="tl-haas-card" alt="">
      </div>
      <span class="tl-date">Dec 2025 — Present</span>
      <div class="we-stem"></div>
      <div class="we-dot"></div>
    </div>

  </div>
</div>
