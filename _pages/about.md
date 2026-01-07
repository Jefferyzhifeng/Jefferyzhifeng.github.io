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

<span class='anchor' id='about-me'></span>

<div class="hero">
  <div class="hero-left">
    <div class="hero-title">
      <h1>Zhifeng Wang <span class="hero-cn">(汪智峰)</span></h1>
      <p class="hero-subtitle">
        3rd-year M.S. @ NUDT · Research Visiting Intern @ Alibaba DAMO Academy
      </p>
    </div>

    <div class="hero-tags">
      <span class="tag">Low-Level Vision</span>
      <span class="tag">AI for Healthcare</span>
      <span class="tag">AIGC</span>
      <span class="tag">LLMs</span>
    </div>

    <div class="hero-actions">
      <a class="btn btn-primary" href="mailto:zhifengwang@nudt.edu.cn">Email</a>
      <a class="btn" href="https://scholar.google.com/citations?user=DhtAFkwAAAAJ" target="_blank" rel="noopener">Google Scholar</a>
      <a class="btn" href="https://github.com/jefferyzhifeng" target="_blank" rel="noopener">GitHub</a>
      <a class="btn" href="/cv/" target="_blank" rel="noopener">CV</a>
    </div>

    <div class="hero-note">
      <span class="pill pill-red">Open to</span>
      <span>Internship / Collaboration in AIGC for Healthcare (esp. LLMs)</span>
    </div>

    <div class="contact-line">
      <span class="muted">Contact:</span>
      <a href="mailto:zhifengwang@nudt.edu.cn">zhifengwang@nudt.edu.cn</a> ·
      <a href="mailto:zhifengwang686@gmail.com">zhifengwang686@gmail.com</a>
    </div>
  </div>

  <div class="hero-right">
    <!-- 如果暂时没有头像，先把这行注释掉或把 src 改成你真实头像路径 -->
    <img class="avatar" src="/images/avatar.jpg" alt="Zhifeng Wang">
    <div class="hero-meta">
      <div><span class="k">Advisor</span> Prof. <a href="https://kevinkaixu.net/" target="_blank" rel="noopener">Kai Xu</a></div>
      <div><span class="k">Co-advisor</span> Assoc. Prof. <a href="https://renjiaoyi.github.io/" target="_blank" rel="noopener">Renjiao Yi</a></div>
      <div><span class="k">Lab</span> College of CS, NUDT</div>
      <div><span class="k">Now</span> Alibaba DAMO Academy</div>
    </div>
  </div>
</div>

---

## About

- I am a third-year M.S. student at the College of Computer Science and Technology, National University of Defense Technology (NUDT).
- I am supervised by Prof. [Kai Xu](https://kevinkaixu.net/) and Assoc. Prof. [Renjiao Yi](https://renjiaoyi.github.io/).
- I am currently a research visiting intern at Alibaba DAMO Academy.
- I received my Bachelor’s degree from Jiangxi Normal University (2019–2023) and worked closely with Dr. [Aiwen Jiang](https://jsjxy.jxnu.edu.cn/2014/0423/c3381a106160/page.htm).
- I founded and led [Mt-aistudio](https://motong-ai-studio.github.io/) for computer vision research.

---

# 🔥 News

<details open>
<summary><span class="muted">Recent updates (click to expand/collapse)</span></summary>

- **2025.11** · National Scholarship (Rank 3/183).
- **2025.05** · One paper is accepted by TVC Journal.
- **2025.04** · 1st place, CVPR 2025 Workshop: Mobile AI Real-Time Rendering Realistic Bokeh Challenge.
- **2025.04** · 6th place, CVPR 2025 Workshop: Mobile AI Challenge: RGB Photo Enhancement on Mobile GPUs.
- **2025.02** · One paper is accepted by CVPR 2025 (CCF-A).
- **2024.09** · One paper is accepted by Meta-Radiology.

</details>

---

# 📝 Publications

<div class="section-hint muted">Selected publications. Full list on Google Scholar.</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">CVPR 2025</div>
      <img src='images/2025cvpr1.png' alt="VasTSD" width="100%">
    </div>
  </div>

  <div class='paper-box-text' markdown="1">
[VasTSD: Learning 3D Vascular Tree-state Space Diffusion Model for Angiography Synthesis](https://openaccess.thecvf.com/)

**Zhifeng Wang**, Renjiao Yi, Xin Wen, Chenyang Zhu&#9993;, Kai Xu&#9993;

<div class="paper-links">
  <a class="btn btn-sm btn-primary" href="https://jefferyzhifeng.github.io/projects/VasTSD/" target="_blank" rel="noopener">Project</a>
  <a class="btn btn-sm" href="https://openaccess.thecvf.com/" target="_blank" rel="noopener">Paper</a>
  <a class="btn btn-sm" href="https://github.com/" target="_blank" rel="noopener">Code</a>
  <span class="cite"><strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong></span>
</div>

- IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2025.
  </div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">TVC 2025</div>
      <img src='images/2024tvc.png' alt="Angio-Diff" width="100%">
    </div>
  </div>

  <div class='paper-box-text' markdown="1">
[Angio-Diff: Learning a Self-Supervised Adversarial Diffusion Model for Angiographic Geometry Generation](https://jefferyzhifeng.github.io)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu, Kunlun He&#9993;

<div class="paper-links">
  <a class="btn btn-sm btn-primary" href="https://jefferyzhifeng.github.io" target="_blank" rel="noopener">Project</a>
  <a class="btn btn-sm" href="https://jefferyzhifeng.github.io" target="_blank" rel="noopener">Paper</a>
  <a class="btn btn-sm" href="https://github.com/" target="_blank" rel="noopener">Code</a>
  <span class="cite"><strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong></span>
</div>

- The Visual Computer, 2025.
  </div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">Meta-Radiology 2024</div>
      <img src='images/2024meta.png' alt="Survey" width="100%">
    </div>
  </div>

  <div class='paper-box-text' markdown="1">
[Cardiovascular medical image and analysis based on 3D vision: A comprehensive survey](https://www.sciencedirect.com/science/article/pii/S2950162824000560)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu

<div class="paper-links">
  <a class="btn btn-sm btn-primary" href="https://jefferyzhifeng.github.io" target="_blank" rel="noopener">Project</a>
  <a class="btn btn-sm" href="https://www.sciencedirect.com/science/article/pii/S2950162824000560" target="_blank" rel="noopener">Paper</a>
  <a class="btn btn-sm" href="https://github.com/" target="_blank" rel="noopener">Code</a>
  <span class="cite"><strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong></span>
</div>

- Meta-Radiology, 2024.
  </div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">PRCV 2022</div>
      <img src='images/2022prcv.png' alt="Bokeh ViT" width="100%">
    </div>
  </div>

  <div class='paper-box-text' markdown="1">
[A Dense Prediction ViT Network for Single Image Bokeh Rendering](https://link.springer.com/chapter/10.1007/978-3-031-18916-6_18)

**Zhifeng Wang**, Aiwen Jiang&#9993;

<div class="paper-links">
  <a class="btn btn-sm btn-primary" href="https://jefferyzhifeng.github.io" target="_blank" rel="noopener">Project</a>
  <a class="btn btn-sm" href="https://link.springer.com/chapter/10.1007/978-3-031-18916-6_18" target="_blank" rel="noopener">Paper</a>
  <a class="btn btn-sm" href="https://github.com/" target="_blank" rel="noopener">Code</a>
  <span class="cite"><strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong></span>
</div>

- PRCV, 2022.
  </div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">JVCIR 2022</div>
      <img src='images/2022jvcir.png' alt="Pyramid fusion" width="100%">
    </div>
  </div>

  <div class='paper-box-text' markdown="1">
[Self-supervised multi-scale pyramid fusion networks for realistic bokeh effect rendering](https://openaccess.thecvf.com/)

**Zhifeng Wang**, Aiwen Jiang&#9993;, Chunjie Zhang, Hanxi Li, Bo Liu

<div class="paper-links">
  <a class="btn btn-sm btn-primary" href="https://jefferyzhifeng.github.io" target="_blank" rel="noopener">Project</a>
  <a class="btn btn-sm" href="https://openaccess.thecvf.com/" target="_blank" rel="noopener">Paper</a>
  <a class="btn btn-sm" href="https://github.com/" target="_blank" rel="noopener">Code</a>
  <span class="cite"><strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong></span>
</div>

- Journal of Visual Communication and Image Representation (JVCIR), 2022.
  </div>
</div>

---

# 🎖 Honors and Awards

<div class="grid-2">
  <div class="card">
    <h3>Highlights</h3>
    <ul>
      <li><b>National Scholarship</b> (2025, Rank 3/183)</li>
      <li><b>National Scholarship</b> (2022, Top 0.2%)</li>
      <li><b>CVPR 2025 Workshop</b> · Mobile AI Bokeh Challenge · Winner</li>
      <li><b>CVPR 2025 Workshop</b> · Mobile AI RGB Enhancement · 6th Place</li>
    </ul>
  </div>

  <div class="card">
    <h3>Scholarships</h3>
    <ul class="compact">
      <li>2022 · First-class Academic Scholarship</li>
      <li>2021 · First-class Academic Scholarship</li>
      <li>2020 · First-class Academic Scholarship</li>
    </ul>
  </div>
</div>

---

<span class='anchor' id='-Services'></span>

# 📖 Services

<div class="grid-2">
  <div class="card">
    <h3>Reviewing</h3>
    <div class="chips">
      <span class="chip">PRCV 2023/2024</span>
      <span class="chip">CAD/CG</span>
      <span class="chip">JVCIR</span>
      <span class="chip">PG</span>
    </div>
  </div>

  <div class="card">
    <h3>Memberships</h3>
    <div class="chips">
      <span class="chip">IEEE Student Member</span>
      <span class="chip">CSIG Student Member</span>
      <span class="chip">CAAI Student Member</span>
      <span class="chip">CVF Member</span>
    </div>
  </div>
</div>

---

# 💻 Internships

<div class="timeline">
  <div class="t-item">
    <div class="t-time">2025.03 – Now</div>
    <div class="t-body">
      <b>AI Research Intern (Medical LLMs)</b> ·
      <a href="https://damo.alibaba.com/?language=zh" target="_blank" rel="noopener">Alibaba DAMO Academy</a> ·
      Hangzhou, China
    </div>
  </div>

  <div class="t-item">
    <div class="t-time">2022.10 – 2023.07</div>
    <div class="t-body">
      <b>Algorithm Engineer Intern</b> ·
      <a href="https://www.speedbot.com/en/home" target="_blank" rel="noopener">SpeedBot Robotics Co., Ltd.</a> ·
      Changsha, China
    </div>
  </div>
</div>

---

<p class="footer-quote">
  <i>I know I am not the perfect one, yet aspire to chase the world and achieve greatness @ Zhifeng Wang --- Latest update: 2025-11-04</i>
</p>
