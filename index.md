---
layout: single
title: "About Me"
author_profile: true
---

<div style="display:flex;align-items:flex-start;gap:30px;margin-bottom:30px;">
  <img src="personal_photo.png" alt="Vadim Atlassov" style="width:180px;height:180px;border-radius:50%;object-fit:cover;flex-shrink:0;">
  <div>
    <h1>Vadim Atlassov</h1>
    <p class="bio">
      Researcher at HCI Lab, Nazarbayev University, supervised by <a href="{{ site.author.scholar }}">Minho Lee</a>. 
      Developing <strong>controllable diffusion models</strong> for medical image synthesis with clinical validation.
    </p>
    <div class="contact">
      <a href="mailto:{{ site.author.email }}">Email</a>
      <a href="https://github.com/{{ site.author.github }}" target="_blank">GitHub</a>
      <a href="{{ site.url }}/assets/CV.pdf" target="_blank">CV (PDF)</a>
      <a href="{{ site.author.scholar }}" target="_blank">Google Scholar</a>
    </div>
  </div>
</div>

<div class="status">Seeking PhD positions for Fall 2027</div>

## Research

My research focuses on **controllable generation for medical imaging**, specifically latent diffusion models conditioned on clinical attributes (text prompts, anatomical coordinates, segmentation masks). This addresses critical data scarcity problems in medical AI.

**Current interests:** Multi-modal conditioning in diffusion models, downstream task validation, semantic alignment in latent space, and synthetic data generation for rare pathologies.

## Publications & Preprints

{% for paper in site.publications %}
<div class="card fade-in">
  <h3>{{ paper.title }}</h3>
  <p><em>{{ paper.venue }}</em></p>
  <p>{{ paper.description }}</p>
  {% if paper.link %}<a href="{{ paper.link }}" class="btn btn-primary">Paper / Code</a>{% endif %}
</div>
{% endfor %}

## Open Source

{% for proj in site.projects %}
<div class="card fade-in">
  <h3>
    <a href="{{ proj.link }}" target="_blank">{{ proj.title }}</a>
    {% if proj.featured %}<span style="color:#28a745">⭐ Featured</span>{% endif %}
  </h3>
  <p>{{ proj.description }}</p>
  {% if proj.tags %}
    {% for tag in proj.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
  {% endif %}
</div>
{% endfor %}

## Background

- **M.Sc. Electrical & Computer Engineering**, Nazarbayev University (2024, GPA 3.21/4.0)  
- Academic exchange: Brno University of Technology, Czech Republic  
- Hands-on experience training large-scale diffusion models (2× RTX 5090 GPUs), medical image research, PyTorch implementations  

**Languages:** Russian (native), English (IELTS 7.0), Czech (B2), Kazakh (B2), German (A1)

## PhD Applications

Seeking PhD positions starting **Fall 2027** in generative modeling, diffusion models, and medical AI. Focus on European and Korean institutions with strong computer vision and medical imaging groups.
