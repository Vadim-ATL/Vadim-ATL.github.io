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
  Researcher at <strong>HCI Lab, Nazarbayev University</strong>, supervised by <strong><a href="https://scholar.google.com/citations?user=ipi5AVsAAAAJ&hl=ko">Prof. Minho Lee</a></strong>. I build controllable generative models for <strong>medical imaging</strong> and <strong>structural health monitoring</strong>.
</p>
<p style="margin-top: 6px; margin-bottom: 8px; font-size: 14px;">
  <strong>M.Sc. Electrical & Computer Engineering</strong>, Nazarbayev University (2024, GPA 3.21/4.0)
</p>
<div style="background-color:hsl(208, 100.00%, 97.10%); padding: 12px; border-left: 4px solid #0066cc; margin: 15px 0;">
  <strong>Actively seeking PhD positions for Fall 2026</strong> in medical imaging, generative modeling, and conditional synthesis. Open to collaborations on diffusion models for clinical applications.
</div>
    <div class="contact">
        <a href="www.linkedin.com/in/vadim-atlassov">LinkedIn</a>
        <a href="mailto:vadim.atlassov@nu.edu.kz">Email</a>
        <a href="https://github.com/Vadim-ATL">GitHub</a>
        <a href="https://scholar.google.com">Scholar</a>
    </div>
  </div>
</div>

## Research {#research}

<p style="margin-bottom: 6px;"><strong>Focus:</strong> Controllable generative AI for chest X-ray synthesis and RC joint failure analysis.</p>
<p style="margin: 6px 0;"><strong>Method:</strong> Physically grounded conditioning with <strong>ESA</strong> and <strong>SG-MoE-EA</strong>.</p>
<p style="margin-top: 6px;"><strong>Goal:</strong> Improve downstream diagnosis/classification under limited real data.</p>

<div style="background-color: #f8f9fb; padding: 12px; border-left: 4px solid #111827; margin: 15px 0;">
  <strong>Measured impact:</strong> CXR diagnosis <strong>69.0% -> 86.5%</strong> (<strong>+17.5%</strong>) and rebar exposure detection <strong>83.3% -> 95.2%</strong> (<strong>+11.9%</strong>) with synthetic-data augmentation.
</div>

## Publications & Preprints {#publications}

<div class="paper">
    <div class="paper-title">LatAlignCXR: Latent-Aligned Diffusion for Controllable Chest X-ray Synthesis</div>
    <div class="paper-venue">Medical Diffusion / Clinical AI</div>
    <p style="font-size: 14px; margin-top: 8px;">
  A latent-aligned diffusion framework for controllable CXR generation from multimodal priors.
  <br><br>
  <strong>Core metrics:</strong> FID <strong>56.78</strong> | Dice <strong>0.6536</strong> | MS-SSIM <strong>0.3298</strong>.
  <br><br>
  <strong>Data:</strong> MIMIC-CXR, <strong>218,131</strong> frontal-view images (80/10/10 split), <strong>512x512</strong>.
  <br><br>
  <strong>Clinical impact:</strong> Synthetic augmentation improves diagnostic classification from <strong>69.0%</strong> to <strong>86.5%</strong> (<strong>+17.5%</strong> absolute).</p>
    <div class="paper-links">
        <a class="btn btn-secondary" href="https://github.com/nubcico/XrayGen/tree/main" target="_blank" rel="noopener">Code</a>
        <span style="margin: 0 8px;">|</span>
        <a href="https://drive.google.com/file/d/15GdmNFHsGnfKEw_baX7_C4s7PcGfTG69/view?usp=sharing">Paper (Preprint)</a>
    </div>
</div>

<div class="paper">
    <div class="paper-title">RECON: Efficient Vision-Language Reasoning with SG-MoE-EA</div>
    <div class="paper-venue">Vision-Language Modeling / Structural Assessment</div>
    <p style="font-size: 14px; margin-top: 8px;">
        Uses a frozen <strong>DINOv2</strong> visual encoder with a Semantic-Guided Mixture-of-Experts Evidence Adapter (<strong>SG-MoE-EA</strong>) and dual-temperature evidence attention.
        <br><br>
        <strong>Efficiency:</strong> <strong>90.6 GFLOPS</strong>.
        <br><br>
        <strong>NLG/structured metrics:</strong> BLEU-4 <strong>48.86</strong>, CIDEr <strong>0.28</strong>, field accuracy <strong>0.3324</strong>, Macro F1 <strong>0.2010</strong>. Validated by 3 domain experts (10+ years experience).
    </p>
    <div class="paper-links">
        <span>Paper details available on request</span>
    </div>
</div>

<div class="paper">
    <div class="paper-title">RC-Joint-Diffusion: Controllable Synthesis for RC Joint Failure Diagnosis</div>
    <div class="paper-venue">Diffusion for Structural Health Monitoring</div>
    <p style="font-size: 14px; margin-top: 8px;">
        A geometry-aware diffusion pipeline with <strong>Edge-guided Spatial Attention (ESA)</strong> for faithful damage synthesis.
        <br><br>
        <strong>Fidelity:</strong> KID <strong>0.0628</strong> (38% error reduction via ESA), FID <strong>205.21</strong>, SSIM <strong>0.790</strong>.
        <br><br>
        <strong>Downstream gains (baseline -> augmented):</strong> Rebar Exposure <strong>83.3% -> 95.2%</strong> (+11.9%), Spalling <strong>73.8% -> 85.3%</strong> (+11.5%), Flexural Cracking <strong>71.4% -> 84.3%</strong> (+12.9%), Failure-Type <strong>80.6% -> 85.8%</strong>, Concrete Crushing <strong>66.7% -> 74.2%</strong>, Damage Severity <strong>77.4% -> 81.0%</strong>.
    </p>
    <div class="paper-links">
        <a href="https://github.com/nubcico/GenBeamJoint" target="_blank" rel="noopener">Code</a>
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

* Academic exchange: Brno University of Technology, Czech Republic
* Hands-on experience training large-scale image generative models, diffusion and flow matching models

<p style="margin-top: 20px;">
    <strong>Status:</strong> Seeking PhD positions for <strong>Fall 2026</strong> in generative modeling and medical AI.
</p>
