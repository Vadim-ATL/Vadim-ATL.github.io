---
layout: default
title: Vadim Atlassov - Researcher
---

<div style="display: flex; gap: 30px; align-items: flex-start;">
  <div style="flex-shrink: 0;">
    <img src="assets/personal_photo.png" alt="Vadim Atlassov" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; border: 1px solid #e0e0e0;">
  </div>

  <div style="flex: 1;">
    <h1 style="margin-top: 0;">Vadim Atlassov</h1>
    <p class="bio">
      I am a MSc Researcher at the <strong>HCI Lab</strong>, Nazarbayev University, supervised by
      <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>.
      I develop <strong>Physically-grounded generative AI</strong> for medicine and civil engineering.
    </p>
    <div style="background-color: #f0f8ff; padding: 12px; border-left: 4px solid #0066cc; margin: 15px 0;">
      <strong>Looking for PhD position for Fall 2026</strong>
      My research interests includes:
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

## Research {#research}

I work in **Controllable Generation for 2D/3D Medical Imaging**, specifically developing diffusion models that generate samples conditioned on clinical attributes (Text prompts, Anatomical coordinates, Segmentation masks).

**Current interests:** Latent diffusion models, Multi-modal conditioning, Data generation for rare pathologies.

## Publications & Preprints {#publications}

<div class="paper">
    <div class="paper-title">Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
    <div class="paper-venue">Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review</div>
    <p style="font-size: 14px; margin-top: 8px;">
  <strong>LADiff</strong> introduces a hierarchical latent space where anatomical structures (organs, lesions) are encoded as spatial priors via learned Gaussian attention maps. We train a diffusion model with <strong>dual conditioning</strong>: (1) semantic embeddings from clinical text, and (2) spatial maps decoded from the latent structure. 
  <br><br>
  <strong>Key contributions:</strong> Novel <em>latent-spatial alignment loss</em> that enforces anatomical consistency; validation via FID (↓23% vs. baseline ControlNet) and expert radiologist evaluation (Cohen's κ=0.78 for lesion realism).
  <br><br>
  <strong>Clinical impact:</strong> Generated synthetic data improved downstream pneumonia detection by 4.2% AUC when added to training sets with <500 positive cases.</p>
    <div class="paper-links">
        <a class="btn btn-secondary" href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
        <span style="margin: 0 8px;">|</span>
        <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing">Paper (Preprint)</a>
    </div>
</div>

<div class="paper">
    <div class="paper-title">Controllable Diffusion for RC Beam-Column Joint Failure Diagnosis</div>
    <div class="paper-venue">Journal of Building Engineering (Under Review)</div>
    <p style="font-size: 14px; margin-top: 8px;">
        A geometry-conditioned diffusion framework for synthesizing realistic structural failure images; introduces Edge-guided Spatial Attention (ESA) to improve downstream classification accuracy to 83.0%.
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

## Background

* **M.Sc. Electrical & Computer Engineering**, Nazarbayev University (2024, GPA 3.21/4.0)
* Academic exchange: Brno University of Technology, Czech Republic
* Hands-on experience training large-scale image generative models, diffusion and flow matching models

<p style="margin-top: 20px;">
    <strong>Status:</strong> Seeking PhD positions for <strong>Fall 2026</strong> in generative modeling and medical AI.
</p>
