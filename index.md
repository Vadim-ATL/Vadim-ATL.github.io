---
layout: default
title: Vadim Atlassov - Researcher
---

<style>
  .cv-page {
    font-size: 17px;
    line-height: 1.6;
    color: var(--text, #333);
  }
  
  .cv-page h1 {
    font-size: 2.2em;
    margin: 0 0 8px 0;
    letter-spacing: -0.02em;
    font-weight: 700;
  }
  
  .cv-page h2 {
    font-size: 1.4em;
    margin-top: 40px;
    margin-bottom: 16px;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border, #eee);
    letter-spacing: -0.01em;
  }
  
  .cv-page .profile-header {
    display: flex;
    gap: 32px;
    align-items: flex-start;
    margin-bottom: 24px;
  }
  
  .cv-page .profile-photo {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
    flex-shrink: 0;
  }
  
  .cv-page .profile-info {
    flex: 1;
  }
  
  .cv-page .bio {
    font-size: 1.05em;
    line-height: 1.6;
    margin-bottom: 16px;
  }
  
  .cv-page .phd-status {
    border-left: 3px solid var(--link, #0076df);
    padding-left: 16px;
    margin: 20px 0;
  }
  
  .cv-page .skills-list {
    font-size: 0.95em;
    margin-top: 8px;
    padding-left: 20px;
  }
  
  .cv-page .skills-list li {
    margin-bottom: 6px;
  }
  
  .cv-page .contact {
    margin-top: 16px;
    display: flex;
    gap: 16px;
  }
  
  .cv-page .contact a {
    text-decoration: none;
    font-weight: 500;
  }
  
  .cv-page .contact a:hover {
    text-decoration: underline;
  }
  
  .cv-page .paper {
    margin-bottom: 32px;
    padding-bottom: 16px;
  }
  
  .cv-page .paper-title {
    font-size: 1.15em;
    font-weight: 700;
    margin-bottom: 4px;
  }
  
  .cv-page .paper-venue {
    font-size: 0.95em;
    color: var(--text-muted, #666);
    margin-bottom: 12px;
    font-style: italic;
  }
  
  .cv-page .paper p {
    font-size: 0.95em;
    margin: 0 0 8px 0;
  }
  
  .cv-page .paper ul {
    font-size: 0.95em;
    margin-top: 4px;
    margin-bottom: 12px;
    padding-left: 20px;
  }
  
  .cv-page .paper ul li {
    margin-bottom: 4px;
  }
  
  .cv-page .paper-links {
    margin-top: 12px;
    font-size: 0.9em;
  }
  
  .cv-page .paper-links a {
    text-decoration: none;
    font-weight: 500;
  }
  
  .cv-page .paper-links a:hover {
    text-decoration: underline;
  }
  
  .cv-page .link-separator {
    color: var(--text-muted, #ccc);
    margin: 0 8px;
  }
  
  .cv-page .project {
    margin-bottom: 24px;
  }
  
  .cv-page .project-title {
    font-size: 1.1em;
    font-weight: 700;
    margin-bottom: 6px;
  }
  
  .cv-page .project-title a {
    text-decoration: none;
  }
  
  .cv-page .project-title a:hover {
    text-decoration: underline;
  }
  
  .cv-page .project p {
    font-size: 0.95em;
    margin: 0 0 12px 0;
  }
  
  .cv-page .tag {
    font-size: 0.8em;
    color: var(--text-muted, #666);
    background: var(--panel, #f5f5f5);
    padding: 3px 8px;
    border-radius: 4px;
    margin-right: 6px;
    display: inline-block;
  }
  
  .cv-page ul {
    padding-left: 20px;
  }
  
  .cv-page li {
    margin-bottom: 6px;
  }

  @media (max-width: 600px) {
    .cv-page .profile-header {
      flex-direction: column;
      gap: 16px;
      align-items: center;
      text-align: center;
    }
    .cv-page .contact {
      justify-content: center;
    }
    .cv-page .phd-status {
      text-align: left;
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

  <h2 id="education">Education</h2>

  <ul>
    <li><strong>M.Sc. in Electrical &amp; Computer Engineering</strong>, Nazarbayev University (2024; GPA 3.21/4.0)</li>
    <li><em>Academic Exchange:</em> Brno University of Technology, Czech Republic</li>
    <li>Hands-on experience training large-scale image generative models, including diffusion and flow matching architectures</li>
  </ul>

  <h2 id="publications">Publications &amp; Preprints</h2>

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
      <span class="link-separator">|</span>
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
      <span class="link-separator">|</span>
      <a href="https://drive.google.com/file/d/1GpUAm8dhRuAxDzlUNANdaiV1kBqmBDmX/view?usp=sharing">Paper (Preprint)</a>
    </div>
  </div>

  <h2 id="projects">Projects</h2>

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
