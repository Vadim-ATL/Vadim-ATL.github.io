---
layout: default
title: Vadim Atlassov - Researcher
---

<div style="display: flex; gap: 30px; align-items: flex-start;">
  <div style="flex-shrink: 0;">
    <img src="assets/personal_photo.png" alt="Vadim Atlassov" style="width: 150px; height: 150px; object-fit: cover; border: 1px solid var(--border);">
  </div>

  <div style="flex: 1;">
    <h1 style="margin-top: 0;">Vadim Atlassov</h1>
    <p class="bio">
      MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
      <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
      Research focus: <strong>physically-grounded generative AI</strong> for medicine and civil engineering.
    </p>
    <div style="background-color: var(--panel); padding: 12px; border-left: 4px solid var(--link); margin: 15px 0;">
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
  <p style="font-size: 14px; margin-top: 8px;">
    <strong>Quantitative Results:</strong> On the <a href="https://physionet.org/content/mimic-cxr/2.1.0/" style="color: inherit; text-decoration: none;">MIMIC-CXR</a> dataset, the model achieved a <abbr title="Fréchet Inception Distance">FID</abbr> of 56.78 and a DICE coefficient of lung masks of 0.6536 (anatomical fidelity).
  </p>
  <p style="font-size: 14px;">
    <strong>Clinical Utility:</strong> Data augmentation with the model's synthetic images improved downstream diagnostic accuracy by 17.5% and 4.2% AUC for pneumonia classification.
  </p>
  <p style="font-size: 14px;">
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
  <p style="font-size: 14px; margin-top: 8px;">
    <strong>Quantitative Results:</strong> The model demonstrated high fidelity and structural consistency in generating failure states, achieving a <abbr title="Kernel Inception Distance">KID</abbr> of 0.0628 and an <abbr title="Structural Similarity Index">SSIM</abbr> of 0.790.
  </p>
  <p style="font-size: 14px;">
    <strong>Diagnostic Accuracy Gains:</strong> Synthetic data augmentation significantly enhanced automated diagnostic performance:
  </p>
  <ul style="font-size: 14px; margin-top: 4px; margin-bottom: 12px;">
    <li>Failure-Type Classification: <strong>+5.2%</strong> (to 85.8%)</li>
    <li>Rebar Exposure Detection: <strong>+11.9%</strong> (to 95.2%)</li>
    <li>Flexural Cracking Detection: <strong>+12.9%</strong> (to 84.3%)</li>
    <li>Concrete Spalling Detection: <strong>+11.5%</strong> (to 85.3%)</li>
  </ul>
  <p style="font-size: 14px;">
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
  <p style="font-size: 14px; margin-top: 5px;">
    Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.
  </p>
  <div>
    <span class="tag">Medical Imaging</span>
    <span class="tag">DDPM</span>
    <span class="tag">Hematology</span>
  </div>
</div>
