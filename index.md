<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vadim Atlassov — Researcher</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #F5F2EC;
    --surface: #EFEAE0;
    --card: #FAF8F3;
    --border: #D6CFC0;
    --border-light: #E5DFD0;
    --text: #1A1714;
    --muted: #7A7165;
    --accent: #2C5F2E;
    --accent-light: #D8EAD8;
    --accent-mid: #4A8A4C;
    --highlight: #8B5E3C;
    --highlight-light: #F0E4D8;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Outfit', sans-serif;
    font-weight: 400;
    font-size: 15px;
    line-height: 1.7;
    min-height: 100vh;
  }

  /* Layout */
  .page {
    max-width: 780px;
    margin: 0 auto;
    padding: 60px 40px 100px;
  }

  /* Hero */
  .hero {
    display: grid;
    grid-template-columns: 160px 1fr;
    gap: 40px;
    align-items: start;
    margin-bottom: 56px;
    padding-bottom: 56px;
    border-bottom: 1px solid var(--border);
  }

  .avatar-wrap {
    position: relative;
  }

  .avatar {
    width: 160px;
    height: 160px;
    object-fit: cover;
    border-radius: 12px;
    display: block;
    border: 1px solid var(--border);
  }

  .avatar-placeholder {
    width: 160px;
    height: 160px;
    border-radius: 12px;
    background: var(--surface);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 42px;
    color: var(--muted);
    letter-spacing: -0.02em;
  }

  .name {
    font-family: 'DM Serif Display', serif;
    font-size: 38px;
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 10px;
    color: var(--text);
  }

  .bio {
    font-size: 14px;
    color: var(--muted);
    line-height: 1.75;
    margin-bottom: 20px;
  }

  .bio strong {
    color: var(--text);
    font-weight: 500;
  }

  .bio a {
    color: var(--text);
    text-decoration: underline;
    text-decoration-color: var(--border);
    text-underline-offset: 3px;
  }

  /* PhD callout */
  .callout {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 18px;
    margin-bottom: 20px;
  }

  .callout-header {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 12px;
  }

  .callout-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--accent-mid);
    flex-shrink: 0;
  }

  .callout-title {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
  }

  .interest-list {
    display: flex;
    flex-direction: column;
    gap: 6px;
    list-style: none;
  }

  .interest-list li {
    font-size: 13px;
    color: var(--muted);
    padding-left: 14px;
    position: relative;
    line-height: 1.5;
  }

  .interest-list li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--border);
  }

  .interest-list li strong {
    color: var(--text);
    font-weight: 500;
  }

  /* Contact links */
  .links {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .link-pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 100px;
    border: 1px solid var(--border);
    background: var(--card);
    font-size: 13px;
    font-weight: 400;
    color: var(--text);
    text-decoration: none;
    transition: background 0.15s, border-color 0.15s;
  }

  .link-pill:hover {
    background: var(--surface);
    border-color: var(--muted);
  }

  .link-icon {
    width: 14px;
    height: 14px;
    opacity: 0.6;
  }

  /* Section */
  .section { margin-bottom: 52px; }

  .section-label {
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border-light);
  }

  /* Education */
  .edu-list {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .edu-row {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 16px;
    align-items: baseline;
    padding: 12px 0;
    border-bottom: 1px solid var(--border-light);
  }

  .edu-row:last-child { border-bottom: none; }

  .edu-title {
    font-size: 14px;
    font-weight: 500;
  }

  .edu-sub {
    font-size: 13px;
    color: var(--muted);
    margin-top: 1px;
  }

  .edu-year {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--muted);
    white-space: nowrap;
  }

  /* Paper card */
  .paper {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px 26px;
    margin-bottom: 16px;
  }

  .paper-top {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 12px;
    margin-bottom: 6px;
  }

  .paper-title {
    font-family: 'DM Serif Display', serif;
    font-size: 17px;
    line-height: 1.3;
    color: var(--text);
    flex: 1;
  }

  .status-badge {
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 3px 10px;
    border-radius: 100px;
    background: var(--highlight-light);
    color: var(--highlight);
    white-space: nowrap;
    flex-shrink: 0;
    margin-top: 3px;
  }

  .paper-venue {
    font-size: 12px;
    color: var(--muted);
    margin-bottom: 20px;
    font-style: italic;
  }

  /* Metrics grid */
  .metrics {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 8px;
    margin-bottom: 16px;
  }

  .metric-box {
    background: var(--surface);
    border-radius: 8px;
    padding: 12px 14px;
    border: 1px solid var(--border-light);
  }

  .metric-value {
    font-family: 'DM Mono', monospace;
    font-size: 17px;
    font-weight: 500;
    color: var(--text);
    line-height: 1.2;
    margin-bottom: 4px;
  }

  .metric-value.pos { color: var(--accent); }

  .metric-desc {
    font-size: 11px;
    color: var(--muted);
    line-height: 1.4;
  }

  /* Stat rows */
  .stats {
    border-top: 1px solid var(--border-light);
    padding-top: 14px;
    margin-bottom: 16px;
  }

  .stat-row {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 5px 0;
    font-size: 13px;
    border-bottom: 1px solid var(--border-light);
  }

  .stat-row:last-child { border-bottom: none; }

  .stat-label { color: var(--muted); }

  .stat-val {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    font-weight: 500;
    color: var(--text);
    text-align: right;
  }

  .gain {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--accent-mid);
    margin-left: 6px;
  }

  /* Paper links */
  .paper-links {
    display: flex;
    gap: 8px;
    padding-top: 4px;
  }

  .paper-link {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    font-size: 12px;
    padding: 5px 14px;
    border-radius: 100px;
    border: 1px solid var(--border);
    background: var(--bg);
    color: var(--text);
    text-decoration: none;
    transition: background 0.15s;
  }

  .paper-link:hover { background: var(--surface); }

  /* Project */
  .project {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 26px;
  }

  .project-title {
    font-size: 15px;
    font-weight: 500;
    margin-bottom: 6px;
  }

  .project-title a {
    color: var(--text);
    text-decoration: underline;
    text-decoration-color: var(--border);
    text-underline-offset: 3px;
  }

  .project-desc {
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 14px;
    line-height: 1.65;
  }

  .tags { display: flex; gap: 6px; flex-wrap: wrap; }

  .tag {
    font-size: 11px;
    padding: 3px 10px;
    border-radius: 100px;
    background: var(--surface);
    color: var(--muted);
    border: 1px solid var(--border-light);
  }

  /* Footer */
  .footer {
    margin-top: 60px;
    padding-top: 24px;
    border-top: 1px solid var(--border-light);
    font-size: 12px;
    color: var(--muted);
    display: flex;
    justify-content: space-between;
  }

  @media (max-width: 620px) {
    .page { padding: 36px 20px 60px; }
    .hero { grid-template-columns: 1fr; gap: 24px; }
    .avatar, .avatar-placeholder { width: 100px; height: 100px; font-size: 28px; }
    .name { font-size: 28px; }
    .metrics { grid-template-columns: repeat(2, 1fr); }
    .paper-top { flex-direction: column; gap: 8px; }
    .footer { flex-direction: column; gap: 4px; }
  }
</style>
</head>
<body>
<div class="page">

  <!-- Hero -->
  <div class="hero">
    <div class="avatar-wrap">
      <img src="assets/personal_photo.png" alt="Vadim Atlassov" class="avatar"
           onerror="this.outerHTML='<div class=\'avatar-placeholder\'>VA</div>'">
    </div>
    <div>
      <h1 class="name">Vadim Atlassov</h1>
      <p class="bio">
        MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
        <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
        Research focus: <strong>physically-grounded generative AI</strong> for medicine and civil engineering.
      </p>

      <div class="callout">
        <div class="callout-header">
          <div class="callout-dot"></div>
          <div class="callout-title">Actively seeking PhD positions</div>
        </div>
        <ul class="interest-list">
          <li><strong>Generative AI:</strong> Latent Diffusion (LDM), Flow Matching, Latent Disentanglement, Spatial-Latent Alignment</li>
          <li><strong>Multimodal Learning:</strong> Vision-Language Models (VLM), Mixture-of-Experts (MoE) Adapters, DINOv2, Semantic Grounding</li>
          <li><strong>Domain Applications:</strong> Medical Imaging (Chest X-ray, Hematology), AI in Structural Engineering Monitoring (RC Beam Failure Diagnosis)</li>
        </ul>
      </div>

      <div class="links">
        <a href="https://www.linkedin.com/in/vadim-atlassov" class="link-pill" target="_blank">
          <svg class="link-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
        <a href="mailto:vadim.atlassov@nu.edu.kz" class="link-pill">
          <svg class="link-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
          Email
        </a>
        <a href="https://github.com/Vadim-ATL" class="link-pill" target="_blank">
          <svg class="link-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
          GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- Education -->
  <div class="section">
    <div class="section-label">Education</div>
    <div class="edu-list">
      <div class="edu-row">
        <div>
          <div class="edu-title">M.Sc. in Electrical &amp; Computer Engineering</div>
          <div class="edu-sub">Nazarbayev University · GPA 3.21 / 4.0</div>
        </div>
        <div class="edu-year">2024</div>
      </div>
      <div class="edu-row">
        <div>
          <div class="edu-title">Academic Exchange</div>
          <div class="edu-sub">Brno University of Technology, Czech Republic</div>
        </div>
        <div class="edu-year">—</div>
      </div>
      <div class="edu-row">
        <div>
          <div class="edu-sub">Hands-on experience training large-scale image generative models, including diffusion and flow matching architectures</div>
        </div>
        <div></div>
      </div>
    </div>
  </div>

  <!-- Publications -->
  <div class="section">
    <div class="section-label">Publications &amp; Preprints</div>
    <!-- Paper 1 -->
    <div class="paper">
      <div class="paper-top">
        <div class="paper-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
        <div class="status-badge">Under review</div>
      </div>
      <div class="paper-venue">Computerized Medical Imaging and Graphics (CMIG), 2025</div>
      <div class="metrics">
        <div class="metric-box">
          <div class="metric-value">56.78</div>
          <div class="metric-desc">FID on MIMIC-CXR</div>
        </div>
        <div class="metric-box">
          <div class="metric-value">0.6536</div>
          <div class="metric-desc">DICE — lung mask fidelity</div>
        </div>
        <div class="metric-box">
          <div class="metric-value pos">+17.5%</div>
          <div class="metric-desc">Pneumonia classification accuracy</div>
        </div>
        <div class="metric-box">
          <div class="metric-value pos">+4.2%</div>
          <div class="metric-desc">Diagnostic AUC improvement</div>
        </div>
      </div>
      <div class="stats">
        <div class="stat-row">
          <span class="stat-label">Radiologist rating — anatomical plausibility</span>
          <span class="stat-val">3.8 / 5</span>
        </div>
        <div class="stat-row">
          <span class="stat-label">Radiologist rating — pathology expression</span>
          <span class="stat-val">3.95 / 5</span>
        </div>
        <div class="stat-row">
          <span class="stat-label">Outperforms baselines</span>
          <span class="stat-val">Roentgen · Cheff · XReal</span>
        </div>
      </div>
      <div class="paper-links">
        <a href="https://github.com/nubcico/XrayGen/tree/main" class="paper-link" target="_blank">
          <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
          Code
        </a>
        <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing" class="paper-link" target="_blank">
          <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
          Preprint
        </a>
      </div>
    </div>
    <!-- Paper 2 -->
    <div class="paper">
      <div class="paper-top">
        <div class="paper-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
        <div class="status-badge">Under review</div>
      </div>
      <div class="paper-venue">Journal of Building Engineering</div>
      <div class="metrics">
        <div class="metric-box">
          <div class="metric-value">0.0628</div>
          <div class="metric-desc">KID score</div>
        </div>
        <div class="metric-box">
          <div class="metric-value">0.790</div>
          <div class="metric-desc">SSIM — structural consistency</div>
        </div>
        <div class="metric-box">
          <div class="metric-value">4.12 / 5</div>
          <div class="metric-desc">Expert — structural realism</div>
        </div>
        <div class="metric-box">
          <div class="metric-value">3.98 / 5</div>
          <div class="metric-desc">Expert — assessment clarity</div>
        </div>
      </div>
      <div class="stats">
        <div class="stat-row">
          <span class="stat-label">Failure-type classification</span>
          <span class="stat-val">85.8% <span class="gain">+5.2%</span></span>
        </div>
        <div class="stat-row">
          <span class="stat-label">Rebar exposure detection</span>
          <span class="stat-val">95.2% <span class="gain">+11.9%</span></span>
        </div>
        <div class="stat-row">
          <span class="stat-label">Flexural cracking detection</span>
          <span class="stat-val">84.3% <span class="gain">+12.9%</span></span>
        </div>
        <div class="stat-row">
          <span class="stat-label">Concrete spalling detection</span>
          <span class="stat-val">85.3% <span class="gain">+11.5%</span></span>
        </div>
      </div>
      <div class="paper-links">
        <a href="https://github.com/nubcico/GenBeamJoint" class="paper-link" target="_blank">
          <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
          Code
        </a>
        <a href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing" class="paper-link" target="_blank">
          <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
          Preprint
        </a>
      </div>
    </div>
  </div>

  <!-- Projects -->
  <div class="section">
    <div class="section-label">Projects</div>
    <div class="project">
      <div class="project-title"><a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM" target="_blank">BloodMNIST-DDPM</a></div>
      <p class="project-desc">Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.</p>
      <div class="tags">
        <span class="tag">Medical Imaging</span>
        <span class="tag">DDPM</span>
        <span class="tag">Hematology</span>
      </div>
    </div>
  </div>

  <div class="footer">
    <span>Vadim Atlassov · Nazarbayev University</span>
    <span>vadim.atlassov@nu.edu.kz</span>
  </div>

</div>
</body>
</html>
