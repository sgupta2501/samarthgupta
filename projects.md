---
layout: page
title: "Projects"
permalink: /projects/
---

<style>
  .page-content { max-width: 775px; }
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

  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin-top: 1.5rem;
  }

  .proj-tile {
    background: white;
    border-radius: 16px;
    padding: 18px 20px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.07), 0 1px 4px rgba(0,0,0,0.04);
    position: relative;
    overflow: hidden;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    display: flex;
    flex-direction: column;
  }
  .proj-tile-desc { flex: 1; }
  .proj-tile-foot-end {
    margin-top: auto;
  }
  /* .proj-tile:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.10), 0 2px 8px rgba(0,0,0,0.06);
  } */

  .proj-tile h3 {
    font-size: 0.95rem;
    font-weight: 700;
    color: #2c2c2c;
    margin: 0 0 4px;
  }
  .proj-tile-tags {
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: #7c6ff7;
    margin-bottom: 10px;
    display: block;
  }
  .proj-tile-desc {
    font-size: 0.8rem;
    color: #6b6b6b;
    line-height: 1.6;
    margin: 0;
    display: block;
  }
  .proj-tile-icon {
    position: absolute;
    right: -10px;
    bottom: -10px;
    font-size: 150px;
    opacity: 0.12;
    line-height: 1;
    pointer-events: none;
    user-select: none;
  }
  .proj-tile-img-icon {
    position: absolute;
    right: -20px;
    bottom: -20px;
    width: 150px;
    height: 150px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
  }
   .proj-tile-img-icon-gre {
    position: absolute;
    right: -15px;
    bottom: -30px;
    width: 200px;
    height: 200px;
    object-fit: contain;
    opacity: 0.22;
    pointer-events: none;
    user-select: none;
  }
  .proj-tile-foot {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    margin-top: 12px;
    font-size: 0.85rem;
    font-weight: 600;
  }
  .proj-tile-foot i {
    font-size: 1.5rem;
    color: #2c2c2c;
  }
  .proj-tile-cta {
    color: #5bc8af;
    text-decoration: none;
    transition: color 0.15s ease, transform 0.15s ease;
    display: inline-block;
  }
  .proj-tile-cta:hover {
    color: #3fa88f;
    transform: translateX(2px);
  }
  .proj-tile-desc ul {
    margin: 0;
    padding-left: 18px;
  }
  .proj-tile-desc li {
    font-size: 0.8rem;
    color: #6b6b6b;
    line-height: 1.6;
    margin-bottom: 4px;
  }

</style>

<p class="exp-label">04 / Build</p>
<p class="exp-intro">Some started as course projects, some as consulting deliverables, and at least one as a 3am idea I couldn't shake. The through line is usually the same: a real problem, a scrappy build, and something that actually ran in production. Not everything shipped cleanly. Most of them taught me more when they didn't.</p>

<div class="projects-grid" markdown="0">
  <div class="proj-tile">
    <h3>Animal &rarr; Origami Image Translation</h3>
    <span class="proj-tile-tags">Deep Learning &middot; NST &middot; CycleGAN &middot; AWS</span>
    <div class="proj-tile-desc">
      <ul>
        <li>CS230 team project turning animal photos into origami-style images</li>
        <li>Built and trained the feed-forward NST models</li>
        <li>Ran a YOLOv8 segmentation pipeline over 61K images</li>
        <li>Managed the AWS training stack on EC2, SageMaker, and S3</li>
      </ul>
    </div>
    <div class="proj-tile-foot proj-tile-foot-end">
      <i class="fa fa-github"></i>
      <a href="https://github.com/antranakhasi/Origami-Model-using-CycleGAN" target="_blank" rel="noopener" class="proj-tile-cta">check out the repo &rarr;</a>
    </div>
    <img src="/assets/img/origami.png" class="proj-tile-img-icon" alt="">
  </div>
  <div class="proj-tile">
    <h3>Kintsugi Tax: Re-engagement Pipeline</h3>
    <span class="proj-tile-tags">HubSpot · CRM Automation · Customer Research · Product Strategy</span>
    <div class="proj-tile-desc">
      <ul>
        <li>23+ customer discovery interviews (500+ outreach) surfaced a $40K+ pipeline recovery opportunity</li>
        <li>Defined MVP: HubSpot "Blocked Item" field + feature-triggered rep follow-up workflow</li>
        <li>Built ReEngageBot, a Slack/HubSpot automation that closes the product-to-sales feedback loop</li>
        <li>Scoped MVP at ~$1,400–$1,500 with no new tooling required</li>
      </ul>
    </div>
    <div class="proj-tile-foot proj-tile-foot-end">
      <i class="fa fa-github"></i>
      <a href="https://github.com/antranakhasi/ReEngageBot" target="_blank" rel="noopener" class="proj-tile-cta">check out ReEngageBot &rarr;</a>
    </div>
    <img src="/assets/img/kintsugi.png" class="proj-tile-img-icon" alt="">
  </div>
  <div class="proj-tile">
    <h3>WeatherMesh: Go-to-Market Strategy</h3>
    <span class="proj-tile-tags">Market Research · GTM · Competitive Analysis · B2B · Energy Tech · Product Strategy</span>
    <div class="proj-tile-desc">
      <ul>
        <li>GTM strategy for WeatherMesh: AI weather API with 1-hour resolution in a $10B market</li>
        <li>Segmented ICP across grid operators, energy analysts, and sustainability officers at utilities and IPPs</li>
        <li>Three-tier pricing ($10–25k → $50–100k+/mo) benchmarked against 5 competitors</li>
        <li>Designed distinct inbound (SEO, webinars) and outbound (ABM, trade shows, pilots) motions</li>
      </ul>
    </div>
    <img src="/assets/img/windborne.png" class="proj-tile-img-icon" alt="">
  </div>
  <div class="proj-tile">
    <h3>GRE Analytical Writing Evaluation Tool</h3>
    <span class="proj-tile-tags">Flask · OpenAI API · NLP Prompt Engineering · Web App · EdTech</span>
    <div class="proj-tile-desc">
      <ul>
        <li>Built Flask-based GRE Issue Task simulator with timed in-browser writing and auto-submit system</li>
        <li>Designed OpenAI evaluation pipeline using structured prompt engineering for GRE rubric scoring</li>
        <li>Implemented real-time browser essay capture with preprocessing and submission handling</li>
        <li>Generated rubric-aligned scoring and feedback engine with low-latency inference and improvement suggestions</li>
      </ul>
    </div>
    <img src="/assets/img/gre.png" class="proj-tile-img-icon-gre" alt="">
  </div>
</div>
