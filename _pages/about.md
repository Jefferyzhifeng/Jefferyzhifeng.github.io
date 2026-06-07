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
   About Card (polished & enhanced)
   =============================== */
/* ===============================
   Current Focus Animation
   =============================== */
.focus-animation-wrapper {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
}

.orbit-system {
  position: relative;
  width: 50px;
  height: 50px;
}

/* 中心发光点（代表AI/核心节点） */
.orbit-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 14px;
  height: 14px;
  background: #4f46e5;
  border-radius: 50%;
  box-shadow: 0 0 12px rgba(79, 70, 229, 0.6);
  animation: pulse-center 2s infinite ease-in-out alternate;
}

/* 轨道 */
.orbit-path {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 1px dashed rgba(99, 102, 241, 0.4);
  border-radius: 50%;
  animation: spin-orbit 4s linear infinite;
}

/* 环绕的卫星点（代表物理规律/数据输入） */
.orbit-satellite {
  position: absolute;
  top: -4px;
  left: 50%;
  transform: translateX(-50%);
  width: 8px;
  height: 8px;
  background: #1d4ed8;
  border-radius: 50%;
  box-shadow: 0 0 8px rgba(29, 78, 216, 0.6);
}

/* 动画关键帧 */
@keyframes pulse-center {
  0% { transform: translate(-50%, -50%) scale(0.9); opacity: 0.8; }
  100% { transform: translate(-50%, -50%) scale(1.2); opacity: 1; }
}

@keyframes spin-orbit {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

/* Scroll animations */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.fade-in-up {
  animation: fadeInUp 0.6s ease forwards;
}

.section-title {
  animation: fadeInUp 0.5s ease forwards;
  background: linear-gradient(90deg, #4f46e5, #1d4ed8, #06b6d4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
/* keep leading emoji rendered in native color (not clipped by gradient) */
.section-emoji {
  -webkit-text-fill-color: initial !important;
  background: none !important;
  -webkit-background-clip: initial !important;
          background-clip: initial !important;
  margin-right: 0.4rem;
  font-size: 0.95em;
  vertical-align: -0.05em;
}

/* 入场动画已移除：内容首屏立即可见，避免一打开网页出现空白渐入的等待感 */

  
.about-card{
  margin-top:0.7rem;
  border:1px solid rgba(99,102,241,0.12);
  border-radius:20px;
  background:linear-gradient(170deg, rgba(99,102,241,0.07) 0%, rgba(255,255,255,1) 40%);
  box-shadow:0 14px 40px rgba(17,24,39,0.09), 0 0 0 1px rgba(99,102,241,0.03);
  padding:2rem 2.1rem;
  position:relative;
  overflow:hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.about-card:hover {
  transform: translateY(-4px);
  box-shadow:0 20px 50px rgba(17,24,39,0.15), 0 0 0 1px rgba(99,102,241,0.1);
}
.about-card::before{
  content:"";
  position:absolute;
  top:-80px; right:-100px;
  width:300px; height:300px;
  background:radial-gradient(circle, rgba(99,102,241,0.15), rgba(99,102,241,0.00) 70%);
  pointer-events:none;
}
.about-card::after{
  content:"";
  position:absolute;
  bottom:-60px; left:-60px;
  width:200px; height:200px;
  background:radial-gradient(circle, rgba(37,99,235,0.10), rgba(37,99,235,0.00) 70%);
  pointer-events:none;
}
.about-card-header{display:flex; align-items:center; gap:1rem; margin-bottom:1.3rem;}
.about-card-title{
  font-size:2.1rem; font-weight:850; margin:0; color:#0f172a; letter-spacing:-0.02em;
  position:relative;
}
.about-card-line{
  height:4px; width:80px; border-radius:999px;
  background:linear-gradient(90deg, #6366f1, #2563eb, #06b6d4);
  margin-top:0.25rem;
}
.about-grid{display:grid; grid-template-columns:1fr; gap:1.5rem;}
.about-left p{margin:0 0 0.85rem 0; line-height:1.85; color:#334155; font-size:1.02rem;}
.about-left a{color:#2563eb; text-decoration:none; transition:color 0.2s;}
.about-left a:hover{color:#1d4ed8; text-decoration:underline;}
.research-scope{
  padding:1.05rem 1.15rem;
  border-radius:14px;
  border:1px solid rgba(99,102,241,0.12);
  background:linear-gradient(135deg, rgba(255,255,255,0.85), rgba(238,242,255,0.9));
  box-shadow:0 2px 8px rgba(99,102,241,0.06);
}
.focus-section{
  margin-top:0;
  padding:1rem 1.1rem;
  border-radius:14px;
  border:1px solid rgba(99,102,241,0.12);
  background:linear-gradient(145deg, rgba(238,242,255,0.6), rgba(255,255,255,0.9));
  box-shadow:0 2px 12px rgba(99,102,241,0.05);
}
.focus-header{
  display:flex; align-items:center; gap:0.5rem;
  margin:0 0 0.7rem 0;
  font-size:1.02rem; font-weight:850; color:#0f172a;
}
.focus-header svg{flex-shrink:0;}
.focus-chips{
  display:flex;
  flex-direction:column;
  gap:0.38rem;
}
.focus-chip{
  position:relative;
  display:flex; align-items:center; gap:0.5rem;
  padding:0.4rem 0.7rem 0.4rem 0.6rem;
  border-radius:10px;
  font-weight:700; font-size:0.85rem;
  letter-spacing:0.01em;
  transition: transform 0.25s ease, box-shadow 0.25s ease, background 0.25s ease, border-color 0.25s ease;
  cursor:default;
  border:1px solid;
  overflow:hidden;
}
.focus-chip::before{
  content:"";
  position:absolute;
  left:0; top:14%; bottom:14%;
  width:3px;
  border-radius:2px;
  background:currentColor;
  opacity:0.65;
  transition: opacity 0.25s ease, transform 0.25s ease;
}
.focus-chip .chip-icon{
  font-size:0.95rem;
  line-height:1;
  display:inline-flex;
  align-items:center;
  justify-content:center;
  width:20px; height:20px;
  border-radius:6px;
  background:rgba(255,255,255,0.55);
  border:1px solid rgba(0,0,0,0.04);
  transition: transform 0.35s cubic-bezier(0.4, 0.0, 0.2, 1);
}
.focus-chip:hover{
  transform:translateX(4px);
  box-shadow:0 6px 16px rgba(0,0,0,0.10);
}
.focus-chip:hover::before{ opacity:1; transform:scaleY(1.08); }
.focus-chip:hover .chip-icon{
  transform:scale(1.18) rotate(-8deg);
}
.focus-chip::after{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(120deg, transparent, rgba(255,255,255,0.55), transparent);
  transform:translateX(-110%);
  transition: transform 0.7s ease;
  pointer-events:none;
}
.focus-chip:hover::after{ transform:translateX(110%); }
.chip-indigo{color:#4338ca; background:rgba(99,102,241,0.10); border-color:rgba(99,102,241,0.22);}
.chip-indigo:hover{background:rgba(99,102,241,0.18);}
.chip-blue{color:#1d4ed8; background:rgba(37,99,235,0.10); border-color:rgba(37,99,235,0.22);}
.chip-blue:hover{background:rgba(37,99,235,0.18);}
.chip-violet{color:#5b21b6; background:rgba(139,92,246,0.10); border-color:rgba(139,92,246,0.22);}
.chip-violet:hover{background:rgba(139,92,246,0.18);}
.chip-teal{color:#0f766e; background:rgba(20,184,166,0.10); border-color:rgba(20,184,166,0.22);}
.chip-teal:hover{background:rgba(20,184,166,0.18);}
.chip-rose{color:#9f1239; background:rgba(244,63,94,0.10); border-color:rgba(244,63,94,0.22);}
.chip-rose:hover{background:rgba(244,63,94,0.18);}
.chip-emerald{color:#047857; background:rgba(16,185,129,0.10); border-color:rgba(16,185,129,0.22);}
.chip-emerald:hover{background:rgba(16,185,129,0.18);}
.about-pill{
  margin-top:1rem;
  display:inline-flex; align-items:center; gap:0.5rem;
  padding:0.38rem 0.75rem;
  border-radius:999px;
  font-weight:750; font-size:0.92rem;
  color:#B42318;
  background:rgba(180,35,24,0.07);
  border:1px solid rgba(180,35,24,0.16);
  transition:all 0.2s ease;
}
.about-pill:hover{background:rgba(180,35,24,0.12); transform:translateY(-1px);}
.about-pill::before{
  content:"";
  display:inline-block;
  width:7px; height:7px;
  border-radius:50%;
  background:#ef4444;
  box-shadow:0 0 6px rgba(239,68,68,0.5);
  animation:pulse-dot 2s infinite ease-in-out;
}
@keyframes pulse-dot{
  0%, 100%{opacity:1; transform:scale(1);}
  50%{opacity:0.6; transform:scale(0.85);}
}
.about-philosophy{
  margin-top:1rem;
  padding:0.85rem 1.15rem 0.85rem 1.85rem;
  border-radius:12px;
  border:1px solid rgba(99,102,241,0.15);
  background:linear-gradient(135deg, rgba(99,102,241,0.06), rgba(139,92,246,0.06));
  line-height:1.6;
  color:#0f172a;
  font-size:0.92rem;
  font-style:italic;
  position:relative;
}
.about-philosophy::before{
  content:"\201C";
  position:absolute;
  top:-2px; left:6px;
  font-size:2.2rem;
  color:rgba(99,102,241,0.18);
  font-family:Georgia, serif;
  line-height:1;
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
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.paper-box:hover .paper-box-image {
  transform: scale(1.02);
  box-shadow:0 12px 30px rgba(17,24,39,0.12);
}

.paper-box-image img{
  width:100%;
  height:100%;
  object-fit:cover;
  object-position:center;
  display:block;
  cursor:zoom-in;
  transition: transform 0.3s ease;
}

.paper-box-image img:hover {
  transform: scale(1.05);
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

/* ===============================
   About Me — beautification additions
   =============================== */
.about-card-header{
  display:flex;
  align-items:flex-start;
  justify-content:space-between;
  flex-wrap:wrap;
  gap:1rem;
  margin-bottom:0.85rem;
}
.about-card-title-wrap{display:flex; flex-direction:column;}

/* legacy — no longer used after layout flatten */
.about-grid{display:block;}

/* full-width text strip + 2-col card row */
.about-card{ padding:1.55rem 1.7rem !important; }
.about-card .about-intro{ margin:0.2rem 0 0.85rem 0 !important; font-size:1rem !important; line-height:1.7 !important; }
.about-card .research-scope{ padding:0.85rem 1.05rem !important; }
.about-card .research-scope p{ font-size:0.97rem !important; line-height:1.7 !important; }

.about-pill{ margin:0.85rem 0 0.4rem 0; }
.about-pill--bottom{
  display:flex;
  margin:1.1rem 0 0.2rem 0;
  width:fit-content;
}

/* Header right cluster: compact mail buttons + status badge */
.about-header-meta{
  display:flex;
  align-items:center;
  gap:0.55rem;
  flex-wrap:wrap;
  justify-content:flex-end;
}
.about-contact-row--compact{
  display:inline-flex;
  gap:0.4rem;
  margin:0;
}
.about-contact-row--compact .contact-btn{
  padding:0.3rem 0.65rem;
  font-size:0.78rem;
  font-weight:750;
  border-radius:8px;
  box-shadow:0 2px 6px rgba(99,102,241,0.06);
}
.about-contact-row--compact .contact-btn svg{
  width:13px; height:13px;
}

.about-cards-row{
  display:grid;
  grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
  gap:1rem;
  margin-top:1.1rem;
  align-items:stretch;
}
.about-cards-row > .focus-section,
.about-cards-row > .about-highlights{
  display:flex;
  flex-direction:column;
  height:100%;
}
.about-cards-row > .focus-section .focus-chips,
.about-cards-row > .about-highlights .highlights-list{
  flex:1;
}
@media (max-width: 860px){
  .about-cards-row{grid-template-columns:1fr;}
  .about-action-row{justify-content:flex-start;}
}

.about-status-badge{
  display:inline-flex;
  align-items:center;
  gap:0.5rem;
  padding:0.4rem 0.9rem;
  border-radius:999px;
  font-size:0.85rem;
  font-weight:750;
  color:#047857;
  background:rgba(16,185,129,0.10);
  border:1px solid rgba(16,185,129,0.30);
  white-space:nowrap;
}
.status-dot{
  width:9px; height:9px;
  border-radius:50%;
  background:#10b981;
  box-shadow:0 0 0 0 rgba(16,185,129,0.55);
  animation:pulse-status 2s infinite;
  flex-shrink:0;
}
@keyframes pulse-status{
  0%{box-shadow:0 0 0 0 rgba(16,185,129,0.55);}
  70%{box-shadow:0 0 0 9px rgba(16,185,129,0);}
  100%{box-shadow:0 0 0 0 rgba(16,185,129,0);}
}

.about-intro{
  font-size:1.05rem !important;
  line-height:1.85 !important;
}

.about-meta-chips{
  display:flex;
  flex-wrap:wrap;
  gap:0.5rem;
  margin:0.4rem 0 1rem 0;
}
.meta-chip{
  display:inline-flex;
  align-items:center;
  gap:0.4rem;
  padding:0.32rem 0.72rem;
  border-radius:999px;
  font-size:0.83rem;
  font-weight:650;
  color:#334155;
  background:rgba(99,102,241,0.07);
  border:1px solid rgba(99,102,241,0.20);
  transition:all 0.2s ease;
}
.meta-chip:hover{
  transform:translateY(-1px);
  background:rgba(99,102,241,0.12);
  border-color:rgba(99,102,241,0.35);
}
.meta-chip svg{width:14px; height:14px; color:#4f46e5; flex-shrink:0;}

.about-contact-row{
  display:flex;
  flex-wrap:wrap;
  gap:0.5rem;
  margin:0.85rem 0;
}
.contact-btn{
  display:inline-flex;
  align-items:center;
  gap:0.45rem;
  padding:0.45rem 0.85rem;
  border-radius:10px;
  border:1px solid rgba(99,102,241,0.22);
  background:linear-gradient(135deg, rgba(99,102,241,0.08), rgba(255,255,255,0.95));
  color:#1d4ed8 !important;
  font-weight:700;
  font-size:0.88rem;
  text-decoration:none !important;
  transition:transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease, background 0.22s ease;
  box-shadow:0 2px 8px rgba(99,102,241,0.08);
}
.contact-btn:hover{
  transform:translateY(-2px);
  box-shadow:0 8px 22px rgba(99,102,241,0.22);
  border-color:rgba(99,102,241,0.45);
  background:linear-gradient(135deg, rgba(99,102,241,0.16), rgba(255,255,255,1));
}
.contact-btn svg{width:15px; height:15px; flex-shrink:0;}

/* ===============================
   News — scrollable container
   =============================== */
.news-scroll{
  max-height:300px;
  overflow-y:auto;
  scroll-behavior:smooth;
  padding-right:0.55rem;
  -webkit-overflow-scrolling:touch;
}
.news-list{
  margin:0;
  padding-left:1.1rem;
  line-height:1.75;
}
.news-list li{
  margin:0.25rem 0;
  padding-left:0.15rem;
}
.news-list li em{
  display:inline-block;
  min-width:4.2em;
  color:#6b7280;
  font-style:normal;
  font-weight:700;
  margin-right:0.45rem;
  letter-spacing:0.01em;
}
.news-scroll{
  scrollbar-width:thin;
  scrollbar-color: rgba(99,102,241,0.45) rgba(99,102,241,0.05);
}
.news-scroll::-webkit-scrollbar{width:8px;}
.news-scroll::-webkit-scrollbar-track{
  background:rgba(99,102,241,0.05);
  border-radius:8px;
}
.news-scroll::-webkit-scrollbar-thumb{
  background:linear-gradient(180deg, rgba(99,102,241,0.45), rgba(99,102,241,0.30));
  border-radius:8px;
}
.news-scroll::-webkit-scrollbar-thumb:hover{
  background:linear-gradient(180deg, rgba(99,102,241,0.65), rgba(99,102,241,0.50));
}
.news-fade{
  position:relative;
}
.news-fade::after{
  content:"";
  position:absolute;
  left:0; right:0; bottom:0;
  height:32px;
  background:linear-gradient(180deg, rgba(255,255,255,0), rgba(255,255,255,0.92));
  border-radius:0 0 14px 14px;
  pointer-events:none;
}

/* ===============================
   About-right column (focus + highlights stacked)
   =============================== */
.about-right{
  display:flex;
  flex-direction:column;
  gap:1.2rem;
  position:relative;
}

/* ===============================
   Highlights card
   =============================== */
.about-highlights{
  position:relative;
  padding:1rem 1.1rem;
  border-radius:14px;
  border:1px solid rgba(99,102,241,0.14);
  background:
    radial-gradient(at top right, rgba(139,92,246,0.10), transparent 60%),
    linear-gradient(145deg, rgba(255,255,255,0.95), rgba(238,242,255,0.7));
  box-shadow:0 4px 16px rgba(99,102,241,0.07);
  overflow:hidden;
}
.about-highlights::before{
  content:"";
  position:absolute;
  inset:-1px;
  border-radius:16px;
  padding:1px;
  background:linear-gradient(135deg, rgba(99,102,241,0.45), rgba(6,182,212,0.10) 40%, transparent 75%);
  -webkit-mask: linear-gradient(#000 0 0) content-box, linear-gradient(#000 0 0);
          mask: linear-gradient(#000 0 0) content-box, linear-gradient(#000 0 0);
  -webkit-mask-composite: xor;
          mask-composite: exclude;
  pointer-events:none;
  opacity:0.6;
}
.highlights-header{
  position:relative;
  display:flex; align-items:center; gap:0.5rem;
  margin:0 0 0.7rem 0;
  font-size:1.02rem;
  font-weight:850;
  color:#0f172a;
}
.highlights-header > svg{ color:#f59e0b; width:20px; height:20px; flex-shrink:0; }
.highlights-orbit{
  position:relative;
  width:22px; height:22px;
  margin-left:auto;
  display:inline-block;
}
.highlights-orbit .orbit-ring{
  position:absolute; inset:0;
  border:1px dashed rgba(99,102,241,0.45);
  border-radius:50%;
  animation:spin-orbit 6s linear infinite;
}
.highlights-orbit .orbit-dot{
  position:absolute;
  top:-3px; left:50%;
  width:6px; height:6px;
  background:#4f46e5;
  border-radius:50%;
  transform:translateX(-50%);
  box-shadow:0 0 8px rgba(79,70,229,0.6);
  animation:spin-orbit 6s linear infinite;
  transform-origin:50% 14px;
}

.highlights-list{
  margin:0;
  padding:0;
  list-style:none;
  display:grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap:0.55rem;
  position:relative;
}
.hl-item{
  display:flex;
  align-items:center;
  gap:0.55rem;
  padding:0.5rem 0.65rem;
  border-radius:11px;
  background:linear-gradient(135deg, rgba(99,102,241,0.07), rgba(255,255,255,0.85));
  border:1px solid rgba(99,102,241,0.12);
  transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
  min-width:0;
}
.hl-item:hover{
  transform:translateY(-2px);
  border-color:rgba(99,102,241,0.32);
  box-shadow:0 6px 18px rgba(99,102,241,0.18);
}
.hl-icon{
  flex-shrink:0;
  width:30px; height:30px;
  display:flex; align-items:center; justify-content:center;
  border-radius:9px;
  font-size:0.95rem;
  background:linear-gradient(135deg, rgba(99,102,241,0.20), rgba(37,99,235,0.10));
  border:1px solid rgba(99,102,241,0.20);
  box-shadow:0 2px 8px rgba(99,102,241,0.10);
}
.hl-content{ flex:1; min-width:0; }
.hl-number{
  font-size:0.84rem;
  font-weight:800;
  color:#1d4ed8;
  line-height:1.25;
  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;
}
.hl-number .hl-unit{font-weight:700; color:#475569; font-size:0.78rem;}
.hl-label{
  font-size:0.7rem;
  color:#64748b;
  margin-top:0.1rem;
  letter-spacing:0.01em;
  line-height:1.3;
}
@media (max-width: 1080px){
  .highlights-list{grid-template-columns:1fr;}
}

/* ===============================
   Stagger entrance for new components
   =============================== */
/* contact-btn 入场动画已移除：首屏立刻可见 */

/* Shimmer sweep across contact buttons on hover */
.contact-btn{position:relative; overflow:hidden;}
.contact-btn::after{
  content:"";
  position:absolute;
  top:0; left:-120%;
  width:60%; height:100%;
  background:linear-gradient(120deg, transparent, rgba(255,255,255,0.55), transparent);
  transition:left 0.6s ease;
}
.contact-btn:hover::after{ left:120%; }

/* Subtle floating dots in about-card background */
.about-card{position:relative;}
.about-card .float-orbs{
  position:absolute; inset:0;
  pointer-events:none;
  overflow:hidden;
  border-radius:20px;
  z-index:0;
}
.about-card .float-orbs span{
  position:absolute;
  display:block;
  border-radius:50%;
  background:radial-gradient(circle, rgba(99,102,241,0.30), rgba(99,102,241,0));
  filter:blur(2px);
  animation:float-orb 14s ease-in-out infinite;
}
.about-card .float-orbs span:nth-child(1){width:140px;height:140px;top:5%; left:65%;animation-delay:0s;}
.about-card .float-orbs span:nth-child(2){width:90px; height:90px; top:55%;left:8%; background:radial-gradient(circle, rgba(6,182,212,0.30), rgba(6,182,212,0));animation-delay:-4s;}
.about-card .float-orbs span:nth-child(3){width:120px;height:120px;top:78%;left:78%;background:radial-gradient(circle, rgba(139,92,246,0.26), rgba(139,92,246,0));animation-delay:-8s;}
@keyframes float-orb{
  0%, 100% { transform: translate(0,0) scale(1); opacity:0.7; }
  50%      { transform: translate(20px,-30px) scale(1.15); opacity:1; }
}
.about-card > *{ position:relative; z-index:1; }

/* ===============================
   Research Group card (Mt-aistudio)
   =============================== */
.research-group-card{
  position:relative;
  display:flex;
  align-items:center;
  gap:0.85rem;
  padding:0.85rem 1rem;
  border-radius:14px;
  border:1px solid rgba(99,102,241,0.18);
  background:linear-gradient(135deg, rgba(99,102,241,0.10), rgba(6,182,212,0.05));
  text-decoration:none !important;
  color:#1d4ed8 !important;
  font-weight:700;
  overflow:hidden;
  transition: transform 0.28s ease, box-shadow 0.28s ease, border-color 0.28s ease;
  box-shadow:0 3px 12px rgba(99,102,241,0.10);
}
.research-group-card:hover{
  transform:translateY(-3px);
  border-color:rgba(99,102,241,0.42);
  box-shadow:0 12px 28px rgba(99,102,241,0.22);
}
.rgc-glow{
  position:absolute;
  inset:-40% -40% auto auto;
  width:140px; height:140px;
  background:radial-gradient(circle, rgba(139,92,246,0.30), transparent 70%);
  filter:blur(8px);
  animation:float-orb 9s ease-in-out infinite;
  pointer-events:none;
}
.rgc-icon{
  flex-shrink:0;
  width:38px; height:38px;
  display:flex; align-items:center; justify-content:center;
  border-radius:12px;
  font-size:1.2rem;
  background:linear-gradient(135deg, rgba(99,102,241,0.22), rgba(6,182,212,0.12));
  border:1px solid rgba(99,102,241,0.20);
}
.rgc-content{ flex:1; min-width:0; }
.rgc-title{
  font-size:0.98rem;
  font-weight:850;
  color:#1d4ed8;
  letter-spacing:0.01em;
}
.rgc-sub{
  font-size:0.75rem;
  font-weight:600;
  color:#64748b;
  margin-top:0.1rem;
}
.rgc-arrow{
  width:18px; height:18px;
  color:#4f46e5;
  transition:transform 0.28s ease;
  flex-shrink:0;
}
.research-group-card:hover .rgc-arrow{ transform:translateX(3px); }
</style>

<!-- ===============================
     About Me
     =============================== -->
<span class="anchor" id="about-me"></span>
<div class="about-card">
  <div class="float-orbs" aria-hidden="true">
    <span></span><span></span><span></span>
  </div>
  <div class="about-card-header">
    <div class="about-card-title-wrap">
      <h2 class="about-card-title">About Me</h2>
      <div class="about-card-line"></div>
    </div>
    <div class="about-header-meta">
      <div class="about-contact-row about-contact-row--compact">
        <a class="contact-btn" href="https://mail.nudt.edu.cn/" target="_blank" rel="noopener" title="zhifengwang@nudt.edu.cn">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          NUDT
        </a>
        <a class="contact-btn" href="https://mail.google.com/" target="_blank" rel="noopener" title="zhifengwang686@gmail.com">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          Gmail
        </a>
      </div>
      <span class="about-status-badge" title="Currently open to research collaborations">
        <span class="status-dot" aria-hidden="true"></span>
        <span>Available for collaborations</span>
      </span>
    </div>
  </div>

  <p class="about-intro">
    Hi, I am <strong>Zhifeng Wang (汪智峰)</strong>, a third-year master's student at the College of Computer Science and Technology,
    National University of Defense Technology, advised by Prof. <a href="https://kevinkaixu.net/">Kai Xu</a> and Assoc. Prof.
    <a href="https://renjiaoyi.github.io/">Renjiao Yi</a>.
  </p>

  <div class="research-scope">
<p style="
  margin: 0;
  line-height: 1.85;
  font-size: 1.03rem;
  color: #374151;
">
  My research focuses on
  <span style="font-weight:700; color:#1f3a8a;">computer vision and medical AI</span>,
  building
  <span style="font-weight:700; color:#4f46e5;">world models</span>
  and
  <span style="font-weight:600; color:#4338ca;">large language models</span>
  that perceive, reason about, and generate the visual world.
  By integrating
  <span style="font-weight:600; color:#0f766e;">structural priors</span>
  and
  <span style="font-weight:600; color:#0f766e;">explicit physical constraints</span>,
  I aim to improve the
  <span style="font-weight:600; color:#7c2d12;">robustness</span>
  and
  <span style="font-weight:600; color:#7c2d12;">generalization</span>
  of learned representations for
  <span style="font-weight:600; color:#374151; text-decoration:underline;">real-world deployment</span>.
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

  <div class="about-cards-row">
    <div class="focus-section">
      <h3 class="focus-header">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#4f46e5" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
        Current Focus
      </h3>
      <div class="focus-chips">
        <span class="focus-chip chip-indigo"><span class="chip-icon">🌍</span> World Models &amp; Simulation</span>
        <span class="focus-chip chip-blue"><span class="chip-icon">👁️</span> Computer Vision &amp; 3D</span>
        <span class="focus-chip chip-violet"><span class="chip-icon">🧠</span> Large Language Models</span>
        <span class="focus-chip chip-emerald"><span class="chip-icon">🏥</span> Medical AI &amp; Imaging</span>
        <span class="focus-chip chip-teal"><span class="chip-icon">✨</span> Generative Modeling</span>
        <span class="focus-chip chip-rose"><span class="chip-icon">⚛️</span> Physics-informed Intelligence</span>
      </div>
    </div>

    <div class="about-highlights">
      <h3 class="highlights-header">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
        Highlights
        <span class="highlights-orbit" aria-hidden="true">
          <span class="orbit-ring"></span>
          <span class="orbit-dot"></span>
        </span>
      </h3>
      <ul class="highlights-list">
        <li class="hl-item">
          <div class="hl-icon"><span>📄</span></div>
          <div class="hl-content">
            <div class="hl-number">8+ <span class="hl-unit">Papers</span></div>
            <div class="hl-label">Published / Under review</div>
          </div>
        </li>
        <li class="hl-item">
          <div class="hl-icon"><span>🏆</span></div>
          <div class="hl-content">
            <div class="hl-number">CVPR 2025</div>
            <div class="hl-label">Top-tier CV conference (CCF-A)</div>
          </div>
        </li>
        <li class="hl-item">
          <div class="hl-icon"><span>🥇</span></div>
          <div class="hl-content">
            <div class="hl-number">1st Place</div>
            <div class="hl-label">CVPR&#39;25W · MAI Bokeh Challenge</div>
          </div>
        </li>
        <li class="hl-item">
          <div class="hl-icon"><span>🎓</span></div>
          <div class="hl-content">
            <div class="hl-number">2× National Scholar.</div>
            <div class="hl-label">Top 0.2% · Rank 3 / 183</div>
          </div>
        </li>
      </ul>
    </div>
  </div>

  <span class="about-pill about-pill--bottom">Open to research-oriented collaborations in computer vision, medical AI, world models, and large language models.</span>

  <div class="about-philosophy">
    As a result of this honesty, we are forced to doubt. — Richard Feynman
  </div>
</div>

<!-- ===============================
     Tools & Projects
     =============================== -->
<h2 class="section-title"><span class="section-emoji">🛠</span> Tools & Projects</h2>
{% capture tools_cards %}
  <a href="https://paperscope.top" target="_blank" rel="noopener" class="tool-card tool-card--paperscope">
    <div class="tool-card-cover" aria-hidden="true">
      <div class="cover-grid"></div>
      <div class="cover-glow"></div>
    </div>
    <div class="tool-card-body">
      <div class="tool-icon" aria-hidden="true">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="7" y="3" width="13" height="16" rx="1.5"/>
          <path d="M3 7v14h14"/>
          <line x1="11" y1="9" x2="17" y2="9"/>
          <line x1="11" y1="13" x2="17" y2="13"/>
          <line x1="11" y1="17" x2="14" y2="17"/>
        </svg>
      </div>
      <div class="tool-card-text">
        <div class="tool-title-row">
          <h3>Paperscope</h3>
          <span class="tool-status"><span class="status-dot status-dot--live" aria-hidden="true"></span>Live</span>
          <svg class="tool-arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <line x1="7" y1="17" x2="17" y2="7"/>
            <polyline points="9 7 17 7 17 15"/>
          </svg>
        </div>
        <p class="tool-tagline">Discover · Browse · Explore AI papers</p>
        <p class="tool-desc">A comprehensive platform for AI research papers. Search and explore cutting-edge work in computer vision and medical imaging.</p>
        <div class="tool-footer">
          <span class="tool-tag">Research Platform</span>
          <span class="tool-domain">paperscope.top</span>
        </div>
      </div>
    </div>
  </a>

  <a href="https://cc.cchub.cloud/" target="_blank" rel="noopener" class="tool-card tool-card--ccconsole">
    <div class="tool-card-cover" aria-hidden="true">
      <div class="cover-grid"></div>
      <div class="cover-glow"></div>
    </div>
    <div class="tool-card-body">
      <div class="tool-icon" aria-hidden="true">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="4" width="20" height="16" rx="2"/>
          <polyline points="6 9 9 12 6 15"/>
          <line x1="12" y1="15" x2="17" y2="15"/>
        </svg>
      </div>
      <div class="tool-card-text">
        <div class="tool-title-row">
          <h3>CC-Console</h3>
          <span class="tool-status"><span class="status-dot status-dot--live" aria-hidden="true"></span>Live</span>
          <svg class="tool-arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <line x1="7" y1="17" x2="17" y2="7"/>
            <polyline points="9 7 17 7 17 15"/>
          </svg>
        </div>
        <p class="tool-tagline">Manage · Monitor · Claude Code</p>
        <p class="tool-desc">A web console for Claude Code — launch and track agent sessions, monitor token usage and cost, and control your workflows from a single dashboard. My latest software.</p>
        <div class="tool-footer">
          <span class="tool-tag">Claude Code Console</span>
          <span class="tool-domain">cc.cchub.cloud</span>
        </div>
      </div>
    </div>
  </a>

  <a href="https://motong-ai-studio.github.io/" target="_blank" rel="noopener" class="tool-card tool-card--mtaistudio">
    <div class="tool-card-cover" aria-hidden="true">
      <div class="cover-grid"></div>
      <div class="cover-glow"></div>
    </div>
    <div class="tool-card-body">
      <div class="tool-icon" aria-hidden="true">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="4" y="4" width="16" height="16" rx="2"/>
          <rect x="9" y="9" width="6" height="6"/>
          <line x1="9" y1="2" x2="9" y2="4"/>
          <line x1="15" y1="2" x2="15" y2="4"/>
          <line x1="9" y1="20" x2="9" y2="22"/>
          <line x1="15" y1="20" x2="15" y2="22"/>
          <line x1="20" y1="9" x2="22" y2="9"/>
          <line x1="20" y1="14" x2="22" y2="14"/>
          <line x1="2" y1="9" x2="4" y2="9"/>
          <line x1="2" y1="14" x2="4" y2="14"/>
        </svg>
      </div>
      <div class="tool-card-text">
        <div class="tool-title-row">
          <h3>Mt-aistudio</h3>
          <span class="tool-status tool-status--member"><span class="status-dot status-dot--member" aria-hidden="true"></span>Core Member</span>
          <svg class="tool-arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <line x1="7" y1="17" x2="17" y2="7"/>
            <polyline points="9 7 17 7 17 15"/>
          </svg>
        </div>
        <p class="tool-tagline">CV Research Group · Collaborative</p>
        <p class="tool-desc">A research group focusing on computer vision and generative modeling. Collaborate with peers on cutting-edge CV projects.</p>
        <div class="tool-footer">
          <span class="tool-tag">Research Group</span>
          <span class="tool-domain">motong-ai-studio.github.io</span>
        </div>
      </div>
    </div>
  </a>
{% endcapture %}

<div class="tools-marquee">
  <div class="tools-viewport">
    <div class="tools-track">
      {{ tools_cards }}
      <span class="tools-dup" aria-hidden="true">{{ tools_cards }}</span>
    </div>
  </div>
</div>

<style>
/* ---- Auto-scrolling carousel inside an animated gradient frame ---- */
.tools-marquee{
  position:relative;
  margin-top:0.9rem;
  padding:1.15rem;
  border-radius:22px;
  background:linear-gradient(135deg, rgba(99,102,241,0.05), rgba(16,185,129,0.045) 60%, rgba(168,85,247,0.05));
  overflow:hidden;
  isolation:isolate;
}
/* animated gradient border ("dynamic frame") */
.tools-marquee::before{
  content:"";
  position:absolute; inset:0;
  border-radius:22px;
  padding:1.6px;
  background:linear-gradient(120deg,#6366f1,#06b6d4,#10b981,#a855f7,#6366f1);
  background-size:300% 300%;
  animation: toolsFrame 9s ease infinite;
  -webkit-mask:linear-gradient(#000 0 0) content-box, linear-gradient(#000 0 0);
          mask:linear-gradient(#000 0 0) content-box, linear-gradient(#000 0 0);
  -webkit-mask-composite:xor; mask-composite:exclude;
  pointer-events:none;
  z-index:2;
}
@keyframes toolsFrame{
  0%{ background-position:0% 50%; }
  50%{ background-position:100% 50%; }
  100%{ background-position:0% 50%; }
}
/* viewport clips the track and fades both edges */
.tools-viewport{
  overflow:hidden;
  -webkit-mask-image:linear-gradient(to right, transparent, #000 5%, #000 95%, transparent);
          mask-image:linear-gradient(to right, transparent, #000 5%, #000 95%, transparent);
}
.tools-track{
  display:flex;
  width:max-content;
  align-items:stretch;
  animation: toolsMarquee 32s linear infinite;
}
.tools-marquee:hover .tools-track{ animation-play-state:paused; }
.tools-dup{ display:contents; }
@keyframes toolsMarquee{
  from{ transform:translateX(0); }
  to{ transform:translateX(-50%); }
}
@media (prefers-reduced-motion: reduce){
  .tools-track{ animation:none; }
  .tools-marquee::before{ animation:none; }
}

.tool-card{
  position:relative;
  display:flex;
  flex-direction:column;
  flex:0 0 360px;
  width:360px;
  margin-right:1.25rem;
  border-radius:18px;
  overflow:hidden;
  text-decoration:none !important;
  color:inherit !important;
  background:#ffffff;
  border:1px solid rgba(99,102,241,0.16);
  box-shadow:0 6px 20px rgba(17,24,39,0.06);
  transition: transform 0.32s ease, box-shadow 0.32s ease, border-color 0.32s ease;
  isolation:isolate;
}
.tool-card:hover{
  transform:translateY(-6px);
  box-shadow:0 22px 46px rgba(99,102,241,0.18);
  border-color:rgba(99,102,241,0.45);
}

/* Top cover banner */
.tool-card-cover{
  position:relative;
  height:66px;
  overflow:hidden;
}
.tool-card--paperscope .tool-card-cover{
  background:linear-gradient(135deg, #4f46e5 0%, #2563eb 55%, #06b6d4 100%);
}
.tool-card--mtaistudio .tool-card-cover{
  background:linear-gradient(135deg, #7c3aed 0%, #a855f7 50%, #ec4899 100%);
}
.tool-card--ccconsole .tool-card-cover{
  background:linear-gradient(135deg, #0f766e 0%, #10b981 55%, #34d399 100%);
}
.cover-grid{
  position:absolute; inset:0;
  background-image: radial-gradient(rgba(255,255,255,0.20) 1px, transparent 1px);
  background-size:14px 14px;
  opacity:0.55;
}
.cover-glow{
  position:absolute;
  top:-50%; right:-15%;
  width:170px; height:170px;
  background:radial-gradient(circle, rgba(255,255,255,0.55), transparent 70%);
  filter:blur(8px);
  transition: transform 0.7s ease;
  pointer-events:none;
}
.tool-card:hover .cover-glow{
  transform: translate(-40px, 30px) scale(1.25);
}

/* Body */
.tool-card-body{
  position:relative;
  flex:1 1 auto;
  display:flex;
  flex-direction:column;
  padding:1rem 1.2rem 1.15rem 1.2rem;
}
.tool-icon{
  position:absolute;
  top:-26px; left:1.2rem;
  width:52px; height:52px;
  border-radius:14px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:#ffffff;
  color:#4f46e5;
  border:1px solid rgba(99,102,241,0.20);
  box-shadow:0 8px 20px rgba(17,24,39,0.14);
  transition: transform 0.35s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.35s ease;
}
.tool-card--mtaistudio .tool-icon{ color:#7c3aed; border-color:rgba(139,92,246,0.20); }
.tool-card--ccconsole .tool-icon{ color:#0d9488; border-color:rgba(16,185,129,0.22); }
.tool-card:hover .tool-icon{
  transform:scale(1.08) rotate(-6deg);
  box-shadow:0 12px 26px rgba(17,24,39,0.18);
}

.tool-card-text{ margin-top:1.55rem; flex:1 1 auto; display:flex; flex-direction:column; }
.tool-title-row{
  display:flex; align-items:center; gap:0.55rem;
  margin-bottom:0.18rem;
}
.tool-title-row h3{
  margin:0;
  font-size:1.18rem;
  font-weight:850;
  color:#1d4ed8;
  letter-spacing:-0.005em;
}
.tool-card--mtaistudio .tool-title-row h3{ color:#7c3aed; }
.tool-card--ccconsole .tool-title-row h3{ color:#0d9488; }

.tool-status{
  display:inline-flex;
  align-items:center;
  gap:0.35rem;
  padding:0.18rem 0.55rem;
  border-radius:999px;
  font-size:0.7rem;
  font-weight:800;
  letter-spacing:0.02em;
  color:#047857;
  background:rgba(16,185,129,0.10);
  border:1px solid rgba(16,185,129,0.28);
}
.tool-status .status-dot{
  width:6px; height:6px;
}
.tool-status--member{
  color:#7c3aed;
  background:rgba(139,92,246,0.12);
  border-color:rgba(139,92,246,0.30);
}
.tool-status--member .status-dot{ background:#a855f7; box-shadow:none; animation:none; }

.tool-arrow{
  width:16px; height:16px;
  color:#94a3b8;
  margin-left:auto;
  transition: transform 0.3s ease, color 0.3s ease;
}
.tool-card:hover .tool-arrow{
  color:#4f46e5;
  transform: translate(3px, -3px);
}
.tool-card--mtaistudio:hover .tool-arrow{ color:#7c3aed; }
.tool-card--ccconsole:hover .tool-arrow{ color:#0d9488; }

.tool-tagline{
  margin:0.2rem 0 0.65rem 0 !important;
  font-size:0.74rem !important;
  font-weight:800;
  letter-spacing:0.06em;
  text-transform:uppercase;
  color:#6366f1;
  line-height:1.4 !important;
}
.tool-card--mtaistudio .tool-tagline{ color:#8b5cf6; }
.tool-card--ccconsole .tool-tagline{ color:#10b981; }

.tool-desc{
  margin:0 0 0.85rem 0 !important;
  font-size:0.88rem !important;
  line-height:1.6 !important;
  color:#475569;
}

.tool-footer{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:0.6rem;
  flex-wrap:wrap;
  margin-top:auto;
}
.tool-tag{
  display:inline-flex;
  align-items:center;
  padding:0.22rem 0.65rem;
  border-radius:999px;
  font-size:0.72rem;
  font-weight:750;
  color:#4f46e5;
  background:rgba(99,102,241,0.10);
  border:1px solid rgba(99,102,241,0.22);
  letter-spacing:0.01em;
}
.tool-card--mtaistudio .tool-tag{
  color:#7c3aed;
  background:rgba(139,92,246,0.10);
  border-color:rgba(139,92,246,0.28);
}
.tool-card--ccconsole .tool-tag{
  color:#0d9488;
  background:rgba(16,185,129,0.10);
  border-color:rgba(16,185,129,0.28);
}
.tool-domain{
  font-size:0.72rem;
  font-weight:650;
  color:#94a3b8;
  font-family: Menlo, Monaco, "Lucida Console", monospace;
  letter-spacing:0.01em;
}
</style>

<!-- ===============================
     News
     =============================== -->
<span class="anchor" id="news"></span>
<h2 class="section-title"><span class="section-emoji">🔥</span> News</h2>
<div class="news-card news-fade">
  <div class="news-scroll">
    <ul class="news-list">
      <li><em>2026.04</em>🎉 One paper is accepted by ICML 2026, Congratulations to Xingyue.</li>
      <li><em>2026.01</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">ICASSP 2026</a>, Congratulations to Lubing.</li>
      <li><em>2025.11</em>🎉 Awarded the <a href="https://jefferyzhifeng.github.io">China National Scholarship</a> (Ranking 3/183).</li>
      <li><em>2025.05</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">TVC Journal</a>.</li>
      <li><em>2025.04</em>🎉 Won 1st place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21562#learn_the_details">CVPR2025W</a> "Mobile AI 2025 Real-Time Rendering Realistic Bokeh Challenge", Congratulations to Kang.</li>
      <li><em>2025.04</em>🎉 Won 6th place in the <a href="https://codalab.lisn.upsaclay.fr/competitions/21564">CVPR2025W</a> "Mobile AI Challenge: RGB Photo Enhancement on Mobile GPUs", Congratulations to Runhua.</li>
      <li><em>2025.02</em>🎉 One paper is accepted by <a href="https://cvpr.thecvf.com/Conferences/2025/">CVPR 2025</a> (CCF-A).</li>
      <li><em>2024.09</em>🎉 One paper is accepted by <a href="https://www.sciencedirect.com/science/article/pii/S2950162824000560">Meta-Radiology</a>.</li>
      <li><em>2024.07</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">FCS Journal</a> (CCF-T1).</li>
      <li><em>2024.05</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">ICIP 2024</a>.</li>
      <li><em>2022.12</em>🎉 Awarded the <a href="https://jefferyzhifeng.github.io">China National Scholarship</a> (Top 0.2%).</li>
      <li><em>2022.10</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">PRCV</a>.</li>
      <li><em>2022.06</em>🎉 One paper is accepted by <a href="https://jefferyzhifeng.github.io">JVCIR Journal</a>.</li>
    </ul>
  </div>
</div>

<!-- ===============================
     Publications
     =============================== -->
<span class="anchor" id="publications"></span>
<h2 class="section-title"><span class="section-emoji">📝</span> Publications</h2>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Preprint 2026</div>
    <img src="images/2026_icml.png" alt="PhysConSR teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io/">
      PhysConSR: Learning Fast Differentiable Physically-Informed Continuous Medical Super-Resolution via 2D Gaussians
    </a>
    <div class="paper-authors"><strong>Zhifeng Wang</strong>, Long Peng, Xingyue Zhao, Chenyang Zhu, Kai Xu, Renjiao Yi.</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/">Project</a></div>
    <ul class="paper-meta">
      <li>Under Review, 2026.</li>
    </ul>
  </div>
</div>

<div class="paper-box">
  <div class="paper-box-image">
    <div class="paper-badge">Preprint 2025</div>
    <img src="images/2025nc.png" alt="Science Advances teaser">
  </div>
  <div class="paper-box-text">
    <a class="paper-title" href="https://jefferyzhifeng.github.io/">
      Time-indexed reuse of physical states for hardware-efficient in-sensor visual computing
    </a>
    <div class="paper-authors">Xiong, J., Huang, M., <strong>Zhifeng Wang</strong>, et al.</div>
    <div class="paper-links"><a href="https://jefferyzhifeng.github.io/">Project</a></div>
    <ul class="paper-meta">
      <li>Science Advances, Under Review, 2025.</li>
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
<span class="anchor" id="honors"></span>
<h2 class="section-title"><span class="section-emoji">🎖</span> Honors and Awards</h2>

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

<ul style="line-height:1.75; margin-top:0.4rem;">
  <li><em>2025.11</em> China National Scholarship (3/183), 2025.</li>
  <li><em>2022.11</em> China National Scholarship (Top 0.2%), 2022.</li>
  <li><em>2022.09</em> First-class Academic Scholarship, 2022.</li>
  <li><em>2021.09</em> First-class Academic Scholarship, 2021.</li>
  <li><em>2020.09</em> First-class Academic Scholarship, 2020.</li>
</ul>

<!-- ===============================
     Services / Internships
     =============================== -->
<span class="anchor" id="services"></span>
<h2 class="section-title"><span class="section-emoji">📖</span> Services</h2>
<ul style="line-height:1.75;">
  <li><strong>Reviewers:</strong> PRCV’23/24, CAD/CG, JVCIR, PG.</li>
  <li><strong>Memberships:</strong> IEEE Student Member, CSIG Student Member, CAAI Student Member, CVF Member.</li>
</ul>

<span class="anchor" id="internships"></span>
<h2 class="section-title"><span class="section-emoji">💻</span> Internships</h2>

<div class="intern-grid">
  <a class="intern-card" href="https://www.antgroup.com/" target="_blank" rel="noopener">
    <div class="intern-logo">
      <img src="images/logos/ant.png" alt="Ant Group logo"
           onerror="this.style.display='none'; this.parentNode.querySelector('.intern-logo-fallback').style.display='flex';">
      <div class="intern-logo-fallback" aria-hidden="true">蚂</div>
    </div>
    <div class="intern-content">
      <h4 class="intern-company">Ant Group <span class="intern-badge intern-badge-ant">2026</span></h4>
      <div class="intern-role">医疗大模型算法 · Medical LLMs Algorithm</div>
      <div class="intern-location">Hangzhou, China</div>
    </div>
  </a>

  <a class="intern-card" href="https://damo.alibaba.com/?language=zh" target="_blank" rel="noopener">
    <div class="intern-logo">
      <img src="images/logos/damo.png" alt="Alibaba DAMO Academy logo"
           onerror="this.style.display='none'; this.parentNode.querySelector('.intern-logo-fallback').style.display='flex';">
      <div class="intern-logo-fallback" aria-hidden="true">达</div>
    </div>
    <div class="intern-content">
      <h4 class="intern-company">Alibaba DAMO Academy <span class="intern-badge intern-badge-damo">2025</span></h4>
      <div class="intern-role">研究型算法研究员 · Research Algorithm Scientist</div>
      <div class="intern-location">Hangzhou, China</div>
    </div>
  </a>

  <a class="intern-card" href="https://www.speedbot.com/en/home" target="_blank" rel="noopener">
    <div class="intern-logo">
      <img src="images/logos/speedbot.png" alt="SpeedBot Robotics logo"
           onerror="this.style.display='none'; this.parentNode.querySelector('.intern-logo-fallback').style.display='flex';">
      <div class="intern-logo-fallback" aria-hidden="true">S</div>
    </div>
    <div class="intern-content">
      <h4 class="intern-company">SpeedBot Robotics <span class="intern-badge intern-badge-speedbot">2022–2023</span></h4>
      <div class="intern-role">Algorithm Engineer Intern</div>
      <div class="intern-location">Changsha, China</div>
    </div>
  </a>
</div>

<style>
.intern-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 1rem;
  margin-top: 0.6rem;
}
.intern-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem 1.1rem;
  border-radius: 14px;
  border: 1px solid rgba(99,102,241,0.15);
  background: linear-gradient(135deg, rgba(99,102,241,0.08) 0%, rgba(255,255,255,0.95) 100%);
  text-decoration: none !important;
  transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
  box-shadow: 0 4px 16px rgba(17,24,39,0.06);
  color: inherit;
}
.intern-card:hover {
  transform: translateY(-3px);
  border-color: rgba(99,102,241,0.35);
  box-shadow: 0 12px 28px rgba(99,102,241,0.18);
}
.intern-logo {
  position: relative;
  flex-shrink: 0;
  width: 56px;
  height: 56px;
  border-radius: 14px;
  background: #ffffff;
  border: 1px solid rgba(99,102,241,0.18);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(17,24,39,0.06);
}
.intern-logo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  padding: 6px;
  display: block;
}
.intern-logo-fallback {
  display: none;
  width: 100%;
  height: 100%;
  align-items: center;
  justify-content: center;
  font-weight: 850;
  font-size: 1.4rem;
  color: #4f46e5;
  background: linear-gradient(135deg, rgba(99,102,241,0.18), rgba(37,99,235,0.10));
}
.intern-content { flex: 1; min-width: 0; }
.intern-company {
  margin: 0 0 0.28rem 0;
  font-size: 1.05rem;
  font-weight: 800;
  color: #1d4ed8;
  display: flex;
  align-items: center;
  gap: 0.55rem;
  flex-wrap: wrap;
}
.intern-badge {
  display: inline-flex;
  align-items: center;
  padding: 0.12rem 0.55rem;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 750;
  letter-spacing: 0.02em;
}
.intern-badge-ant      { color:#0e7490; background:rgba(6,182,212,0.14);  border:1px solid rgba(6,182,212,0.30); }
.intern-badge-damo     { color:#9a3412; background:rgba(249,115,22,0.14); border:1px solid rgba(249,115,22,0.30); }
.intern-badge-speedbot { color:#374151; background:rgba(100,116,139,0.14); border:1px solid rgba(100,116,139,0.30); }
.intern-role {
  font-size: 0.95rem;
  color: #334155;
  font-weight: 600;
  margin-bottom: 0.18rem;
}
.intern-location {
  font-size: 0.82rem;
  color: #64748b;
  display: inline-flex;
  align-items: center;
  gap: 0.32rem;
}
.intern-location::before {
  content: "📍";
  font-size: 0.85rem;
}
</style>



<hr>

<p align="center">
  <i>I know I am not the perfect one, yet aspire to chase the world and achieve greatness @ Zhifeng Wang — Latest update: 2026-04-23</i>
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
