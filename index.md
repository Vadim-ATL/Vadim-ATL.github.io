---
layout: default
title: Vadim Atlassov - Researcher
---

<style>
  /* ===== CSS Variables for Consistent Theming ===== */
  :root {
    --color-bg: #ffffff;
    --color-text: #1a1a1a;
    --color-text-muted: #555555;
    --color-border: #e0e0e0;
    --color-panel: #f9f9f9;
    --color-accent: #2563eb;
    --color-accent-hover: #1d4ed8;
    --shadow-sm: 0 1px 2px rgba(0,0,0,0.04);
    --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
    --shadow-lg: 0 8px 24px rgba(0,0,0,0.12);
    --radius-sm: 8px;
    --radius-md: 12px;
    --radius-lg: 16px;
    --spacing-xs: 8px;
    --spacing-sm: 16px;
    --spacing-md: 24px;
    --spacing-lg: 32px;
    --spacing-xl: 48px;
    --font-sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    --font-mono: "SF Mono", "Fira Code", "Fira Mono", monospace;
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --color-bg: #0f0f0f;
      --color-text: #f5f5f5;
      --color-text-muted: #a0a0a0;
      --color-border: #2a2a2a;
      --color-panel: #1a1a1a;
      --shadow-sm: 0 1px 2px rgba(0,0,0,0.2);
      --shadow-md: 0 4px 12px rgba(0,0,0,0.3);
      --shadow-lg: 0 8px 24px rgba(0,0,0,0.4);
    }
  }

  /* ===== Base Styles ===== */
  .cv-page {
    font-family: var(--font-sans);
    font-size: 18px;
    line-height: 1.7;
    color: var(--color-text);
    background: var(--color-bg);
    max-width: 900px;
    margin: 0 auto;
    padding: var(--spacing-lg);
  }

  .cv-page a {
    color: var(--color-accent);
    text-decoration: none;
    transition: color 0.2s ease;
  }
  .cv-page a:hover {
    color: var(--color-accent-hover);
    text-decoration: underline;
  }

  .cv-page h1 {
    font-size: 2.4em;
    font-weight: 700;
    margin: 0 0 var(--spacing-xs);
    letter-spacing: -0.02em;
    line-height: 1.2;
  }

  .cv-page h2 {
    font-size: 1.6em;
    font-weight: 600;
    margin: var(--spacing-xl) 0 var(--spacing-md);
    padding-bottom: var(--spacing-xs);
    border-bottom: 2px solid var(--color-border);
    letter-spacing: -0.01em;
  }

  .cv-page p {
    margin: 0 0 var(--spacing-sm);
  }

  .cv-page ul {
    padding-left: 24px;
    margin: var(--spacing-sm) 0;
  }

  .cv-page li {
    margin-bottom: var(--spacing-xs);
  }

  /* ===== Header Layout ===== */
  .cv-header {
    display: flex;
    gap: var(--spacing-lg);
    align-items: flex-start;
    margin-bottom: var(--spacing-lg);
    flex-wrap: wrap;
  }

  .cv-photo {
    flex-shrink: 0;
  }
  .cv-photo img {
    width: 170px;
    height: 170px;
    object-fit: cover;
    border: 2px solid var(--color-border);
    border-radius: var(--radius-lg);
    box-shadow: var(--shadow-md);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .cv-photo img:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-lg);
  }

  .cv-header-content {
    flex: 1;
    min-width: 300px;
  }

  .cv-bio {
    font-size: 1.05em;
    line-height: 1.8;
    margin: var(--spacing-sm) 0;
  }

  .cv-highlight {
    background: var(--color-panel);
    padding: var(--spacing-md);
    border-left: 4px solid var(--color-accent);
    border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
    margin: var(--spacing-md) 0;
    box-shadow: var(--shadow-sm);
  }

  .cv-skills-list {
    margin: var(--spacing-sm) 0 0;
    padding-left: 20px;
    font-size: 0.98em;
  }
  .cv-skills-list li {
    margin-bottom: 4px;
  }

  .cv-contact {
    display: flex;
    gap: var(--spacing-md);
    flex-wrap: wrap;
    margin-top: var(--spacing-sm);
    font-size: 0.95em;
  }
  .cv-contact a {
    font-weight: 500;
  }

  /* ===== Cards: Papers & Projects ===== */
  .cv-card {
    background: var(--color-panel);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: var(--spacing-lg);
    margin-bottom: var(--spacing-lg);
    box-shadow: var(--shadow-sm);
    transition: box-shadow 0.2s ease, transform 0.2s ease;
  }
  .cv-card:hover {
    box-shadow: var(--shadow-md);
    transform: translateY(-2px);
  }

  .cv-card-title {
    font-size: 1.2em;
    font-weight: 700;
    margin: 0 0 var(--spacing-xs);
    line-height: 1.3;
  }

  .cv-card-venue {
    font-size: 0.95em;
    color: var(--color-text-muted);
    margin: 0 0 var(--spacing-sm);
    font-weight: 500;
  }

  .cv-card p {
    font-size: 0.98em;
    margin-bottom: var(--spacing-sm);
  }

  .cv-card ul {
    font-size: 0.98em;
    margin: var(--spacing-sm) 0;
  }

  .cv-card-links {
    margin-top: var(--spacing-md);
    display: flex;
    gap: var(--spacing-sm);
    flex-wrap: wrap;
    align-items: center;
  }

  /* ===== Buttons ===== */
  .btn {
    display: inline-flex;
    align-items: center;
    padding: 8px 16px;
    background: var(--color-accent);
    color: white;
    border-radius: var(--radius-sm);
    font-weight: 500;
    font-size: 0.95em;
    text-decoration: none;
    transition: background 0.2s ease, transform 0.1s ease;
    border: none;
    cursor: pointer;
  }
  .btn:hover {
    background: var(--color-accent-hover);
    text-decoration: none;
    transform: translateY(-1px);
  }
  .btn-secondary {
    background: var(--color-panel);
    color: var(--color-text);
    border: 1px solid var(--color-border);
  }
  .btn-secondary:hover {
    background: var(--color-border);
  }

  /* ===== Tags ===== */
  .tag {
    display: inline-block;
    font-size: 0.8em;
    font-weight: 500;
    padding: 4px 10px;
    background: var(--color-border);
    color: var(--color-text);
    border-radius: 20px;
    margin-right: 8px;
    margin-bottom: 6px;
  }

  /* ===== Education Section ===== */
  .cv-education-item {
    margin-bottom: var(--spacing-md);
  }
  .cv-education-item strong {
    font-weight: 600;
  }

  /* ===== Responsive Design ===== */
  @media (max-width: 768px) {
    .cv-page {
      padding: var(--spacing-md);
    }
    .cv-header {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
    .cv-contact {
      justify-content: center;
    }
    .cv-card-links {
      justify-content: center;
    }
  }

  /* ===== Print Styles ===== */
  @media print {
    .cv-page {
      padding: 0;
      max-width: none;
      font-size: 11pt;
      color: #000;
      background: #fff;
    }
    .cv-card, .cv-highlight {
      box-shadow: none;
      border: 1px solid #ccc;
      break-inside: avoid;
    }
    .cv-photo img {
      border: 1px solid #ccc;
    }
    a {
      color: #000;
      text-decoration: none;
    }
    .btn {
      background: none;
      color: #000;
      border: 1px solid #000;
      padding: 4px 12px;
    }
  }

  /* ===== Accessibility ===== */
  @media (prefers-reduced-motion: reduce) {
    * {
      transition: none !important;
      animation: none !important;
    }
  }
  .cv-page a:focus,
  .btn:focus {
    outline: 2px solid var(--color-accent);
    outline-offset: 2px;
  }
</style>

<div class="cv-page">

<div class="cv-header">
  <div class="cv-photo">
    <img src="assets/personal_photo.png" alt="Vadim Atlassov">
  </div>

  <div class="cv-header-content">
    <h1>Vadim Atlassov</h1>
    <p class="cv-bio">
      MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
      <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
      Research focus: <strong>physically-grounded generative AI</strong> for medicine and civil engineering.
    </p>
    <div class="cv-highlight">
      <strong>Actively seeking PhD positions.</strong> Research interests include:
      <ul class="cv-skills-list">
        <li><strong>Generative AI:</strong> Latent Diffusion (LDM), Flow Matching, Latent Disentanglement, Spatial-Latent Alignment.</li>
        <li><strong>Multimodal Learning:</strong> Vision-Language Models (VLM), Mixture-of-Experts (MoE) Adapters, DINOv2, Semantic Grounding.</li>
        <li><strong>Domain Applications:</strong> Medical Imaging (Chest X-ray, Hematology), AI in Structural Engineering Monitoring (RC Beam Failure Diagnosis).</li>
      </ul>
    </div>
    <div class="cv-contact">
      <a href="https://www.linkedin.com/in/vadim-atlassov" target="_blank" rel="noopener">LinkedIn</a>
      <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
      <a href="https://github.com/Vadim-ATL" target="_blank" rel="noopener">GitHub</a>
    </div>
  </div>
</div>

## Education {#education}

<div class="cv-education-item">
* **M.Sc. in Electrical & Computer Engineering**, Nazarbayev University (2024; GPA 3.21/4.0)
* *Academic Exchange:* Brno University of Technology, Czech Republic
* Hands-on experience training large-scale image generative models, including diffusion and flow matching architectures
</div>

## Publications & Preprints {#publications}

<div class="cv-card">
  <div class="cv-card-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
  <div class="cv-card-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review</div>
  <p>
    <strong>Quantitative Results:</strong> On the <a href="https://physionet.org/content/mimic-cxr/2.1.0/" style="color: inherit; text-decoration: none;">MIMIC-CXR</a> dataset, the model achieved a <abbr title="Fréchet Inception Distance">FID</abbr> of 56.78 and a DICE coefficient of lung masks of 0.6536 (anatomical fidelity).
  </p>
  <p>
    <strong>Clinical Utility:</strong> Data augmentation with the model's synthetic images improved downstream diagnostic accuracy by 17.5% and 4.2% AUC for pneumonia classification.
  </p>
  <p>
    <strong>Radiologist Validation:</strong> Board-certified radiologists rated the model highly for anatomical plausibility (3.8/5) and pathology expression (3.95/5), outperforming baselines (Roentgen, Cheff, XReal).
  </p>
  <div class="cv-card-links">
    <a class="btn btn-secondary" href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
    <span style="margin: 0 8px; color: var(--color-border);">|</span>
    <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing" target="_blank" rel="noopener">Paper (Preprint)</a>
  </div>
</div>

<div class="cv-card">
  <div class="cv-card-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
  <div class="cv-card-venue">Journal of Building Engineering — Under Review</div>
  <p>
    <strong>Quantitative Results:</strong> The model demonstrated high fidelity and structural consistency in generating failure states, achieving a <abbr title="Kernel Inception Distance">KID</abbr> of 0.0628 and an <abbr title="Structural Similarity Index">SSIM</abbr> of 0.790.
  </p>
  <p>
    <strong>Diagnostic Accuracy Gains:</strong> Synthetic data augmentation significantly enhanced automated diagnostic performance:
  </p>
  <ul style="margin-top: 4px; margin-bottom: 12px;">
    <li>Failure-Type Classification: <strong>+5.2%</strong> (to 85.8%)</li>
    <li>Rebar Exposure Detection: <strong>+11.9%</strong> (to 95.2%)</li>
    <li>Flexural Cracking Detection: <strong>+12.9%</strong> (to 84.3%)</li>
    <li>Concrete Spalling Detection: <strong>+11.5%</strong> (to 85.3%)</li>
  </ul>
  <p>
    <strong>Expert Validation:</strong> Structural specialists rated the outputs on a 5-point scale — Structural Realism: 4.12/5; Assessment Clarity: 3.98/5.
  </p>
  <div class="cv-card-links">
    <a class="btn btn-secondary" href="https://github.com/nubcico/GenBeamJoint" target="_blank" rel="noopener">Code</a>
    <span style="margin: 0 8px; color: var(--color-border);">|</span>
    <a href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing" target="_blank" rel="noopener">Paper (Preprint)</a>
  </div>
</div>

## Projects {#projects}

<div class="cv-card">
  <div class="cv-card-title"><a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM" style="color: inherit;">BloodMNIST-DDPM</a></div>
  <p style="margin-top: 8px;">
    Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.
  </p>
  <div style="margin-top: 12px;">
    <span class="tag">Medical Imaging</span>
    <span class="tag">DDPM</span>
    <span class="tag">Hematology</span>
  </div>
</div>

</div>
