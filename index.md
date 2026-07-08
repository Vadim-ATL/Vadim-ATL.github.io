<style>
  .cv-page {
    font-size: 16px;
    line-height: 1.65;
    color: var(--text, #1a1a1a);
    max-width: 100%;
  }

  .cv-page h1 {
    font-size: 2.4em;
    margin: 0 0 10px 0;
    letter-spacing: -0.03em;
    font-weight: 700;
    line-height: 1.15;
  }

  .cv-page h2 {
    font-size: 1.3em;
    margin-top: 48px;
    margin-bottom: 20px;
    padding-bottom: 10px;
    border-bottom: 1.5px solid var(--border, #e5e7eb);
    letter-spacing: -0.01em;
    font-weight: 600;
    color: var(--text, #1a1a1a);
  }

  .cv-page .profile-header {
    display: flex;
    gap: 36px;
    align-items: flex-start;
    margin-bottom: 32px;
  }

  .cv-page .profile-photo {
    width: 160px;
    height: 160px;
    object-fit: cover;
    border-radius: 10px;
    flex-shrink: 0;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  }

  .cv-page .profile-info {
    flex: 1;
  }

  .cv-page .bio {
    font-size: 1.05em;
    line-height: 1.7;
    margin-bottom: 18px;
    color: var(--text, #1a1a1a);
  }

  .cv-page .phd-status {
    border-left: 3px solid var(--link, #2563eb);
    padding-left: 18px;
    margin: 22px 0;
    background: var(--panel, #f3f4f6);
    padding: 16px 18px 16px 18px;
    border-radius: 0 8px 8px 0;
  }

  .cv-page .phd-status > strong:first-child {
    display: block;
    margin-bottom: 10px;
    font-size: 1.05em;
  }

  .cv-page .skills-list {
    font-size: 0.95em;
    margin-top: 10px;
    padding-left: 20px;
  }

  .cv-page .skills-list li {
    margin-bottom: 8px;
    line-height: 1.55;
  }

  .cv-page .contact {
    margin-top: 18px;
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }

  .cv-page .contact a {
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95em;
    color: var(--link, #2563eb);
    transition: color 0.15s ease;
  }

  .cv-page .contact a:hover {
    text-decoration: underline;
    color: var(--link-hover, #1d4ed8);
  }

  /* Paper styling */
  .cv-page .paper {
    margin-bottom: 36px;
    padding-bottom: 0;
    background: var(--card-bg, #ffffff);
    border: 1px solid var(--border, #e5e7eb);
    border-radius: 10px;
    padding: 24px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.04);
    transition: box-shadow 0.2s ease, transform 0.15s ease;
  }

  .cv-page .paper:hover {
    box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    transform: translateY(-1px);
  }

  .cv-page .paper-title {
    font-size: 1.1em;
    font-weight: 700;
    margin-bottom: 6px;
    line-height: 1.35;
    color: var(--text, #1a1a1a);
  }

  .cv-page .paper-venue {
    font-size: 0.92em;
    color: var(--text-muted, #6b7280);
    margin-bottom: 14px;
    font-style: italic;
  }

  .cv-page .paper p {
    font-size: 0.95em;
    margin: 0 0 10px 0;
    line-height: 1.6;
  }

  .cv-page .paper ul {
    font-size: 0.95em;
    margin-top: 6px;
    margin-bottom: 14px;
    padding-left: 20px;
  }

  .cv-page .paper ul li {
    margin-bottom: 5px;
    line-height: 1.5;
  }

  .cv-page .paper-links {
    margin-top: 14px;
    font-size: 0.9em;
    padding-top: 12px;
    border-top: 1px solid var(--border, #e5e7eb);
  }

  .cv-page .paper-links a {
    text-decoration: none;
    font-weight: 500;
    color: var(--link, #2563eb);
    transition: color 0.15s ease;
  }

  .cv-page .paper-links a:hover {
    text-decoration: underline;
    color: var(--link-hover, #1d4ed8);
  }

  .cv-page .link-separator {
    color: var(--text-muted, #d1d5db);
    margin: 0 10px;
    font-weight: 300;
  }

  .cv-page .news-item {
    display: flex;
    gap: 18px;
    margin-bottom: 16px;
    font-size: 0.95em;
    align-items: baseline;
    padding: 10px 0;
    border-bottom: 1px solid var(--border, #f0f0f0);
  }

  .cv-page .news-item:last-child {
    border-bottom: none;
  }

  .cv-page .news-date {
    min-width: 90px;
    color: var(--text-muted, #6b7280);
    font-size: 0.88em;
    flex-shrink: 0;
    font-weight: 500;
    font-variant-numeric: tabular-nums;
  }

  .cv-page .project {
    margin-bottom: 24px;
    background: var(--card-bg, #ffffff);
    border: 1px solid var(--border, #e5e7eb);
    border-radius: 10px;
    padding: 24px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.04);
    transition: box-shadow 0.2s ease, transform 0.15s ease;
  }

  .cv-page .project:hover {
    box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    transform: translateY(-1px);
  }

  .cv-page .project-title {
    font-size: 1.05em;
    font-weight: 700;
    margin-bottom: 8px;
  }

  .cv-page .project-title a {
    text-decoration: none;
    color: var(--link, #2563eb);
    transition: color 0.15s ease;
  }

  .cv-page .project-title a:hover {
    text-decoration: underline;
    color: var(--link-hover, #1d4ed8);
  }

  .cv-page .project p {
    font-size: 0.95em;
    margin: 0 0 14px 0;
    line-height: 1.6;
    color: var(--text, #1a1a1a);
  }

  .cv-page .tag {
    font-size: 0.78em;
    color: var(--text-muted, #6b7280);
    background: var(--tag-bg, #e5e7eb);
    padding: 4px 10px;
    border-radius: 4px;
    margin-right: 6px;
    display: inline-block;
    font-weight: 500;
    letter-spacing: 0.01em;
  }

  .cv-page ul {
    padding-left: 20px;
  }

  .cv-page li {
    margin-bottom: 8px;
    line-height: 1.6;
  }

  /* Paper preview image */
  .cv-page .paper-preview {
    width: 170px;
    height: 170px;
    object-fit: cover;
    border-radius: 8px;
    flex-shrink: 0;
    box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  }

  @media (max-width: 640px) {
    .cv-page .profile-header {
      flex-direction: column;
      gap: 20px;
      align-items: center;
      text-align: center;
    }
    .cv-page .contact {
      justify-content: center;
    }
    .cv-page .phd-status {
      text-align: left;
    }
    .cv-page .paper {
      padding: 18px;
    }
    .cv-page .project {
      padding: 18px;
    }
    .cv-page h1 {
      font-size: 2em;
    }
    .cv-page .paper-preview {
      width: 100%;
      height: 200px;
      margin-bottom: 16px;
    }
    .cv-page .paper > div:first-child {
      flex-direction: column !important;
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
    Research focus: <strong>physically-grounded generative AI</strong> for medicine and civil engineering.
  </p>

  <div class="phd-status">
    <strong>Actively seeking PhD positions.</strong> Research interests include:
    <ul class="skills-list">
      <li><strong>Generative AI:</strong> Latent Diffusion (LDM), Flow Matching, Latent Disentanglement, Spatial-Latent Alignment.</li>
      <li><strong>Multimodal Learning:</strong> Vision-Language Models (VLM), Mixture-of-Experts (MoE) Adapters, DINOv2, Semantic Grounding.</li>
      <li><strong>Domain Applications:</strong> Medical Imaging (Chest X-ray, Mammography), AI for Structural Health Monitoring (RC Beam Failure Diagnosis).</li>
    </ul>
  </div>

  <div class="contact">
    <a href="https://www.linkedin.com/in/vadim-atlassov">LinkedIn</a>
    <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
    <a href="https://github.com/Vadim-ATL">GitHub</a>
    <a href="https://scholar.google.com/citations?hl=ko&user=1IG1kf0AAAAJ">Scholar</a>
  </div>
</div>
  </div>
  <h2 id="publications">Publications &amp; Preprints</h2>
  <div class="paper">
    <div style="display: flex; gap: 24px; align-items: flex-start;">
      <img class="paper-preview" src="assets/jbe_preview.png" alt="RC joint failure generation preview">
      <div style="flex: 1;">
        <div class="paper-title">Controllable Diffusion-Based Image Generation for Failure Diagnosis of Reinforced Concrete Beam–Column Joints</div>
        <div class="paper-venue">Journal of Building Engineering, Vol. 128 (2026) 116466 — Elsevier, IF 7.4, Q1 — <strong>Accepted</strong></div>
        <p>
          <strong>Quantitative Results:</strong> The model demonstrated high fidelity and structural consistency, achieving a <abbr title="Kernel Inception Distance">KID</abbr> of 0.0628 and <abbr title="Structural Similarity Index">SSIM</abbr> of 0.790, outperforming ControlNet, CycleGAN, and Pix2Pix baselines.
        </p>
        <p><strong>Diagnostic Accuracy Gains:</strong></p>
        <ul>
          <li>Failure-Type Classification: <strong>+5.2%</strong> (to 85.8%)</li>
          <li>Rebar Exposure Detection: <strong>+11.9%</strong> (to 95.2%)</li>
          <li>Flexural Cracking Detection: <strong>+12.9%</strong> (to 84.3%)</li>
          <li>Concrete Spalling Detection: <strong>+11.5%</strong> (to 85.3%)</li>
        </ul>
        <p>
          <strong>Expert Validation:</strong> Structural Realism: 4.12/5; Assessment Clarity: 3.98/5.
        </p>
        <div class="paper-links">
          <a href="https://github.com/nubcico/GenBeamJoint" target="_blank" rel="noopener">Code</a>
          <span class="link-separator">|</span>
          <a href="https://doi.org/10.1016/j.jobe.2026.116466" target="_blank" rel="noopener">Paper</a>
        </div>
      </div>
    </div>
  </div>
  <div class="paper">
    <div style="display: flex; gap: 24px; align-items: flex-start;">
      <img class="paper-preview" src="assets/cxr_preview.png" alt="Chest X-ray synthesis preview">
      <div style="flex: 1;">
        <div class="paper-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
        <div class="paper-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review</div>
        <p>
          <strong>Quantitative Results:</strong> On the <a href="https://physionet.org/content/mimic-cxr/2.1.0/" style="color: inherit; text-decoration: none;">MIMIC-CXR</a> dataset, the model achieved <abbr title="Fréchet Inception Distance">FID</abbr> 45.38, MS-SSIM 0.736, and Dice 0.6564, outperforming RoentGen, CheXGen, and XReal baselines.
        </p>
        <p>
          <strong>Clinical Utility:</strong> Synthetic augmentation improved downstream pneumonia classification accuracy by 17.5% and AUC by 4.2%.
        </p>
        <p>
          <strong>Radiologist Validation:</strong> Anatomical plausibility 3.8/5; pathology expression 3.95/5.
        </p>
        <div class="paper-links">
          <a href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
        </div>
      </div>
    </div>
  </div>
  <div class="paper">
    <div style="display: flex; gap: 24px; align-items: flex-start;">
      <img class="paper-preview" src="assets/rc_bcj_dataset_preview.png" alt="RC-BCJ-Dataset preview">
      <div style="flex: 1;">
        <div class="paper-title">RC-BCJ-Dataset: A Benchmark Image Dataset of Reinforced Concrete Beam–Column Joint Failures</div>
        <div class="paper-venue">Scientific Data (Nature Portfolio), 2026 — Under Review</div>
        <p>
          <strong>Dataset Overview:</strong> 572 annotated images of RC beam–column joint failures with expert-verified multi-attribute annotations for structural damage recognition, vision–language modeling, and generative modeling.
        </p>
        <p><strong>Annotations:</strong></p>
        <ul>
          <li><strong>Categorical labels:</strong> Joint type, failure mechanism (B / J / BJ), damage type, damage severity (DS0–DS4)</li>
          <li><strong>1,716 expert-written diagnostic descriptions</strong> (3 per image) for image-to-text and multimodal learning</li>
          <li><strong>Segmentation masks</strong> for background, beam, column, and joint-core regions</li>
        </ul>
        <p>
          <strong>Baseline Results:</strong> Failure-mode classification up to 70.30% accuracy (ViT-B/16); best image-to-text generation (Qwen3-VL-4B): BLEU-4 0.82, BERTScore 0.98.
        </p>
        <div class="paper-links">
          <a href="https://zenodo.org/records/20268086" target="_blank" rel="noopener">Dataset</a>
          <span class="link-separator">|</span>
          <a href="https://github.com/nubcico/RC-BCJ-Dataset" target="_blank" rel="noopener">Code</a>
        </div>
      </div>
    </div>
  </div>
  <h2 id="news">News</h2>
  <div class="news-item">
    <span class="news-date">Jun 2026</span>
    <span>Paper accepted at <strong>Journal of Building Engineering</strong> (Elsevier, IF 7.4, Q1) — controllable diffusion for RC structural failure diagnosis. <a href="https://doi.org/10.1016/j.jobe.2026.116466">DOI</a></span>
  </div>
  <div class="news-item">
    <span class="news-date">2026</span>
    <span>Benchmark dataset paper on RC beam-column joint failures submitted to <strong>Scientific Data</strong> (Nature Portfolio) — under review.</span>
  </div>
  <div class="news-item">
    <span class="news-date">2025</span>
    <span>Paper on latent-aligned diffusion for chest X-ray synthesis submitted to <strong>Computerized Medical Imaging and Graphics</strong> — Under review.</span>
  </div>
  <h2 id="projects">Projects</h2>
    <div style="display: flex; gap: 24px; align-items: flex-start;">
      <img class="paper-preview" src="assets/counterfactual_cxr_preview.png" alt="Counterfactual CXR preview" style="width: 140px; height: 140px;">
      <div style="flex: 1;">
        <div class="project-title"><a href="https://github.com/Vadim-ATL/Counterfactual-CXR-Generation">Counterfactual Chest X-Ray Generation</a></div>
        <p style="margin-top: 10px;">
          Disentangled anatomy and diffusion transformers (SiT) for counterfactual disease trajectory generation in chest X-rays. Simulates realistic progression (Healthy → Sick) and regression (Sick → Healthy) while preserving patient identity via orthogonal spatial latents.
        </p>
        <div style="margin-top: 14px;">
          <span class="tag">Medical Imaging</span>
          <span class="tag">Diffusion Transformers</span>
          <span class="tag">Counterfactual</span>
          <span class="tag">MIMIC-CXR</span>
        </div>
      </div>
    </div>
  </div>

  <div class="project">
    <div style="display: flex; gap: 24px; align-items: flex-start;">
      <img class="paper-preview" src="assets/bloodmnist_preview.png" alt="BloodMNIST preview" style="width: 140px; height: 140px;">
      <div style="flex: 1;">
        <div class="project-title"><a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM">BloodMNIST-DDPM</a></div>
        <p style="margin-top: 10px;">
          Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.
        </p>
        <div style="margin-top: 14px;">
          <span class="tag">Medical Imaging</span>
          <span class="tag">DDPM</span>
          <span class="tag">Hematology</span>
        </div>
      </div>
    </div>
  </div>
</div>