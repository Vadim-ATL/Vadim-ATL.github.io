---
layout: default
title: Vadim Atlassov - Researcher
---

<style>
  .cv-page {
    --cv-text: var(--text, #242424);
    --cv-muted: var(--text-muted, #626262);
    --cv-border: var(--border, #e7e2dc);
    --cv-panel: var(--panel, #f7f6f3);
    --cv-link: var(--link, #0b66c3);
    --cv-max: 840px;

    max-width: var(--cv-max);
    margin: 0 auto;
    color: var(--cv-text);
    font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    font-size: 15.8px;
    line-height: 1.58;
    letter-spacing: 0;
  }

  .cv-page a {
    color: var(--cv-link);
    text-decoration: none;
    text-underline-offset: 3px;
  }

  .cv-page a:hover {
    text-decoration: underline;
  }

  .cv-page h1,
  .cv-page h2,
  .cv-page h3,
  .cv-page p,
  .cv-page ul {
    margin-top: 0;
  }

  .cv-page h1 {
    margin-bottom: 6px;
    font-size: clamp(2rem, 5vw, 2.55rem);
    line-height: 1.05;
    font-weight: 750;
    letter-spacing: 0;
  }

  .cv-page h2 {
    display: flex;
    align-items: center;
    gap: 12px;
    margin: 34px 0 15px;
    color: #171717;
    font-size: 0.82rem;
    line-height: 1.2;
    font-weight: 750;
    letter-spacing: 0.09em;
    text-transform: uppercase;
  }

  .cv-page h2::after {
    content: "";
    height: 1px;
    flex: 1;
    background: var(--cv-border);
  }

  .cv-page ul {
    padding-left: 1.1rem;
    margin-bottom: 0;
  }

  .cv-page li {
    margin-bottom: 5px;
  }

  .cv-page .profile-header {
    display: grid;
    grid-template-columns: 116px minmax(0, 1fr);
    gap: 24px;
    align-items: start;
    padding-bottom: 26px;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-page .profile-photo {
    width: 116px;
    height: 116px;
    object-fit: cover;
    border-radius: 7px;
    background: var(--cv-panel);
  }

  .cv-page .bio {
    max-width: 68ch;
    margin-bottom: 14px;
    color: #2f2f2f;
    font-size: 1.02rem;
    line-height: 1.55;
  }

  .cv-page .phd-status {
    margin: 16px 0 14px;
    padding: 13px 15px;
    border: 1px solid var(--cv-border);
    border-left: 3px solid var(--cv-link);
    border-radius: 6px;
    background: color-mix(in srgb, var(--cv-panel) 72%, transparent);
  }

  .cv-page .phd-status > strong {
    display: block;
    margin-bottom: 8px;
  }

  .cv-page .skills-list {
    display: grid;
    gap: 4px;
    padding-left: 1rem;
    color: var(--cv-muted);
    font-size: 0.93rem;
    line-height: 1.48;
  }

  .cv-page .skills-list strong {
    color: var(--cv-text);
  }

  .cv-page .contact {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 12px;
  }

  .cv-page .contact a,
  .cv-page .paper-links a {
    display: inline-flex;
    align-items: center;
    min-height: 32px;
    padding: 5px 10px;
    border: 1px solid var(--cv-border);
    border-radius: 6px;
    color: var(--cv-text);
    background: #fff;
    font-size: 0.9rem;
    font-weight: 650;
  }

  .cv-page .contact a:hover,
  .cv-page .paper-links a:hover {
    border-color: color-mix(in srgb, var(--cv-link) 38%, var(--cv-border));
    color: var(--cv-link);
    text-decoration: none;
  }

  .cv-page .compact-list {
    color: #343434;
  }

  .cv-page .paper,
  .cv-page .project {
    padding: 0 0 22px;
    margin-bottom: 22px;
    border-bottom: 1px solid var(--cv-border);
  }

  .cv-page .project:last-child,
  .cv-page .paper:last-of-type {
    border-bottom: 0;
  }

  .cv-page .paper-title,
  .cv-page .project-title {
    margin-bottom: 4px;
    color: #171717;
    font-size: 1.05rem;
    line-height: 1.35;
    font-weight: 750;
  }

  .cv-page .paper-venue {
    margin-bottom: 10px;
    color: var(--cv-muted);
    font-size: 0.91rem;
    font-style: italic;
  }

  .cv-page .paper p,
  .cv-page .project p {
    margin-bottom: 8px;
    color: #333;
    font-size: 0.95rem;
    line-height: 1.53;
  }

  .cv-page .paper-points {
    display: grid;
    gap: 8px;
    margin-bottom: 12px;
  }

  .cv-page .metric-list {
    columns: 2;
    column-gap: 28px;
    margin: 4px 0 12px;
    color: #333;
    font-size: 0.94rem;
  }

  .cv-page .paper-links {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 12px;
  }

  .cv-page .link-separator {
    display: none;
  }

  .cv-page .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 10px;
  }

  .cv-page .tag {
    display: inline-flex;
    align-items: center;
    min-height: 24px;
    padding: 2px 8px;
    border-radius: 999px;
    color: #555;
    background: var(--cv-panel);
    font-size: 0.78rem;
    font-weight: 600;
  }

  @media (max-width: 640px) {
    .cv-page {
      font-size: 15.5px;
    }

    .cv-page .profile-header {
      grid-template-columns: 82px minmax(0, 1fr);
      gap: 16px;
    }

    .cv-page .profile-photo {
      width: 82px;
      height: 82px;
    }

    .cv-page .bio {
      font-size: 0.98rem;
    }

    .cv-page .phd-status {
      grid-column: 1 / -1;
    }

    .cv-page .contact {
      grid-column: 1 / -1;
    }

    .cv-page .metric-list {
      columns: 1;
    }
  }
</style>

<div class="cv-page">

  <div class="profile-header">
    <img class="profile-photo" src="assets/personal_photo.png" alt="Vadim Atlassov">
    <div class="profile-info">
      <h1>Vadim Atlassov</h1>
      <p class="bio">
        MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
        <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
        Research focus: <strong>physically grounded generative AI</strong> for medicine and civil engineering.
      </p>
      <div class="phd-status">
        <strong>Actively seeking PhD positions.</strong>
        <ul class="skills-list">
          <li><strong>Generative AI:</strong> Latent Diffusion, Flow Matching, Latent Disentanglement, Spatial-Latent Alignment.</li>
          <li><strong>Multimodal Learning:</strong> Vision-Language Models, MoE Adapters, DINOv2, Semantic Grounding.</li>
          <li><strong>Applications:</strong> Medical Imaging and AI for Structural Engineering Monitoring.</li>
        </ul>
      </div>
      <div class="contact" aria-label="Contact links">
        <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
        <a href="https://github.com/Vadim-ATL">GitHub</a>
        <a href="https://www.linkedin.com/in/vadim-atlassov">LinkedIn</a>
      </div>
    </div>
  </div>

  <h2 id="education">Education</h2>

  <ul class="compact-list">
    <li><strong>M.Sc. in Electrical &amp; Computer Engineering</strong>, Nazarbayev University (2024; GPA 3.21/4.0)</li>
    <li><em>Academic Exchange:</em> Brno University of Technology, Czech Republic</li>
    <li>Hands-on experience training large-scale image generative models, including diffusion and flow matching architectures</li>
  </ul>

  <h2 id="publications">Publications &amp; Preprints</h2>

  <div class="paper">
    <div class="paper-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
    <div class="paper-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 - Under Review</div>
    <div class="paper-points">
      <p><strong>Quantitative results:</strong> On the <a href="https://physionet.org/content/mimic-cxr/2.1.0/">MIMIC-CXR</a> dataset, achieved <abbr title="Frechet Inception Distance">FID</abbr> 56.78 and lung-mask DICE 0.6536.</p>
      <p><strong>Clinical utility:</strong> Synthetic augmentation improved downstream diagnostic accuracy by 17.5% and pneumonia classification AUC by 4.2%.</p>
      <p><strong>Radiologist validation:</strong> Board-certified radiologists rated anatomical plausibility 3.8/5 and pathology expression 3.95/5, outperforming Roentgen, Cheff, and XReal baselines.</p>
    </div>
    <div class="paper-links">
      <a href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
      <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing">Preprint</a>
    </div>
  </div>

  <div class="paper">
    <div class="paper-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
    <div class="paper-venue">Journal of Building Engineering - Under Review</div>
    <div class="paper-points">
      <p><strong>Quantitative results:</strong> High-fidelity failure-state generation with <abbr title="Kernel Inception Distance">KID</abbr> 0.0628 and <abbr title="Structural Similarity Index">SSIM</abbr> 0.790.</p>
      <p><strong>Diagnostic accuracy gains:</strong> Synthetic data augmentation improved failure-type classification and visual damage detection.</p>
    </div>
    <ul class="metric-list">
      <li>Failure-Type Classification: <strong>+5.2%</strong> to 85.8%</li>
      <li>Rebar Exposure Detection: <strong>+11.9%</strong> to 95.2%</li>
      <li>Flexural Cracking Detection: <strong>+12.9%</strong> to 84.3%</li>
      <li>Concrete Spalling Detection: <strong>+11.5%</strong> to 85.3%</li>
    </ul>
    <p><strong>Expert validation:</strong> Structural specialists rated outputs on a 5-point scale: Structural Realism 4.12/5; Assessment Clarity 3.98/5.</p>
    <div class="paper-links">
      <a href="https://github.com/nubcico/GenBeamJoint" target="_blank" rel="noopener">Code</a>
      <a href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing">Preprint</a>
    </div>
  </div>

  <h2 id="projects">Projects</h2>

  <div class="project">
    <div class="project-title"><a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM">BloodMNIST-DDPM</a></div>
    <p>
      Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.
    </p>
    <div class="tags">
      <span class="tag">Medical Imaging</span>
      <span class="tag">DDPM</span>
      <span class="tag">Hematology</span>
    </div>
  </div>

</div>
