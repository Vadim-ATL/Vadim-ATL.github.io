---
layout: default
title: Vadim Atlassov - Researcher
---

<style>
  .cv-page { font-size: 18px; line-height: 1.7; }
  .cv-page h1 { font-size: 2.4em; margin-top: 0; margin-bottom: 8px; letter-spacing: -0.02em; }
  .cv-page h2 { font-size: 1.6em; margin-top: 48px; margin-bottom: 20px; padding-bottom: 10px; border-bottom: 2px solid var(--border); letter-spacing: -0.01em; }
  .cv-page .bio { font-size: 1.1em; line-height: 1.8; }
  .cv-page .skills-list { font-size: 0.95em; }
  .cv-page .skills-list li { margin-bottom: 6px; }
  .cv-page .contact { font-size: 1em; margin-top: 16px; }
  .cv-page .contact a { font-size: 1em; }
  .cv-page .paper { background: var(--panel); border: 1px solid var(--border); border-radius: 12px; padding: 28px 32px; margin-bottom: 28px; }
  .cv-page .paper-title { font-size: 1.2em; font-weight: 700; margin-bottom: 6px; }
  .cv-page .paper-venue { font-size: 0.95em; color: var(--text-muted, #666); margin-bottom: 14px; }
  .cv-page .paper p { font-size: 0.95em; margin-bottom: 10px; }
  .cv-page .paper ul { font-size: 0.95em; }
  .cv-page .paper-links { margin-top: 18px; font-size: 0.95em; }
  .cv-page .project { background: var(--panel); border: 1px solid var(--border); border-radius: 12px; padding: 24px 28px; }
  .cv-page .project-title { font-size: 1.15em; font-weight: 700; }
  .cv-page .project p { font-size: 0.95em; }
  .cv-page .tag { font-size: 0.82em; }
  .cv-page ul { padding-left: 22px; }
  .cv-page li { margin-bottom: 8px; }
</style>

<div class="cv-page">

<div style="display: flex; gap: 36px; align-items: flex-start; margin-bottom: 12px;">
  <div style="flex-shrink: 0;">
    <img src="assets/personal_photo.png" alt="Vadim Atlassov" style="width: 170px; height: 170px; object-fit: cover; border: 2px solid var(--border); border-radius: 16px;">
  </div>

  <div style="flex: 1;">
    <h1>Vadim Atlassov</h1>
    <p class="bio">
      MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
      <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
      Research focus: <strong>physically-grounded generative AI</strong> for medicine and civil engineering.
    </p>
    <div style="background-color: var(--panel); padding: 18px 22px; border-left: 5px solid var(--link); border-radius: 0 10px 10px 0; margin: 20px 0;">
      <strong>Actively seeking PhD positions.</strong> Research interests include:
      <ul class="skills-list">
        <li><strong>Generative AI:</strong> Latent Diffusion (LDM), Flow Matching, Latent Disentanglement, Spatial-Latent Alignment.</li>
        <li><strong>Multimodal Learning:</strong> Vision-Language Models (VLM), Mixture-of-Experts (MoE) Adapters, DINOv2, Semantic Grounding.</li>
        <li><strong>Domain Applications:</strong> Medical Imaging (Chest X-ray, Hematology), AI in Structural Engineering Monitoring (RC Beam Failure Diagnosis).</li>
      </ul>
    </div>
    <div class="contact">
      <a href="https://www.linkedin.com/in/vadim-atlassov">LinkedIn</a>
      <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
      <a href="https://github.com/Vadim-ATL">GitHub</a>
    </div>
  </div>
</div>

## Education {#education}

* **M.Sc. in Electrical & Computer Engineering**, Nazarbayev University (2024; GPA 3.21/4.0)
* *Academic Exchange:* Brno University of Technology, Czech Republic
* Hands-on experience training large-scale image generative models, including diffusion and flow matching architectures

## Publications & Preprints {#publications}

<div class="paper">
  <div class="paper-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
  <div class="paper-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review</div>
  <p>
    <strong>Quantitative Results:</strong> On the <a href="https://physionet.org/content/mimic-cxr/2.1.0/" style="color: inherit; text-decoration: none;">MIMIC-CXR</a> dataset, the model achieved a <abbr title="Fréchet Inception Distance">FID</abbr> of 56.78 and a DICE coefficient of lung masks of 0.6536 (anatomical fidelity).
  </p>
  <p>
    <strong>Clinical Utility:</strong> Data augmentation with the model's synthetic images improved downstream diagnostic accuracy by 17.5% and 4.2% AUC for pneumonia classification.
  </p>
  <p>
    <strong>Radiologist Validation:</strong> Board-certified radiologists rated the model highly for anatomical plausibility (3.8/5) and pathology expression (3.95/5), outperforming baselines (Roentgen, Cheff, XReal).
  </p>
  <div class="paper-links">
    <a class="btn btn-secondary" href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
    <span style="margin: 0 8px;">|</span>
    <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing">Paper (Preprint)</a>
  </div>
</div>

<div class="paper">
  <div class="paper-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
  <div class="paper-venue">Journal of Building Engineering — Under Review</div>
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
  <div class="paper-links">
    <a href="https://github.com/nubcico/GenBeamJoint" target="_blank" rel="noopener">Code</a>
    <span style="margin: 0 8px;">|</span>
    <a href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing">Paper (Preprint)</a>
  </div>
</div>

## Projects {#projects}

<div class="project">
  <div class="project-title"><a href="https://github.com/Vadim-ATL/BloodMNIST-DDPM">BloodMNIST-DDPM</a></div>
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
