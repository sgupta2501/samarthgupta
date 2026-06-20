---
layout: page
title: "Education"
permalink: /education/
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
  .wave-timeline {
    position: relative;
    width: 100%;
    min-width: 1000px;
    height: 760px;
    margin: -170px 0px 10px;
  }
  .wave-svg {
    position: absolute;
    top: 280px;
    left: 0;
    width: 100%;
    height: 340px;
    pointer-events: none;
    z-index: 1;
  }

  .wave-entry {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 480px;
    z-index: 2;
  }
  .wave-above {
    transform: translate(-50%, calc(-100% + 7px));
  }
  .wave-below {
    transform: translate(-50%, -7px);
  }

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
    align-items: center;
    gap: 8px;
    margin-bottom: 3px;
  }
  .tl-card-img-icon {
    position: absolute;
    right: -40px;
    bottom: -30px;
    width: 150px;
    height: 150px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
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
  .tl-subheading {
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: #7c6ff7;
    margin: 12px 0 6px;
  }
  .tl-card-icon {
    position: absolute;
    right: -10px;
    bottom: -10px;
    font-size: 110px;
    opacity: 0.12;
    line-height: 1;
    pointer-events: none;
    user-select: none;
  }
</style>

<p class="exp-label">03 / Foundation</p>
<p class="exp-intro">EE undergrad who got obsessed with why products fail, won some hackathons, consulted across three continents, and ended up at Stanford. The throughline was always the same: find the messy human problem, build the technical solution, make it scale.</p>

<div class="wave-wrap">
  <div class="wave-timeline">

    <!-- ── The wave line (SVG) ── -->
    <!-- viewBox 0 0 1000 240. Two quadratic curves:
         (0,120)→(500,120) via control (250,240) → trough at (250,180)
         (500,120)→(1000,120) via control (750,0) → peak  at (750,60)  -->
    <svg class="wave-svg" viewBox="0 0 1000 340" preserveAspectRatio="none">
      <defs>
        <linearGradient id="waveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="0%" stop-color="#5bc8af"/>
          <stop offset="100%" stop-color="#7c6ff7"/>
        </linearGradient>
      </defs>
      <path d="M 0 170 Q 250 500 500 170 T 1000 170"
            stroke="url(#waveGrad)" stroke-width="3" fill="none" stroke-linecap="round"/>
    </svg>

    <!-- ── Stanford: above the wave, dot at left trough (25%, y=460) ── -->
    <div class="wave-entry wave-above" style="left: 25%; top: 617px;">
      <div class="tl-card">
        <div class="tl-card-header">
          <h3>Stanford University</h3>
          <span class="tl-location">Stanford, CA</span>
        </div>
        <span class="tl-role">Master of Science in Management Science and Engineering</span>
        <ul class="tl-desc">
          <li>Teaching Assistant for Managing Innovation and Driving Adoption in Frontier Technologies.</li>
          <li>Partnered with Windborne Systems on weather intelligence and AI applications spanning Latin America and Europe.</li>
          <li>Built GTM automation and re-engagement workflows at Kintsugi, a startup navigating the chaos of US sales tax compliance.</li>
          <li><em>Relevant coursework: Data Science · Optimization · Strategy · Product Management · Deep Learning · NLP</em></li>
        </ul>
        <img src="/assets/img/stanford-logo.avif" class="tl-card-img-icon" alt="">
      </div>
      <span class="tl-date">Sept 2024 — Present</span>
      <div class="we-stem"></div>
      <div class="we-dot"></div>
    </div>

    <!-- ── VIT: below the wave, dot at right peak (75%, y=340) ── -->
    <div class="wave-entry wave-below" style="left: 75%; top: 283px;">
      <div class="we-dot"></div>
      <div class="we-stem"></div>
      <span class="tl-date">Jul 2019 — Jun 2023</span>
      <div class="tl-card">
        <div class="tl-card-header">
          <h3>Vellore Institute of Technology</h3>
          <span class="tl-location">Vellore, India</span>
        </div>
        <span class="tl-role">Bachelor of Technology in Electrical & Electronics Engineering</span>
        <ul class="tl-desc">
          <li>Merit Scholar for Academic years 2019-20 and 2020-21.</li>
          <li><em>Relevant coursework: Python · Java · OOP · Statistical Data Analysis · Neural Networks · IoT</em></li>
        </ul>
        <p class="tl-subheading">Extracurriculars</p>
        <ul class="tl-desc">
          <li>Led E'Summit'21 — an 8-event, 4-day business festival — managing 50+ volunteers and architecting Innoventure with 300+ participants.</li>
          <li>Designed Futerpreneurs 6.0, a national business competition; managed a team of 15+ coordinators.</li>
          <li>Placed in three national competitions: HackWIE (3rd), 3-Day CEO (2nd), Escape Rooms CEO (3rd).</li>
        </ul>
        <img src="/assets/img/vit-logo.png" class="tl-card-img-icon" alt="">
      </div>
    </div>

  </div>
</div>
