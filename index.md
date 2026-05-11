<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vadim Atlassov — Researcher</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #faf9f7;
    --ink: #1a1916;
    --ink-soft: #5a5753;
    --ink-faint: #9a9793;
    --rule: #e2e0db;
    --accent: #2a5caa;
    --accent-warm: #c0392b;
    --panel: #f0ede8;
  }

  html { font-size: 17px; }

  body {
    font-family: 'EB Garamond', Georgia, serif;
    background: var(--bg);
    color: var(--ink);
    line-height: 1.65;
    min-height: 100vh;
  }

  /* ── Layout ── */
  .shell {
    max-width: 780px;
    margin: 0 auto;
    padding: 0 32px;
  }

  /* ── Top bar ── */
  header {
    border-bottom: 1px solid var(--rule);
    padding: 18px 0;
    margin-bottom: 56px;
  }

  .nav-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
  }

  .nav-name {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--ink-soft);
    text-decoration: none;
  }

  nav {
    display: flex;
    gap: 24px;
    list-style: none;
  }

  nav a {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--ink-soft);
    text-decoration: none;
    transition: color 0.2s;
  }
  nav a:hover { color: var(--accent); }
  nav a.active { color: var(--ink); }

  /* ── Hero ── */
  .hero {
    display: grid;
    grid-template-columns: 140px 1fr;
    gap: 40px;
    align-items: start;
    margin-bottom: 64px;
    animation: fadeUp 0.6s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .photo {
    width: 140px;
    height: 140px;
    object-fit: cover;
    border-radius: 4px;
    display: block;
    background: var(--panel);
    border: 1px solid var(--rule);
  }

  .hero-text h1 {
    font-size: 2.5rem;
    font-weight: 500;
    letter-spacing: -0.025em;
    line-height: 1.15;
    margin-bottom: 12px;
  }

  .hero-text .role {
    font-style: italic;
    color: var(--ink-soft);
    font-size: 1.05rem;
    margin-bottom: 20px;
  }

  .hero-text .role strong {
    font-style: normal;
    font-weight: 500;
    color: var(--ink);
  }

  .status-bar {
    border-left: 2px solid var(--accent);
    padding: 10px 16px;
    background: var(--panel);
    font-size: 0.9rem;
    line-height: 1.55;
    margin-bottom: 20px;
    border-radius: 0 3px 3px 0;
  }

  .status-bar strong {
    display: block;
    font-size: 0.8rem;
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 4px;
  }

  .contact-links {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }

  .contact-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--ink-soft);
    text-decoration: none;
    border-bottom: 1px solid var(--rule);
    padding-bottom: 1px;
    transition: color 0.2s, border-color 0.2s;
  }

  .contact-links a:hover {
    color: var(--accent);
    border-color: var(--accent);
  }

  /* ── Section ── */
  section {
    margin-bottom: 56px;
    animation: fadeUp 0.6s ease both;
    animation-delay: 0.1s;
  }

  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-faint);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--rule);
  }

  /* ── Research interests ── */
  .interests-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }

  .interest-card {
    border: 1px solid var(--rule);
    padding: 14px 16px;
    border-radius: 4px;
    background: white;
  }

  .interest-card .ic-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    color: var(--ink-faint);
    margin-bottom: 6px;
  }

  .interest-card .ic-items {
    font-size: 0.875rem;
    line-height: 1.55;
    color: var(--ink-soft);
  }

  /* ── Education ── */
  .edu-item {
    display: grid;
    grid-template-columns: 100px 1fr;
    gap: 12px 24px;
    padding: 14px 0;
    border-bottom: 1px solid var(--rule);
    font-size: 0.95rem;
  }

  .edu-item:last-child { border-bottom: none; }

  .edu-year {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--ink-faint);
    padding-top: 3px;
  }

  .edu-title { font-weight: 500; margin-bottom: 3px; }
  .edu-inst { color: var(--ink-soft); font-style: italic; }
  .edu-note { font-size: 0.85rem; color: var(--ink-faint); margin-top: 4px; }

  /* ── Publications preview ── */
  .pub-item {
    padding: 20px 0;
    border-bottom: 1px solid var(--rule);
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 16px;
    align-start: start;
  }

  .pub-item:last-child { border-bottom: none; }

  .pub-title {
    font-size: 1.05rem;
    font-weight: 500;
    margin-bottom: 4px;
    line-height: 1.4;
  }

  .pub-venue {
    font-size: 0.82rem;
    font-style: italic;
    color: var(--ink-soft);
    margin-bottom: 8px;
    font-family: 'DM Mono', monospace;
  }

  .pub-desc {
    font-size: 0.9rem;
    color: var(--ink-soft);
    line-height: 1.6;
  }

  .pub-links {
    display: flex;
    flex-direction: column;
    gap: 6px;
    align-items: flex-end;
    flex-shrink: 0;
  }

  .btn-link {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--accent);
    text-decoration: none;
    border: 1px solid var(--accent);
    padding: 4px 9px;
    border-radius: 3px;
    white-space: nowrap;
    transition: background 0.18s, color 0.18s;
  }

  .btn-link:hover {
    background: var(--accent);
    color: white;
  }

  /* ── Projects ── */
  .proj-item {
    padding: 18px 0;
    border-bottom: 1px solid var(--rule);
    display: flex;
    align-items: flex-start;
    gap: 20px;
  }

  .proj-item:last-child { border-bottom: none; }

  .proj-num {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    color: var(--ink-faint);
    padding-top: 4px;
    flex-shrink: 0;
    width: 24px;
  }

  .proj-title {
    font-weight: 500;
    font-size: 0.98rem;
    margin-bottom: 4px;
  }

  .proj-title a { color: var(--ink); text-decoration: none; border-bottom: 1px solid var(--rule); }
  .proj-title a:hover { border-color: var(--accent); color: var(--accent); }

  .proj-desc { font-size: 0.875rem; color: var(--ink-soft); line-height: 1.55; }

  .tag-row { margin-top: 8px; display: flex; gap: 6px; flex-wrap: wrap; }

  .tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.04em;
    color: var(--ink-faint);
    background: var(--panel);
    border: 1px solid var(--rule);
    padding: 2px 7px;
    border-radius: 2px;
  }

  /* ── Footer ── */
  footer {
    border-top: 1px solid var(--rule);
    padding: 24px 0 40px;
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.04em;
    color: var(--ink-faint);
    display: flex;
    justify-content: space-between;
  }

  /* ── Responsive ── */
  @media (max-width: 600px) {
    .shell { padding: 0 20px; }
    .hero { grid-template-columns: 1fr; text-align: center; }
    .photo { margin: 0 auto; }
    .contact-links { justify-content: center; }
    .interests-grid { grid-template-columns: 1fr; }
    .pub-item { grid-template-columns: 1fr; }
    .pub-links { flex-direction: row; align-items: center; }
    footer { flex-direction: column; gap: 6px; }
  }
</style>
</head>
<body>

<div class="shell">
  <header>
    <div class="nav-row">
      <a class="nav-name" href="index.html">Vadim Atlassov</a>
      <nav>
        <a href="index.html" class="active">CV</a>
        <a href="pub-xray.html">CXR Paper</a>
        <a href="pub-beam.html">RC Beam Paper</a>
        <a href="https://github.com/Vadim-ATL" target="_blank">GitHub ↗</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <div class="hero">
    <img class="photo" src="assets/personal_photo.png" alt="Vadim Atlassov">
    <div class="hero-text">
      <h1>Vadim Atlassov</h1>
      <p class="role">MSc Researcher · <strong>HCI Lab, Nazarbayev University</strong><br>
        Supervised by <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko" style="color:inherit;">Prof. Minho Lee</a></strong>
      </p>
      <div class="status-bar">
        <strong>Seeking PhD positions</strong>
        Physically-grounded generative AI for medicine and civil engineering.
        Interests span latent diffusion, flow matching, VLMs, and domain adaptation.
      </div>
      <div class="contact-links">
        <a href="https://www.linkedin.com/in/vadim-atlassov">LinkedIn</a>
        <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
        <a href="https://github.com/Vadim-ATL">GitHub</a>
      </div>
    </div>
  </div>

  <!-- Research Interests -->
  <section>
    <div class="section-label">Research Interests</div>
    <div class="interests-grid">
      <div class="interest-card">
        <div class="ic-label">Generative AI</div>
        <div class="ic-items">Latent Diffusion, Flow Matching, Latent Disentanglement, Spatial-Latent Alignment</div>
      </div>
      <div class="interest-card">
        <div class="ic-label">Multimodal Learning</div>
        <div class="ic-items">VLMs, MoE Adapters, DINOv2, Semantic Grounding</div>
      </div>
      <div class="interest-card">
        <div class="ic-label">Domain Applications</div>
        <div class="ic-items">Medical Imaging, Hematology, Structural Engineering Monitoring</div>
      </div>
    </div>
  </section>

  <!-- Education -->
  <section>
    <div class="section-label">Education</div>
    <div class="edu-item">
      <div class="edu-year">2024</div>
      <div>
        <div class="edu-title">M.Sc. in Electrical &amp; Computer Engineering</div>
        <div class="edu-inst">Nazarbayev University — GPA 3.21/4.0</div>
        <div class="edu-note">Academic Exchange: Brno University of Technology, Czech Republic</div>
      </div>
    </div>
  </section>

  <!-- Publications -->
  <section>
    <div class="section-label">Publications &amp; Preprints</div>
    <div class="pub-item">
      <div>
        <div class="pub-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
        <div class="pub-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review</div>
        <div class="pub-desc">
          FID 56.78 on MIMIC-CXR; DICE 0.6536. Synthetic augmentation improved pneumonia classification by +17.5% accuracy, +4.2% AUC. Radiologist ratings: anatomical plausibility 3.8/5, pathology expression 3.95/5.
        </div>
      </div>
      <div class="pub-links">
        <a class="btn-link" href="pub-xray.html">Details</a>
        <a class="btn-link" href="https://github.com/nubcico/XrayGen" target="_blank">Code ↗</a>
        <a class="btn-link" href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing" target="_blank">PDF ↗</a>
      </div>
    </div>
    <div class="pub-item">
      <div>
        <div class="pub-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
        <div class="pub-venue">Journal of Building Engineering — Under Review</div>
        <div class="pub-desc">
          KID 0.0628, SSIM 0.790. Augmentation gains: failure-type +5.2%, rebar exposure +11.9%, flexural cracking +12.9%, concrete spalling +11.5%. Expert structural realism: 4.12/5.
        </div>
      </div>
      <div class="pub-links">
        <a class="btn-link" href="pub-beam.html">Details</a>
        <a class="btn-link" href="https://github.com/nubcico/GenBeamJoint" target="_blank">Code ↗</a>
        <a class="btn-link" href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing" target="_blank">PDF ↗</a>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section>
    <div class="section-label">Projects</div>
    <div class="proj-item">
      <div class="proj-num">01</div>
      <div>
        <div class="proj-title">
          <a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM" target="_blank">BloodMNIST-DDPM</a>
        </div>
        <div class="proj-desc">
          Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology using denoising diffusion probabilistic models.
        </div>
        <div class="tag-row">
          <span class="tag">Medical Imaging</span>
          <span class="tag">DDPM</span>
          <span class="tag">Hematology</span>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <span>Vadim Atlassov · Nazarbayev University</span>
    <span>vadim.atlassov@nu.edu.kz</span>
  </footer>
</div>

</body>
</html>
