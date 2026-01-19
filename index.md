---
layout: single
author_profile: true
title: "About Me"
sidebar:
  nav: "docs"
header:
  overlay_color: "#333" # Adds a subtle dark header for contrast
---

I am a Researcher at the **HCI Lab**, Nazarbayev University, supervised by **Minho Lee**. 

My work focuses on **Controllable Diffusion Models** for medical image synthesis. I aim to solve data scarcity in healthcare by generating high-fidelity synthetic data conditioned on clinical attributes (text, segmentation masks, and anatomy).

<div class="notice--info">
  <h4><i class="fas fa-flag"></i> Status Update</h4>
  I am actively seeking <strong>PhD positions for Fall 2027</strong> in Europe or South Korea.
</div>

## Research Interests

* **Generative AI:** Latent Diffusion Models, GANs, Semantic Alignment.
* **Medical Imaging:** Chest X-Ray synthesis, Mammography, Histopathology.
* **Clinical AI:** Synthetic data for rare pathologies, Downstream task validation.

---

<a id="publications"></a>
## Selected Publications

**Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis** *Computerized Medical Imaging and Graphics (CMIG), 2025 — Under Review* We propose a latent diffusion model with semantic alignment mechanisms for generating chest X-rays.  
[<i class="fas fa-file-pdf"></i> Paper (Coming Soon)](#){: .btn .btn--primary .btn--small}

**DenseDiff: Virtual Digital Subtraction of Dense Tissue** *In preparation for MICCAI 2026* A conditional diffusion model for computationally removing dense tissue from mammograms to improve lesion visibility.  
[<i class="fas fa-code"></i> Code (Coming Soon)](#){: .btn .btn--warning .btn--small}

---

<a id="open-source"></a>
## Open Source Projects

{% capture bloodmnist_text %}
**BloodMNIST-DDPM** <span style="color:#28a745">⭐ Featured Project</span>  

A Diffusion model for synthesizing realistic blood cell microscopy images. Generates 8 cell types with clinically accurate morphology.

[View on GitHub](https://github.com/Vadim-ATL/BloodMNIST-DDPM){: .btn .btn--success}
{% endcapture %}

{% capture medical_diff_text %}
**Controllable Medical Diffusion** Clean PyTorch implementation of multi-conditional latent diffusion for medical imaging. Supports text and mask conditioning.

[View on GitHub](https://github.com/Vadim-ATL){: .btn .btn--info}
{% endcapture %}

<div class="feature__wrapper">
  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-teaser">
        <img src="https://raw.githubusercontent.com/Vadim-ATL/BloodMNIST-DDPM/main/assets/sample.png" alt="Blood cells" style="width:100%; object-fit: cover;"> </div>
      <div class="archive__item-body">
        {{ bloodmnist_text | markdownify }}
      </div>
    </div>
  </div>
  
  <div class="feature__item">
     <div class="archive__item-body">
        {{ medical_diff_text | markdownify }}
      </div>
  </div>
</div>

---

## Background & Skills

| **Education** | M.Sc. Electrical & Computer Engineering, Nazarbayev University (2024) |
| **Languages** | Russian (Native), English (IELTS 7.0), Czech (B2), Kazakh (B2) |
| **Tech Stack** | PyTorch, Diffusers, MONAI, 2x RTX 5090 Cluster Management |