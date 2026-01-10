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
# About me
Hi, I am Zhifeng Wang (汪智峰). I am a third-year master's student at the College of Computer Science and Technology of National University of Defense Technology, under the supervision of Prof. [Kai Xu](https://kevinkaixu.net/) and Assoc.Prof. [Renjiao Yi](https://renjiaoyi.github.io/).

I founded and was in charge of the [Mt-aistudio](https://motong-ai-studio.github.io/), which conducts research in the areas of computer vision.

My research interest: include but are not limited to Low-Level Vision, AI for Healthcare, AIGC, and LLMs. 

If you are interested in my research or have any questions, suggestions, or collaboration ideas, please contact me at Email: [zhifengwang@nudt.edu.cn](mailto:zhifengwang@nudt.edu.cn) and [zhifengwang686@gmail.com](mailto:zhifengwang686@gmail.com).

<span style="color:#B42318; font-weight:700; background:rgba(180,35,24,0.08); padding:0.2rem 0.45rem; border-radius:8px; display:inline-block;">
  I am actively seeking internship or collaboration opportunities in the application of AIGC for Healthcare, particularly in LLMs.
</span>


# 🔥 News

<!-- 主容器（卡片风格） -->
<div style="
  margin-top:0.6rem;
  border:1px solid rgba(0,0,0,0.10);
  border-radius:14px;
  background:linear-gradient(180deg, rgba(99,102,241,0.06), rgba(99,102,241,0.02));
  box-shadow:0 6px 18px rgba(0,0,0,0.06);
  padding:0.85rem 0.95rem;
">

  <!-- 默认展示 5 条 -->
  <ul style="margin:0; padding-left:1.1rem; line-height:1.65;">
    <li><em>2025.11</em>: 🎉 Awarded the <a href="https://jefferyzhifeng.github.io">National Scholarship</a> (Ranking 3/183).</li>
    <li><em>2025.05</em>: 🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">TVC Journal</a>.</li>
    <li><em>2025.04</em>: 🎉 Won 1st place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21562#learn_the_details">CVPR2025W</a> “Mobile AI 2025 Real-Time Rendering Realistic Bokeh Challenge”.</li>
    <li><em>2025.04</em>: 🎉 Won 6th place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21564">CVPR2025W</a> “Mobile AI Challenge: RGB Photo Enhancement on Mobile GPUs”.</li>
    <li><em>2025.02</em>: 🎉 One paper is accepted by <a href="https://cvpr.thecvf.com/Conferences/2025/">CVPR 2025</a> (CCF-A).</li>
    <!-- 如需默认显示 6 条，把下面这条移到上面 list 里即可 -->
    <!-- <li><em>2024.09</em>: 🎉 One paper is accepted by <a href="https://www.sciencedirect.com/science/article/pii/S2950162824000560">Meta-Radiology</a>.</li> -->
  </ul>

  <!-- More：按钮样式 + 可滚动内容 -->
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
      <span style="font-weight:600; opacity:0.75;">(scroll)</span>
    </summary>

    <!-- 隐藏默认三角（不同浏览器兼容：尽力而为） -->
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



# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR‘2025</div><img src='images/2025cvpr1.png'  alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[VasTSD: Learning 3D Vascular Tree-state Space Diffusion Model for AngiographySynthesis](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Zhifeng Wang**, Renjiao Yi, Xin Wen, Chenyang Zhu&#9993;, Kai Xu&#9993;

[**Project**](https://jefferyzhifeng.github.io/projects/VasTSD/) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">TVC‘2025</div><img src='images/2024tvc.png'  alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Angio-Diff: Learning a Self-Supervised Adversarial Diffusion Model for Angiographic Geometry Generation](https://jefferyzhifeng.github.io)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu, Kunlun He&#9993;

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
-  The Visual Computer, 2025.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Meta-Radiology'2024</div><img src='images/2024meta.png'  alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Cardiovascular medical image and analysis based on 3D vision: A comprehensive survey](https://www.sciencedirect.com/science/article/pii/S2950162824000560)

**Zhifeng Wang**, Renjiao Yi&#9993;, Xin Wen, Chenyang Zhu, Kai Xu

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Meta-Radiology 2024.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">PRCV‘2022</div><img src='images/2022prcv.png'  alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[A Dense Prediction ViT Network for Single Image Bokeh Rendering](https://link.springer.com/chapter/10.1007/978-3-031-18916-6_18)

**Zhifeng Wang**, Aiwen Jiang&#9993;

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- The 5th Chinese Conference on Pattern Recognition and Computer Vision(PRCV), 2022.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">JVCIR‘2022</div><img src='images/2022jvcir.png'  alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Self-supervised multi-scale pyramid fusion networks for realistic bokeh effect rendering](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Zhifeng Wang**, Aiwen Jiang&#9993;, Chunjie Zhang, Hanxi Li, Bo Liu

[**Project**](https://jefferyzhifeng.github.io) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Journal of Visual Communication and Image Representation(JVCIR), 2022.
</div>
</div>


# 🎖 Honors and Awards
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPRW‘2025</div><img src='images/2025cvprw_bokeh.png' alt="sym" style="width: auto; height: 150px; object-fit: cover;"></div></div>
  
<div class='paper-box-text' markdown="1">
  
[Mobile AI Workshop and Challenges 2025](https://codalab.lisn.upsaclay.fr/competitions/21562)

Organized by **CVPR2025**

[**Project**](https://codalab.lisn.upsaclay.fr/competitions/21562) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- MAI 2025 Bokeh Effect Rendering Challenge.

**Winner**
</div>
</div>


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
