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

<style>
/* ===============================
   About Card (polished)
   =============================== */
.about-card{
  margin-top:0.7rem;
  border:1px solid rgba(0,0,0,0.08);
  border-radius:18px;
  background:linear-gradient(180deg, rgba(99,102,241,0.06), rgba(255,255,255,1) 48%);
  box-shadow:0 12px 34px rgba(17,24,39,0.08);
  padding:1.7rem 1.75rem;
  position:relative;
  overflow:hidden;
}
.about-card::before{
  content:"";
  position:absolute;
  top:-90px; right:-120px;
  width:260px; height:260px;
  background:radial-gradient(circle, rgba(99,102,241,0.18), rgba(99,102,241,0.00) 70%);
  pointer-events:none;
}
.about-card-header{display:flex; align-items:center; gap:0.95rem; margin-bottom:1.15rem;}
.about-card-title{font-size:2.05rem; font-weight:850; margin:0; color:#0f172a; letter-spacing:-0.02em;}
.about-card-line{
  height:4px; width:76px; border-radius:999px;
  background:linear-gradient(90deg, rgba(99,102,241,0.75), rgba(37,99,235,0.35));
  margin-top:0.25rem;
}
.about-grid{display:grid; grid-template-columns:2.25fr 1.05fr; gap:2.1rem;}
@media (max-width:860px){.about-grid{grid-template-columns:1fr; gap:1.2rem;}}
.about-left p{margin:0 0 0.85rem 0; line-height:1.85; color:#334155; font-size:1.02rem;}
.about-left a{color:#2563eb; text-decoration:none;}
.about-left a:hover{text-decoration:underline;}
.research-scope{
  padding:0.85rem 0.95rem;
  border-radius:14px;
  border:1px solid rgba(0,0,0,0.07);
  background:rgba(255,255,255,0.75);
  box-shadow:inset 0 0 0 1px rgba(255,255,255,0.45);
}
.about-right{
  padding:1.05rem;
  border-radius:16px;
  border:1px solid rgba(0,0,0,0.07);
  background:rgba(255,255,255,0.72);
  box-shadow:inset 0 0 0 1px rgba(255,255,255,0.45);
}
.about-right h3{margin:0 0 0.7rem 0; font-size:1.08rem; font-weight:850; color:#0f172a;}
.about-right ul{margin:0; padding-left:1.15rem; line-height:1.85; color:#334155; font-size:1.0rem;}
.about-right li{margin:0.28rem 0;}
.about-pill{
  margin-top:0.9rem;
  display:inline-flex; align-items:center; gap:0.45rem;
  padding:0.28rem 0.6rem;
  border-radius:999px;
  font-weight:750; font-size:0.92rem;
  color:#B42318;
  background:rgba(180,35,24,0.08);
  border:1px solid rgba(180,35,24,0.18);
}
.about-pill::before{content:"●"; font-size:0.7rem; opacity:0.7;}
.about-philosophy{
  margin-top:1.25rem;
  padding:1.1rem 1.2rem;
  border-radius:14px;
  border:1px solid rgba(99,102,241,0.18);
  background:rgba(99,102,241,0.07);
  line-height:1.75;
  color:#0f172a;
  font-size:1.0rem;
}
.about-philosophy strong{color:#4f46e5;}

/* ===============================
   Section titles
   =============================== */
.section-title{
  margin:1.6rem 0 0.6rem 0;
  font-size:1.55rem;
  font-weight:850;
  color:#0f172a;
}

/* ===============================
   News card
   =============================== */
.news-card{
  margin-top:0.6rem;
  border:1px solid rgba(0,0,0,0.10);
  border-radius:14px;
  background:linear-gradient(180deg, rgba(99,102,241,0.06), rgba(99,102,241,0.02));
  box-shadow:0 6px 18px rgba(0,0,0,0.06);
  padding:0.85rem 0.95rem;
}

/* ===============================
   Paper-box layout (fixed)
   =============================== */
.paper-box{
  display:flex;
  align-items:flex-start;
  gap:1.25rem;
  margin:0.9rem 0 1.4rem 0;
}
.paper-box-image{
  flex:0 0 300px;
  width:300px;
  height:180px;
  border-radius:12px;
  overflow:hidden;
  background:#f6f7fb;
  position:relative;
  border:1px solid rgba(0,0,0,0.08);
  box-shadow:0 8px 22px rgba(17,24,39,0.06);
}
.paper-box-image img{
  width:100%;
  height:100%;
  object-fit:cover;
  object-position:center;
  display:block;
  cursor:zoom-in;
}

/* Badge: smaller + closer top-left */
.paper-badge{
  position:absolute;
  top:8px; left:8px;
  padding:0.18rem 0.45rem;
  font-size:0.78rem;
  font-weight:850;
  color:#ffffff;
  background:#1d4ed8;
  border-radius:9px;
  box-shadow:0 6px 18px rgba(29,78,216,0.22);
}

/* Typography: unify sizes */
.paper-box-text{flex:1 1 auto; min-width:0;}
.paper-title{
  display:inline-block;
  font-size:1.10rem;        /* 统一更协调 */
  font-weight:750;
  color:#1d4ed8;
  text-decoration:underline;
  text-underline-offset:3px;
  line-height:1.35;
}
.paper-authors{
  margin-top:0.45rem;
  font-size:1.00rem;
  font-weight:500;          /* 不整体加粗 */
  color:#334155;
}
.paper-authors strong{font-weight:800;} /* 只加粗 Zhifeng Wang */

.paper-links{margin-top:0.55rem;}
.paper-links a{
  font-size:1.00rem;
  font-weight:750;
  color:#1d4ed8;
  text-decoration:underline;
  text-underline-offset:3px;
}
.paper-meta{
  margin:0.45rem 0 0 1.1rem;
  color:#334155;
  line-height:1.65;
  font-size:0.98rem;
}
.paper-meta li{margin:0.15rem 0;}

@media (max-width:860px){
  .paper-box{flex-direction:column;}
  .paper-box-image{
    width:100%;
    max-width:520px;
    height:auto;
    aspect-ratio:5/3;
  }
}

/* ===============================
   Lightbox
   =============================== */
.lightbox-overlay{
  position:fixed;
  inset:0;
  background:rgba(15,23,42,0.78);
  display:none;
  align-items:center;
  justify-content:center;
  z-index:9999;
  padding:2.0rem 1.2rem;
}
.lightbox-overlay.is-open{display:flex;}
.lightbox-panel{
  position:relative;
  max-width:min(1100px, 92vw);
  max-height:86vh;
  border-radius:14px;
  overflow:hidden;
  box-shadow:0 20px 60px rgba(0,0,0,0.35);
  background:rgba(255,255,255,0.06);
  border:1px solid rgba(255,255,255,0.12);
}
.lightbox-img{
  display:block;
  max-width:min(1100px, 92vw);
  max-height:86vh;
  width:auto;
  height:auto;
}
.lightbox-close{
  position:absolute;
  top:10px;
  right:10px;
  width:38px;
  height:38px;
  border-radius:999px;
  border:1px solid rgba(255,255,255,0.28);
  background:rgba(15,23,42,0.55);
  color:#fff;
  font-size:22px;
  line-height:36px;
  cursor:pointer;
}
.lightbox-caption{
  padding:0.6rem 0.9rem;
  font-size:0.95rem;
  color:rgba(255,255,255,0.92);
  background:rgba(15,23,42,0.45);
  border-top:1px solid rgba(255,255,255,0.10);
}
</style>

<!-- ===============================
     About Me
     =============================== -->
<span class="anchor" id="about-me"></span>
<div class="about-card">
  <div class="about-card-header">
    <h2 class="about-card-title">About Me</h2>
    <div class="about-card-line"></div>
  </div>

  <div class="about-grid">
    <div class="about-left">
      <p>
        Hi, I am <strong>Zhifeng Wang (汪智峰)</strong>, a third-year master's student at the College of Computer Science and Technology,
        National University of Defense Technology, advised by Prof. <a href="https://kevinkaixu.net/">Kai Xu</a> and Assoc. Prof.
        <a href="https://renjiaoyi.github.io/">Renjiao Yi</a>.
        I founded and currently lead the <a href="https://motong-ai-studio.github.io/">Mt-aistudio</a>, a research group focusing on computer vision.
      </p>

      <div class="research-scope">
<p style="
  margin: 0;
  line-height: 1.85;
  font-size: 1.03rem;
  color: #374151;
">
  My research focuses on
  <span style="font-weight:700; color:#1f3a8a;">AI for healthcare</span>,
  with an emphasis on
  <span style="font-weight:700; color:#4f46e5;">structure-aware methods</span>
  for medical image
  <span style="font-weight:600; color:#4338ca;">
    generation, reconstruction, and enhancement
  </span>.
  By integrating
  <span style="font-weight:600; color:#0f766e;">anatomical priors</span>
  and
  <span style="font-weight:600; color:#0f766e;">explicit structural constraints</span>,
  I aim to improve the
  <span style="font-weight:600; color:#7c2d12;">reliability</span>
  and
  <span style="font-weight:600; color:#7c2d12;">clinical relevance</span>
  of learned representations.
  I am particularly interested in approaches that can be translated into
  <span style="font-weight:600; color:#374151; text-decoration:underline;">
    real-world clinical workflows
  </span>.
  In parallel, I explore
  <span style="font-weight:700; color:#5b21b6;">
    physics-informed intelligence
  </span>
  to better align learning-based models with underlying
  <span style="font-weight:600; color:#1e293b;">
    physical and imaging principles
  </span>.
</p>
      </div>
      <p style="margin-top:0.9rem;">
        <strong>Email:</strong>
        <a href="mailto:zhifengwang@nudt.edu.cn">zhifengwang@nudt.edu.cn</a> /
        <a href="mailto:zhifengwang686@gmail.com">zhifengwang686@gmail.com</a>
      </p>
      <span class="about-pill">Actively seeking internship / collaboration opportunities in AI for Healthcare.</span>
    </div>

    <div class="about-right">
      <h3>Current Focus</h3>
      <ul>
        <li>Structure-aware Medical Imaging</li>
        <li>Anatomical Priors & Structural Constraints</li>
        <li>Medical Image Generation & Reconstruction</li>
        <li>Clinically Motivated Visualization & Analysis</li>
        <li>Physics-informed Intelligence</li>
      </ul>
    </div>
  </div>

  <div class="about-philosophy">
    I believe that <strong>technology can meaningfully reshape the world</strong> when it is built with rigor and validated in real settings.
    With <strong>long-term commitment and sustained effort</strong>, I aim to develop methods that translate into tangible impact in healthcare.
  </div>
</div>

<!-- ===============================
     News
     =============================== -->
<h2 class="section-title">🔥 News</h2>
<div class="news-card">
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
      font-weight:800;
      transition:all 0.18s ease;
      box-shadow:0 2px 10px rgba(99,102,241,0.12);
    "
    onmouseover="this.style.transform='translateY(-1px)'; this.style.background='rgba(99,102,241,0.16)';"
    onmouseout="this.style.transform='translateY(0px)'; this.style.background='rgba(99,102,241,0.10)';"
    >
      <span style="
        display:inline-flex; align-items:center; justify-content:center;
        width:22px; height:22px; border-radius:999px;
        background:rgba(99,102,241,0.18);
        font-size:14px; line-height:1;
      ">+</span>
      <span>More</span>
    </summary>

    <style>summary::-webkit-details-marker { display:none; }</style>

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
     Publications
     =============================== -->
<h2 class="section-title">📝 Publications</h2>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Preprint 2025</div>
    <img src="images/2026physconsr.png" alt="PhysConSR teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io/">
      PhysConSR: Learning Fast Differentiable Physically-Informed Continuous Medical Super-Resolution via 2D Gaussian
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Renjiao Yi, et al.</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/">Project</a></div>
    <ul class="paper-meta">
      <li>Under Review, 2026.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Preprint 2025</div>
    <img src="images/2025nc.png" alt="Nature Communications teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io/">
      Bio-inspired Visual Synaptic Transistors with Reconfigurable Polarization Perception
    </a>
    <div class="paper-authors">Xiong, J., Huang, M., <strong>Zhifeng Wang</strong> (third author), et al.</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/">Project</a></div>
    <ul class="paper-meta">
      <li>Nature Communications, Under Review, 2025.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Preprint 2025</div>
    <img src="images/2025_BoVAR.png" alt="BoVAR teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io/">
      BoVAR: Learning Adaptive Routing and Hierarchical Attention for Variable-Aperture Bokeh Rendering
    </a>
    <div class="paper-authors">Kang Chen, Shijun Yan, <strong>Zhifeng Wang</strong>, Aiwen Jiang.</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/">Project</a></div>
    <ul class="paper-meta">
      <li>Under Review, 2025.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">CVPR 2025</div>
    <img src="images/2025cvpr1.png" alt="VasTSD teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://openaccess.thecvf.com/content/CVPR2025/html/Wang_VasTSD_Learning_3D_Vascular_Tree-state_Space_Diffusion_Model_for_Angiography_CVPR_2025_paper.html">
      VasTSD: Learning 3D Vascular Tree-state Space Diffusion Model for Angiography Synthesis
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Renjiao Yi, Xin Wen, Chenyang Zhu✉, Kai Xu✉</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/projects/VasTSD/">Project</a></div>
    <ul class="paper-meta">
      <li>IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2025.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">TVC 2025</div>
    <img src="images/2024tvc.png" alt="Angio-Diff teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io">
      Angio-Diff: Learning a Self-Supervised Adversarial Diffusion Model for Angiographic Geometry Generation
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Renjiao Yi✉, Xin Wen, Chenyang Zhu, Kai Xu, Kunlun He✉</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io">Project</a></div>
    <ul class="paper-meta">
      <li>The Visual Computer, 2025.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Meta-Radiology 2024</div>
    <img src="images/2024meta.png" alt="Survey teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://www.sciencedirect.com/science/article/pii/S2950162824000560">
      Cardiovascular medical image and analysis based on 3D vision: A comprehensive survey
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Renjiao Yi✉, Xin Wen, Chenyang Zhu, Kai Xu</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io">Project</a></div>
    <ul class="paper-meta">
      <li>Meta-Radiology, 2024.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">PRCV 2022</div>
    <img src="images/2022prcv.png" alt="PRCV teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://link.springer.com/chapter/10.1007/978-3-031-18916-6_18">
      A Dense Prediction ViT Network for Single Image Bokeh Rendering
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Aiwen Jiang✉</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io">Project</a></div>
    <ul class="paper-meta">
      <li>PRCV, 2022.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">JVCIR 2022</div>
    <img src="images/2022jvcir.png" alt="JVCIR teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf">
      Self-supervised multi-scale pyramid fusion networks for realistic bokeh effect rendering
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Aiwen Jiang✉, Chunjie Zhang, Hanxi Li, Bo Liu</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io">Project</a></div>
    <ul class="paper-meta">
      <li>Journal of Visual Communication and Image Representation (JVCIR), 2022.</li>
    </ul>
  </div>
</div>

<!-- ===============================
     Honors and Awards (with the missing card restored)
     =============================== -->
<h2 class="section-title">🎖 Honors and Awards</h2>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">CVPRW 2025</div>
    <img src="images/2025cvprw_bokeh.png" alt="MAI 2025 Bokeh Winner Certificate">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://codalab.lisn.upsaclay.fr/competitions/21562">
      Mobile AI Workshop and Challenges 2025
    </a>
    <div class="paper-authors">Organized by <strong>CVPR2025</strong></div>
    <div class="paper-links"><a href="https://codalab.lisn.upsaclay.fr/competitions/21562">Project</a></div>
    <ul class="paper-meta">
      <li>MAI 2025 Bokeh Effect Rendering Challenge.</li>
      <li><strong>Winner</strong>.</li>
    </ul>
  </div>
</div>

<ul style="line-height:1.75; color:#334155; margin-top:0.4rem;">
  <li><em>2025.11</em> China National Scholarship (3/183), 2025.</li>
  <li><em>2022.11</em> China National Scholarship (Top 0.2%), 2022.</li>
  <li><em>2022.09</em> First-class Academic Scholarship, 2022.</li>
  <li><em>2021.09</em> First-class Academic Scholarship, 2021.</li>
  <li><em>2020.09</em> First-class Academic Scholarship, 2020.</li>
</ul>

<!-- ===============================
     Services / Internships
     =============================== -->
<h2 class="section-title">📖 Services</h2>
<ul style="line-height:1.75; color:#334155;">
  <li><strong>Reviewers:</strong> PRCV’23/24, CAD/CG, JVCIR, PG.</li>
  <li><strong>Memberships:</strong> IEEE Student Member, CSIG Student Member, CAAI Student Member, CVF Member.</li>
</ul>

<h2 class="section-title">💻 Internships</h2>
<ul style="line-height:1.75; color:#334155;">
  <li><em>2025.03 – 2025.08</em>, AI Research Intern (Medical LLMs) @ <a href="https://damo.alibaba.com/?language=zh">Alibaba DAMO Academy</a>, Hangzhou, China.</li>
  <li><em>2022.10 – 2023.07</em>, Algorithm Engineer Intern @ <a href="https://www.speedbot.com/en/home">SpeedBot Robotics Co., Ltd.</a>, Changsha, China.</li>
</ul>

<hr>

<p align="center">
  <i>I know I am not the perfect one, yet aspire to chase the world and achieve greatness @ Zhifeng Wang — Latest update: 2025-11-04</i>
</p>

<!-- ===============================
     Lightbox HTML
     =============================== -->
<div class="lightbox-overlay" id="lightboxOverlay" aria-hidden="true">
  <div class="lightbox-panel" role="dialog" aria-modal="true" aria-label="Image preview">
    <button class="lightbox-close" id="lightboxClose" aria-label="Close">×</button>
    <img class="lightbox-img" id="lightboxImg" src="" alt="">
    <div class="lightbox-caption" id="lightboxCaption"></div>
  </div>
</div>

<script>
(function () {
  const overlay = document.getElementById("lightboxOverlay");
  const imgEl = document.getElementById("lightboxImg");
  const capEl = document.getElementById("lightboxCaption");
  const closeBtn = document.getElementById("lightboxClose");

  function openLightbox(src, alt) {
    imgEl.src = src;
    imgEl.alt = alt || "";
    capEl.textContent = alt || "";
    overlay.classList.add("is-open");
    overlay.setAttribute("aria-hidden", "false");
    document.body.style.overflow = "hidden";
  }

  function closeLightbox() {
    overlay.classList.remove("is-open");
    overlay.setAttribute("aria-hidden", "true");
    imgEl.src = "";
    document.body.style.overflow = "";
  }

  document.querySelectorAll(".paper-box-image img").forEach((img) => {
    img.addEventListener("dblclick", (e) => {
      e.preventDefault();
      openLightbox(img.currentSrc || img.src, img.alt || "");
    });
  });

  overlay.addEventListener("click", (e) => {
    if (e.target === overlay) closeLightbox();
  });

  closeBtn.addEventListener("click", closeLightbox);

  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape" && overlay.classList.contains("is-open")) closeLightbox();
  });
})();
</script>
