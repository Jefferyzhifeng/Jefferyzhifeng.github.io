---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<!-- ===============================
     Global Styles
     =============================== -->
<style>
/* ---- About Card (two-column) ---- */
.about-card {
  margin-top: 0.6rem;
  border: 1px solid rgba(0,0,0,0.10);
  border-radius: 18px;
  background: #fff;
  box-shadow: 0 10px 28px rgba(0,0,0,0.06);
  padding: 1.6rem 1.7rem;
}

.about-card-header {
  display: flex;
  align-items: center;
  gap: 0.9rem;
  margin-bottom: 1.1rem;
}

.about-card-title {
  font-size: 2.0rem;
  font-weight: 800;
  margin: 0;
  color: #111827;
}

.about-card-line {
  height: 4px;
  width: 70px;
  border-radius: 999px;
  background: rgba(99,102,241,0.55);
  margin-top: 0.2rem;
}

.about-grid {
  display: grid;
  grid-template-columns: 2.2fr 1.1fr;
  gap: 2.2rem;
}

@media (max-width: 860px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 1.2rem;
  }
}

.about-left p {
  margin: 0 0 0.85rem 0;
  line-height: 1.85;
  color: #374151;
  font-size: 1.02rem;
}

.about-left a {
  color: #2563eb;
  text-decoration: none;
}

.about-left a:hover {
  text-decoration: underline;
}

.about-right {
  padding-left: 1.2rem;
  border-left: 2px solid rgba(0,0,0,0.06);
}

@media (max-width: 860px) {
  .about-right {
    border-left: none;
    padding-left: 0;
  }
}

.about-right h3 {
  margin: 0 0 0.65rem 0;
  font-size: 1.1rem;
  font-weight: 800;
  color: #111827;
}

.about-right ul {
  margin: 0;
  padding-left: 1.2rem;
  line-height: 1.9;
  color: #374151;
  font-size: 1.0rem;
}

.about-pill {
  margin-top: 0.9rem;
  display: inline-block;
  padding: 0.28rem 0.55rem;
  border-radius: 999px;
  font-weight: 700;
  font-size: 0.92rem;
  color: #B42318;
  background: rgba(180,35,24,0.08);
  border: 1px solid rgba(180,35,24,0.18);
}

.about-philosophy {
  margin-top: 1.2rem;
  padding: 1.1rem 1.2rem;
  border-radius: 14px;
  border: 1px solid rgba(0,0,0,0.08);
  background: rgba(99,102,241,0.06);
  line-height: 1.75;
  color: #1f2937;
  font-size: 1.0rem;
}

.about-philosophy strong {
  color: #4f46e5;
}

/* ---- Unified paper image size: 300 × 180 ---- */
.paper-box-image {
  width: 300px;
  height: 180px;
  overflow: hidden;
  border-radius: 10px;
  background: #f6f7fb;
  display: flex;
  align-items: center;
  justify-content: center;
}

.paper-box-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  display: block;
}
</style>

<!-- ===============================
     About Me (Card)
     =============================== -->
<span class='anchor' id='about-me'></span>

<div class="about-card">

  <div class="about-card-header">
    <h2 class="about-card-title">About Me</h2>
    <div class="about-card-line"></div>
  </div>

  <div class="about-grid">

    <!-- Left: Narrative -->
    <div class="about-left">
      <p>
        Hi, I am <strong>Zhifeng Wang (汪智峰)</strong>, a third-year master's student at the College of Computer Science and Technology,
        National University of Defense Technology, advised by Prof. <a href="https://kevinkaixu.net/">Kai Xu</a> and Assoc. Prof.
        <a href="https://renjiaoyi.github.io/">Renjiao Yi</a>.
        I founded and currently lead the <a href="https://motong-ai-studio.github.io/">Mt-aistudio</a>, a research group focusing on computer vision and medical AI.
      </p>

      <p>
        My research is centered on <strong>AI for Healthcare</strong>, with a strong emphasis on <strong>generative models</strong> for medical imaging.
        I am particularly interested in diffusion-based generative learning, continuous representations, and structure-aware modeling for medical image reconstruction,
        synthesis, and analysis.
      </p>

      <p style="margin-top:0.9rem;">
        If you are interested in my research or potential collaborations, please feel free to contact me at<br>
        Email: <a href="mailto:zhifengwang@nudt.edu.cn">zhifengwang@nudt.edu.cn</a> /
        <a href="mailto:zhifengwang686@gmail.com">zhifengwang686@gmail.com</a>.
      </p>

      <span class="about-pill">Actively seeking internship / collaboration opportunities in AI for Healthcare (Generative Models).</span>
    </div>

    <!-- Right: Interests -->
    <div class="about-right">
      <h3>I am mainly interested in:</h3>
      <ul>
        <li>AI for Healthcare</li>
        <li>Generative Models (Diffusion & Continuous Representations)</li>
        <li>Structure-aware & Physics-informed Learning</li>
        <li>Medical Image Reconstruction and Synthesis</li>
        <li>Clinically-driven Real-world Applications</li>
      </ul>
    </div>

  </div>

  <!-- Bottom: Philosophy -->
  <div class="about-philosophy">
    I believe that <strong>meaningful technological progress</strong> has the power to reshape how humans understand and interact with the world.
    Through <strong>long-term commitment and sustained effort</strong>, I strive to develop methods that are technically rigorous and impactful in real-world healthcare.
  </div>

</div>

<!-- ===============================
     News
     =============================== -->
# 🔥 News

<div style="
  margin-top:0.6rem;
  border:1px solid rgba(0,0,0,0.10);
  border-radius:14px;
  background:linear-gradient(180deg, rgba(99,102,241,0.06), rgba(99,102,241,0.02));
  box-shadow:0 6px 18px rgba(0,0,0,0.06);
  padding:0.85rem 0.95rem;
">

  <ul style="margin:0; padding-left:1.1rem; line-height:1.65;">
    <li><em>2025.11</em>: 🎉 Awarded the <a href="https://jefferyzhifeng.github.io">National Scholarship</a> (Ranking 3/183).</li>
    <li><em>2025.05</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">TVC Journal</a>.</li>
    <li><em>2025.04</em>: 🎉 Won 1st place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21562#learn_the_details">CVPR2025W</a> “Mobile AI 2025 Real-Time Rendering Realistic Bokeh Challenge”.</li>
    <li><em>2025.04</em>: 🎉 Won 6th place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21564">CVPR2025W</a> “Mobile AI Challenge: RGB Photo Enhancement on Mobile GPUs”.</li>
    <li><em>2025.02</em>: 🎉 One paper is accepted by <a href="https://cvpr.thecvf.com/Conferences/2025/">CVPR 2025</a> (CCF-A).</li>
  </ul>

  <details style="margin-top:0.75rem;">
    <summary style="
      list-style:none;
      cursor:pointer;
      user-select:none;
      display:inline-flex;
      align-items:center;
      gap:0.5rem;
      padding:0.45rem 0.8rem;
      border-radius:999px;
      border:1px solid rgba(99,102,241,0.35);
      background:rgba(99,102,241,0.10);
      color:#1F2A5A;
      font-weight:700;
      transition:all 0.18s ease;
      box-shadow:0 2px 10px rgba(99,102,241,0.12);
    "
    onmouseover="this.style.transform='translateY(-1px)'; this.style.background='rgba(99,102,241,0.16)';"
    onmouseout="this.style.transform='translateY(0px)'; this.style.background='rgba(99,102,241,0.10)';"
    onmousedown="this.style.transform='translateY(0px) scale(0.98)';"
    onmouseup="this.style.transform='translateY(-1px) scale(1)';"
    >
      <span style="
        display:inline-flex; align-items:center; justify-content:center;
        width:22px; height:22px; border-radius:999px;
        background:rgba(99,102,241,0.18);
        font-size:14px; line-height:1;
      ">+</span>
      <span>More</span>
    </summary>

    <style>
      summary::-webkit-details-marker { display: none; }
    </style>

    <div style="
      margin-top:0.65rem;
      border:1px solid rgba(0,0,0,0.10);
      border-radius:12px;
      padding:0.75rem 0.85rem;
      background:rgba(255,255,255,0.70);
      max-height:220px;
      overflow-y:auto;
      box-shadow:inset 0 0 0 1px rgba(255,255,255,0.45);
    ">
      <ul style="margin:0; padding-left:1.1rem; line-height:1.65;">
        <li><em>2024.09</em>: 🎉 One paper is accepted by <a href="https://www.sciencedirect.com/science/article/pii/S2950162824000560">Meta-Radiology</a>.</li>
        <li><em>2024.07</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">FCS Journal</a>. (CCF-T1).</li>
        <li><em>2024.05</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">ICIP 2024</a>.</li>
        <li><em>2022.12</em>: 🎉 Awarded the <a href="https://jefferyzhifeng.github.io">National Scholarship</a> (Top 0.2%).</li>
        <li><em>2022.10</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">PRCV</a>.</li>
        <li><em>2022.06</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">JVCIR Journal</a>.</li>
      </ul>
    </div>
  </details>

</div>

<!-- ===============================
     Publications (unchanged structure, just unified image style)
     =============================== -->
# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint 2025</div><img src='images/2026physconsr.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Phys-ConSR: Learning Fast Differentiable Physically-Informed Continuous Medical Super-Resolution via 2D Gaussian](https://jefferyzhifeng.github.io/)

**Zhifeng Wang**, Renjiao Yi, et al.

[**Project**](https://jefferyzhifeng.github.io/) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Under Review, 2026.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint 2025</div><img src='images/2025nc.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Bio-inspired Visual Synaptic Transistors with Reconfigurable Polarization Perception](https://jefferyzhifeng.github.io/)

Xiong, J., Huang, M., **Wang, Z. (third author)**, et al.

[**Project**](https://jefferyzhifeng.github.io/) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Nature Communications, Under Review, 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint 2025</div><img src='images/2025_BoVAR.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[BoVAR: Learning Adaptive Routing and Hierarchical Attention for Variable-Aperture Bokeh Rendering](https://jefferyzhifeng.github.io/)

Kang Chen, Shijun Yan, **Zhifeng Wang**, Aiwen Jiang.

[**Project**](https://jefferyzhifeng.github.io/) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Under Review, 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2025</div><img src='images/2025cvpr1.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[VasTSD: Learning 3D Vascular Tree-state Space Diffusion Model for AngiographySynthesis](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_VasTSD_Learning_3D_Vascular_Tree-state_Space_Diffusion_Model_for_Angiography_CVPR_2025_paper.html)

**Zhifeng Wang**, Renjiao Yi, Xin Wen, Chenyang Zhu&#9993;, Kai Xu&#9993;

[**Project**](https://jefferyzhifeng.github.io/projects/VasTSD/) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">TVC 2025</div><img src='images/2024tvc.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Angio-Diff: Learning a Self-Supervised Adversarial Diffusion Model for Angiographic Geometry Generation](https://jefferyzhifeng.github.io)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu, Kunlun He&#9993;

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- The Visual Computer, 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Meta-Radiology 2024</div><img src='images/2024meta.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Cardiovascular medical image and analysis based on 3D vision: A comprehensive survey](https://www.sciencedirect.com/science/article/pii/S2950162824000560)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Meta-Radiology 2024.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">PRCV 2022</div><img src='images/2022prcv.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[A Dense Prediction ViT Network for Single Image Bokeh Rendering](https://link.springer.com/chapter/10.1007/978-3-031-18916-6_18)

**Zhifeng Wang**, Aiwen Jiang&#9993;

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- PRCV 2022.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">JVCIR 2022</div><img src='images/2022jvcir.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Self-supervised multi-scale pyramid fusion networks for realistic bokeh effect rendering](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Zhifeng Wang**, Aiwen Jiang&#9993;, Chunjie Zhang, Hanxi Li, Bo Liu

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- JVCIR 2022.
</div>
</div>

<!-- ===============================
     Honors
     =============================== -->
# 🎖 Honors and Awards

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPRW 2025</div><img src='images/2025cvprw_bokeh.png' alt="sym"></div></div>
<div class='paper-box-text' markdown="1">

[Mobile AI Workshop and Challenges 2025](https://codalab.lisn.upsaclay.fr/competitions/21562)

Organized by **CVPR2025**

- MAI 2025 Bokeh Effect Rendering Challenge.  
**Winner**
</div>
</div>
- *2025.11* National Scholarship (3/183), 2025.
- *2022.11* National Scholarship (Top 0.2%), 2022.
- *2022.09* First-class Academic Scholarship, 2022.
- *2021.09* First-class Academic Scholarship, 2021.
- *2020.09* First-class Academic Scholarship, 2020.

<span class='anchor' id='-Services'></span>
# 📖 Services
- Reviewers: PRCV’23/24, CAD/CG, JVCIR, PG.
- Memberships: IEEE Student Member, CSIG Student Member, CAAI Student Member, CVF Member.

# 💻 Internships
- *2025.03 - 2025.08*, AI Research Intern (Medical LLMs) @[Alibaba DAMO Academy](https://damo.alibaba.com/?language=zh), Hangzhou, China.
- *2022.10 - 2023.07*, Algorithm Engineer Intern @ [SpeedBot Robotics Co., Ltd.](https://www.speedbot.com/en/home), Changsha, China.

------

<p align="center">
  <i>I know I am not the perfect one, yet aspire to chase the world and achieve greatness @ Zhifeng Wang --- Latest update: 2025-11-04</i>
</p>
