<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abdelrhman Mabrouk — Robotics Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0a0c0f;
  --bg2: #111418;
  --bg3: #181c22;
  --border: rgba(255,255,255,0.07);
  --border2: rgba(255,255,255,0.13);
  --text: #e8e6e0;
  --muted: #8a8780;
  --accent: #4fc4a0;
  --accent2: #2a8a6e;
  --accent-dim: rgba(79,196,160,0.12);
  --accent-dim2: rgba(79,196,160,0.06);
  --gold: #c9a84c;
  --gold-dim: rgba(201,168,76,0.12);
  --blue: #5b9ef0;
  --blue-dim: rgba(91,158,240,0.12);
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Outfit', sans-serif;
  font-weight: 300;
  line-height: 1.7;
  min-height: 100vh;
}

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 3rem;
  height: 64px;
  background: rgba(10,12,15,0.85);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: 'DM Serif Display', serif;
  font-size: 1.1rem;
  color: var(--accent);
  letter-spacing: 0.02em;
  text-decoration: none;
}
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
  text-decoration: none;
  color: var(--muted);
  font-size: 0.82rem;
  font-weight: 400;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--text); }

/* ── HERO ── */
#hero {
  min-height: 100vh;
  display: flex; align-items: center;
  padding: 0 3rem;
  position: relative;
  overflow: hidden;
}
.hero-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  max-width: 1100px;
  margin: 0 auto;
  width: 100%;
  padding-top: 64px;
}
.hero-eyebrow {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 1.2rem;
  display: flex; align-items: center; gap: 0.75rem;
}
.hero-eyebrow::before {
  content: '';
  display: inline-block;
  width: 28px; height: 1px;
  background: var(--accent);
}
h1 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.8rem, 5vw, 4.2rem);
  font-weight: 400;
  line-height: 1.12;
  letter-spacing: -0.01em;
  margin-bottom: 1.5rem;
}
h1 em {
  font-style: italic;
  color: var(--accent);
}
.hero-desc {
  color: var(--muted);
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 2.5rem;
  max-width: 440px;
}
.hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
.btn {
  display: inline-flex; align-items: center; gap: 0.5rem;
  padding: 0.7rem 1.6rem;
  border-radius: 2px;
  font-size: 0.82rem;
  font-weight: 500;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  text-decoration: none;
  transition: all 0.2s;
  cursor: pointer;
}
.btn-primary {
  background: var(--accent);
  color: #0a0c0f;
  border: 1px solid var(--accent);
}
.btn-primary:hover { background: #3db08d; border-color: #3db08d; }
.btn-ghost {
  background: transparent;
  color: var(--text);
  border: 1px solid var(--border2);
}
.btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

/* hero right — stats */
.hero-stats {
  display: flex; flex-direction: column;
  justify-content: center; gap: 0;
}
.stat-item {
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border);
  display: flex; justify-content: space-between; align-items: flex-end;
}
.stat-item:first-child { border-top: 1px solid var(--border); }
.stat-num {
  font-family: 'DM Serif Display', serif;
  font-size: 2.8rem;
  color: var(--accent);
  line-height: 1;
}
.stat-label {
  font-size: 0.82rem;
  color: var(--muted);
  text-align: right;
  max-width: 160px;
  letter-spacing: 0.02em;
}

/* background decoration */
.bg-grid {
  position: absolute; inset: 0; z-index: -1;
  background-image: linear-gradient(var(--border) 1px, transparent 1px), linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 60px 60px;
  opacity: 0.4;
  mask-image: radial-gradient(ellipse 70% 70% at 80% 50%, black 30%, transparent 80%);
}
.bg-glow {
  position: absolute; right: -10%; top: 20%;
  width: 600px; height: 600px; border-radius: 50%;
  background: radial-gradient(circle, rgba(79,196,160,0.06) 0%, transparent 70%);
  pointer-events: none; z-index: -1;
}

/* ── SECTIONS ── */
section { padding: 7rem 3rem; }
.section-inner { max-width: 1100px; margin: 0 auto; }
.section-label {
  font-family: 'DM Mono', monospace;
  font-size: 0.68rem;
  color: var(--accent);
  letter-spacing: 0.18em;
  text-transform: uppercase;
  margin-bottom: 0.75rem;
  display: flex; align-items: center; gap: 0.75rem;
}
.section-label::before {
  content: '';
  width: 24px; height: 1px;
  background: var(--accent);
}
h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2rem, 3.5vw, 2.8rem);
  font-weight: 400;
  line-height: 1.2;
  margin-bottom: 3.5rem;
}

/* ── EXPERIENCE ── */
#experience { background: var(--bg2); }
.exp-list { display: flex; flex-direction: column; gap: 0; }
.exp-item {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 3rem;
  padding: 2.5rem 0;
  border-bottom: 1px solid var(--border);
}
.exp-item:first-child { border-top: 1px solid var(--border); }
.exp-meta { padding-top: 0.2rem; }
.exp-date {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 0.08em;
  margin-bottom: 0.4rem;
}
.exp-company {
  font-size: 0.85rem;
  color: var(--muted);
}
.exp-title {
  font-size: 1.1rem;
  font-weight: 500;
  color: var(--text);
  margin-bottom: 0.6rem;
}
.exp-location {
  font-size: 0.8rem;
  color: var(--muted);
  margin-bottom: 1rem;
  font-family: 'DM Mono', monospace;
}
.exp-body { font-size: 0.92rem; color: var(--muted); line-height: 1.8; }
.exp-body ul { padding-left: 1.1rem; }
.exp-body li { margin-bottom: 0.35rem; }
.exp-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 1rem; }
.tag {
  font-size: 0.7rem;
  font-family: 'DM Mono', monospace;
  padding: 3px 10px;
  border-radius: 2px;
  background: var(--accent-dim2);
  border: 1px solid rgba(79,196,160,0.2);
  color: var(--accent);
  letter-spacing: 0.04em;
}

/* ── INTERNSHIP / PROJECT PHASES ── */
#internship { background: var(--bg); }
.phases-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5px;
  background: var(--border);
  border: 1px solid var(--border);
}
.phase-card {
  background: var(--bg);
  padding: 2rem;
  position: relative;
  overflow: hidden;
  transition: background 0.2s;
}
.phase-card:hover { background: var(--bg3); }
.phase-num {
  font-family: 'DM Serif Display', serif;
  font-size: 3.5rem;
  color: rgba(79,196,160,0.1);
  line-height: 1;
  position: absolute;
  top: 1rem; right: 1.25rem;
}
.phase-status {
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 2px 8px;
  border-radius: 2px;
  margin-bottom: 1rem;
  display: inline-block;
}
.status-done { background: var(--accent-dim); color: var(--accent); border: 1px solid rgba(79,196,160,0.3); }
.status-ongoing { background: var(--gold-dim); color: var(--gold); border: 1px solid rgba(201,168,76,0.3); }
.phase-title {
  font-size: 1rem;
  font-weight: 500;
  margin-bottom: 0.75rem;
  color: var(--text);
}
.phase-body { font-size: 0.85rem; color: var(--muted); line-height: 1.75; }
.phase-body ul { padding-left: 1rem; }
.phase-body li { margin-bottom: 0.3rem; }

/* internship header info */
.internship-meta {
  display: flex; gap: 3rem;
  margin-bottom: 3rem;
  padding: 1.5rem 2rem;
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 2px;
}
.im-item {}
.im-label { font-family: 'DM Mono', monospace; font-size: 0.65rem; color: var(--accent); letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.25rem; }
.im-val { font-size: 0.88rem; color: var(--text); }

/* ── PROJECTS ── */
#projects { background: var(--bg2); }
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
}
.project-card {
  background: var(--bg2);
  padding: 1.75rem;
  transition: background 0.2s;
  position: relative;
}
.project-card:hover { background: var(--bg3); }
.project-card::before {
  content: '';
  position: absolute; top: 0; left: 0; right: 0;
  height: 2px;
  background: transparent;
  transition: background 0.2s;
}
.project-card:hover::before { background: var(--accent); }
.project-icon {
  width: 36px; height: 36px;
  background: var(--accent-dim);
  border: 1px solid rgba(79,196,160,0.2);
  border-radius: 2px;
  display: flex; align-items: center; justify-content: center;
  font-size: 1rem;
  margin-bottom: 1rem;
}
.project-title { font-size: 0.95rem; font-weight: 500; margin-bottom: 0.5rem; }
.project-desc { font-size: 0.82rem; color: var(--muted); line-height: 1.7; margin-bottom: 1rem; }
.project-tech { display: flex; flex-wrap: wrap; gap: 4px; }
.tech-tag {
  font-size: 0.65rem;
  font-family: 'DM Mono', monospace;
  padding: 2px 7px;
  border-radius: 2px;
  background: var(--bg3);
  border: 1px solid var(--border2);
  color: var(--muted);
}

/* ── GIAGBOT FEATURE ── */
#gigabot { background: var(--bg); }
.gigabot-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}
.gigabot-specs {
  display: flex; flex-direction: column; gap: 0;
}
.spec-row {
  display: grid;
  grid-template-columns: 1fr 1.4fr;
  gap: 1rem;
  padding: 0.85rem 0;
  border-bottom: 1px solid var(--border);
  font-size: 0.85rem;
}
.spec-row:first-child { border-top: 1px solid var(--border); }
.spec-key { color: var(--muted); font-family: 'DM Mono', monospace; font-size: 0.75rem; letter-spacing: 0.04em; }
.spec-val { color: var(--text); }
.highlight-box {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-left: 2px solid var(--accent);
  padding: 1.25rem 1.5rem;
  margin-bottom: 1.5rem;
  font-size: 0.88rem;
  color: var(--muted);
  line-height: 1.7;
}
.highlight-box strong { color: var(--text); font-weight: 500; }

/* ── SKILLS ── */
#skills { background: var(--bg2); }
.skills-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}
.skill-group {
  background: var(--bg);
  border: 1px solid var(--border);
  padding: 1.5rem;
}
.skill-group-label {
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  color: var(--accent);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  margin-bottom: 1rem;
  padding-bottom: 0.75rem;
  border-bottom: 1px solid var(--border);
}
.skill-list { display: flex; flex-direction: column; gap: 0.5rem; }
.skill-row { display: flex; align-items: center; justify-content: space-between; font-size: 0.83rem; }
.skill-name { color: var(--text); }
.skill-bar-wrap { width: 80px; height: 3px; background: var(--border2); border-radius: 2px; overflow: hidden; }
.skill-bar { height: 100%; background: var(--accent); border-radius: 2px; transition: width 1s ease; }

/* ── COVER LETTER ── */
#cover { background: var(--bg); }
.letter-wrap {
  max-width: 720px;
  margin: 0 auto;
  background: var(--bg2);
  border: 1px solid var(--border);
  padding: 3rem 3.5rem;
  position: relative;
}
.letter-wrap::before {
  content: '';
  position: absolute; top: 0; left: 0;
  width: 100%; height: 3px;
  background: linear-gradient(90deg, var(--accent), transparent);
}
.letter-header {
  margin-bottom: 2.5rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--border);
}
.letter-name {
  font-family: 'DM Serif Display', serif;
  font-size: 1.6rem;
  margin-bottom: 0.25rem;
}
.letter-contact { font-size: 0.8rem; color: var(--muted); font-family: 'DM Mono', monospace; line-height: 2; }
.letter-body { font-size: 0.9rem; line-height: 1.9; color: var(--muted); }
.letter-body p { margin-bottom: 1.25rem; }
.letter-body p:last-child { margin-bottom: 0; }
.letter-body strong { color: var(--text); font-weight: 500; }
.letter-sign {
  margin-top: 2rem;
  font-family: 'DM Serif Display', serif;
  font-size: 1.1rem;
  color: var(--text);
}

/* ── CONTACT ── */
#contact { background: var(--bg2); }
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}
.contact-info { display: flex; flex-direction: column; gap: 0; }
.contact-row {
  display: flex; align-items: center; gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--border);
}
.contact-row:first-child { border-top: 1px solid var(--border); }
.contact-icon {
  width: 34px; height: 34px;
  background: var(--accent-dim2);
  border: 1px solid rgba(79,196,160,0.2);
  border-radius: 2px;
  display: flex; align-items: center; justify-content: center;
  font-size: 0.9rem;
  flex-shrink: 0;
}
.contact-label { font-size: 0.7rem; font-family: 'DM Mono', monospace; color: var(--muted); letter-spacing: 0.08em; text-transform: uppercase; }
.contact-val { font-size: 0.88rem; color: var(--text); }
.contact-val a { color: var(--accent); text-decoration: none; }
.contact-val a:hover { text-decoration: underline; }
.contact-note {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-left: 2px solid var(--accent);
  padding: 1.5rem 2rem;
}
.contact-note h3 {
  font-family: 'DM Serif Display', serif;
  font-size: 1.3rem;
  font-weight: 400;
  margin-bottom: 0.75rem;
}
.contact-note p { font-size: 0.88rem; color: var(--muted); line-height: 1.8; }

/* ── FOOTER ── */
footer {
  background: var(--bg);
  border-top: 1px solid var(--border);
  padding: 2rem 3rem;
  display: flex; justify-content: space-between; align-items: center;
}
.footer-name { font-family: 'DM Serif Display', serif; font-size: 1rem; color: var(--accent); }
.footer-copy { font-size: 0.75rem; color: var(--muted); font-family: 'DM Mono', monospace; }

/* ── ANIMATIONS ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to { opacity: 1; transform: translateY(0); }
}
.hero-eyebrow { animation: fadeUp 0.6s ease both; animation-delay: 0.1s; }
h1 { animation: fadeUp 0.6s ease both; animation-delay: 0.2s; }
.hero-desc { animation: fadeUp 0.6s ease both; animation-delay: 0.3s; }
.hero-ctas { animation: fadeUp 0.6s ease both; animation-delay: 0.4s; }
.hero-stats { animation: fadeUp 0.6s ease both; animation-delay: 0.5s; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  nav { padding: 0 1.5rem; }
  .nav-links { gap: 1.2rem; }
  section { padding: 5rem 1.5rem; }
  #hero { padding: 0 1.5rem; }
  .hero-grid { grid-template-columns: 1fr; gap: 3rem; }
  .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
  .phases-grid { grid-template-columns: 1fr; }
  .projects-grid { grid-template-columns: 1fr 1fr; }
  .gigabot-inner { grid-template-columns: 1fr; }
  .skills-grid { grid-template-columns: 1fr 1fr; }
  .contact-grid { grid-template-columns: 1fr; gap: 2rem; }
  .internship-meta { flex-wrap: wrap; gap: 1.5rem; }
  footer { flex-direction: column; gap: 0.75rem; text-align: center; }
  .letter-wrap { padding: 2rem; }
}
@media (max-width: 600px) {
  .projects-grid { grid-template-columns: 1fr; }
  .skills-grid { grid-template-columns: 1fr; }
  .nav-links { display: none; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">AM</a>
  <ul class="nav-links">
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#gigabot">GigaBot</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#cover">Cover Letter</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="bg-grid"></div>
  <div class="bg-glow"></div>
  <div class="hero-grid">
    <div>
      <div class="hero-eyebrow">Robotics Engineer · Vienna, Austria</div>
      <h1>Abdelrhman<br><em>Mabrouk</em></h1>
      <p class="hero-desc">
        Mechatronics engineer building autonomous robotic systems. Currently a Research Intern at TU Wien IFT working on the GigaBot AMR — a 5G-enabled autonomous mobile robot for factory automation. Pursuing an MSc in Autonomous Vehicle Engineering at the University of Naples Federico II.
      </p>
      <div class="hero-ctas">
        <a href="#contact" class="btn btn-primary">Get in Touch</a>
        <a href="#experience" class="btn btn-ghost">View Experience</a>
      </div>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">2+</div>
        <div class="stat-label">Years in Embedded Software & Firmware</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">6</div>
        <div class="stat-label">Months of hands-on autonomous robotics research at TU Wien</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">3</div>
        <div class="stat-label">Programming languages across embedded and robotics stacks</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">6+</div>
        <div class="stat-label">Engineering projects spanning robotics, vision, and embedded systems</div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-inner">
    <div class="section-label">Career</div>
    <h2>Work Experience</h2>
    <div class="exp-list">
      <div class="exp-item">
        <div class="exp-meta">
          <div class="exp-date">Dec 2025 – Jun 2026</div>
          <div class="exp-company">TU Wien · IFT</div>
        </div>
        <div>
          <div class="exp-title">Robotics Research Intern</div>
          <div class="exp-location">📍 Vienna, Austria</div>
          <div class="exp-body">
            <ul>
              <li>Designed modular ROS 2 nodes enabling autonomous capabilities for the GigaBot AMR platform</li>
              <li>Developed stereo vision pipeline: camera calibration, image stitching (RANSAC), depth maps, and 3D point clouds</li>
              <li>Implemented SLAM (SLAM Toolbox, ORB-SLAM3) and EKF-based sensor fusion for robust localization</li>
              <li>Configured Nav2 autonomous navigation stack with custom costmaps and behaviour trees</li>
              <li>Built and validated a high-fidelity Gazebo Ignition digital twin of the IFT TEC-Lab</li>
              <li>Integrated 5G connectivity module for real-time teleoperation and M2M communication</li>
            </ul>
          </div>
          <div class="exp-tags">
            <span class="tag">ROS 2</span><span class="tag">SLAM</span><span class="tag">Nav2</span><span class="tag">OpenCV</span><span class="tag">Gazebo</span><span class="tag">5G</span><span class="tag">Python</span><span class="tag">SolidWorks</span>
          </div>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-meta">
          <div class="exp-date">Dec 2023 – Aug 2024</div>
          <div class="exp-company">Cardoo</div>
        </div>
        <div>
          <div class="exp-title">Embedded Software Engineer</div>
          <div class="exp-location">📍 Cairo, Egypt</div>
          <div class="exp-body">
            <ul>
              <li>Developed embedded firmware for microcontroller-based systems in C/C++</li>
              <li>Integrated sensors, actuators, and peripheral devices for seamless system operation</li>
              <li>Implemented and debugged CAN, UART, and I2C communication protocols</li>
            </ul>
          </div>
          <div class="exp-tags">
            <span class="tag">C/C++</span><span class="tag">STM32</span><span class="tag">CAN</span><span class="tag">UART</span><span class="tag">I2C</span><span class="tag">Embedded C</span>
          </div>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-meta">
          <div class="exp-date">Jun 2022 – Nov 2023</div>
          <div class="exp-company">Elsewedy Electric</div>
        </div>
        <div>
          <div class="exp-title">Planning Engineer</div>
          <div class="exp-location">📍 Cairo, Egypt</div>
          <div class="exp-body">
            Engineering planning and project coordination at one of Egypt's largest industrial electrical manufacturing groups.
          </div>
          <div class="exp-tags">
            <span class="tag">Project Planning</span><span class="tag">Industrial</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-inner">
    <div class="section-label">Portfolio</div>
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-icon">🤖</div>
        <div class="project-title">GigaBot WH-AMR</div>
        <div class="project-desc">5G-enabled Autonomous Mobile Robot for factory automation at TU Wien IFT, built on the DMG MORI WH-AMR 10 platform with NVIDIA Jetson Thor. Full-stack ROS 2 development, SLAM, Nav2, and stereo vision.</div>
        <div class="project-tech">
          <span class="tech-tag">ROS 2</span><span class="tech-tag">Nav2</span><span class="tech-tag">5G</span><span class="tech-tag">SLAM</span><span class="tech-tag">Gazebo</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">🧭</div>
        <div class="project-title">Autonomous Maze-Solving Robot</div>
        <div class="project-desc">Designed and programmed a robot to autonomously navigate and solve mazes using ultrasonic sensors for obstacle detection and real-time path decision-making.</div>
        <div class="project-tech">
          <span class="tech-tag">Embedded C</span><span class="tech-tag">Ultrasonic</span><span class="tech-tag">Microcontroller</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">🔒</div>
        <div class="project-title">Electronic Door Lock System</div>
        <div class="project-desc">Secure embedded access control system featuring keypad input, EEPROM-stored credentials, and multi-attempt lockout logic.</div>
        <div class="project-tech">
          <span class="tech-tag">C</span><span class="tech-tag">EEPROM</span><span class="tech-tag">ARM Cortex</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">🌡️</div>
        <div class="project-title">Temperature-Based Speed Control</div>
        <div class="project-desc">Closed-loop fan speed controller using temperature sensor feedback and PWM output — an embedded control system demonstrating real-time PID implementation.</div>
        <div class="project-tech">
          <span class="tech-tag">PWM</span><span class="tech-tag">ADC</span><span class="tech-tag">STM32</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">📏</div>
        <div class="project-title">Distance Measurement Device</div>
        <div class="project-desc">Precision ultrasonic distance measurement system with LCD display and configurable alert thresholds for industrial proximity sensing applications.</div>
        <div class="project-tech">
          <span class="tech-tag">Ultrasonic</span><span class="tech-tag">LCD</span><span class="tech-tag">Embedded C</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">⚙️</div>
        <div class="project-title">Industrial Automation & Classical Control</div>
        <div class="project-desc">Modeled and simulated industrial automation processes using MATLAB/Simulink with Stateflow logic — including PID tuning and Model-in-the-Loop (MIL) validation.</div>
        <div class="project-tech">
          <span class="tech-tag">MATLAB</span><span class="tech-tag">Simulink</span><span class="tech-tag">Stateflow</span><span class="tech-tag">MIL</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GIGABOT DEEP DIVE -->
<section id="gigabot">
  <div class="section-inner">
    <div class="section-label">Featured Project</div>
    <h2>GigaBot — Autonomous Mobile Robot</h2>
    <div class="gigabot-inner" style="grid-template-columns: 1fr; max-width: 780px;">
      <div>
        <div class="highlight-box">
          <strong>What it is:</strong> The GigaBot is a 5G-enabled Autonomous Mobile Robot (AMR) built on the DMG MORI WH-AMR 10 platform, developed at TU Wien IFT in collaboration with DMG MORI, PHINE-TECH, and NVIDIA. It runs on an NVIDIA Jetson Thor onboard compute module and operates over a private 5G campus network — designed to automate material handling, tool delivery, and inspection tasks in live manufacturing environments without rebuilding existing production lines.
        </div>
        <div class="highlight-box">
          <strong>My contributions:</strong> Built the full stereo vision pipeline (camera calibration, RANSAC-based image stitching, depth maps, 3D point cloud generation), designed the mechanical camera mount in SolidWorks, developed the containerized ROS 2 software stack, created a high-fidelity Gazebo Ignition digital twin of the IFT lab, and implemented SLAM and Nav2 autonomous navigation with 5G-connected teleoperation.
        </div>
        <div class="highlight-box">
          <strong>Key technologies:</strong> ROS 2 Humble · Nav2 · SLAM Toolbox · ORB-SLAM3 · OpenCV · Gazebo Ignition · Docker · NVIDIA Jetson · 5G SA private network · SolidWorks · Python · EKF sensor fusion
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-inner">
    <div class="section-label">Technical Profile</div>
    <h2>Skills</h2>
    <div class="skills-grid">
      <div class="skill-group">
        <div class="skill-group-label">Programming</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">C / C++</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:92%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Python</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:85%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Embedded C</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:90%"></div></div></div>
          <div class="skill-row"><span class="skill-name">MATLAB</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:78%"></div></div></div>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Robotics & Autonomy</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">ROS 2</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:88%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Nav2</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:80%"></div></div></div>
          <div class="skill-row"><span class="skill-name">SLAM</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:78%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Gazebo</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:82%"></div></div></div>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Computer Vision</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">OpenCV</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:82%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Stereo Calibration</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:85%"></div></div></div>
          <div class="skill-row"><span class="skill-name">3D Point Clouds</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:80%"></div></div></div>
          <div class="skill-row"><span class="skill-name">RANSAC</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:75%"></div></div></div>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Embedded Systems</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">ARM Cortex / STM32</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:88%"></div></div></div>
          <div class="skill-row"><span class="skill-name">RTOS (OSEK)</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:80%"></div></div></div>
          <div class="skill-row"><span class="skill-name">CAN / UART / I2C</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:85%"></div></div></div>
          <div class="skill-row"><span class="skill-name">HIL / SIL / MIL</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:78%"></div></div></div>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Design & Simulation</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">SolidWorks</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:80%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Simulink / Stateflow</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:78%"></div></div></div>
          <div class="skill-row"><span class="skill-name">PCB Design</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:70%"></div></div></div>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Platforms & Other</div>
        <div class="skill-list">
          <div class="skill-row"><span class="skill-name">NVIDIA Jetson</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:75%"></div></div></div>
          <div class="skill-row"><span class="skill-name">5G / M2M</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:70%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Machine Learning</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:68%"></div></div></div>
          <div class="skill-row"><span class="skill-name">Docker / Git</span><div class="skill-bar-wrap"><div class="skill-bar" style="width:80%"></div></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- COVER LETTER -->
<section id="cover">
  <div class="section-inner">
    <div class="section-label">Application Material</div>
    <h2>Cover Letter</h2>
    <div class="letter-wrap">
      <div class="letter-header">
        <div class="letter-name">Abdelrhman Mabrouk</div>
        <div class="letter-contact">
          Abdelrhmanmabrouk11@gmail.com &nbsp;·&nbsp; (+43) 690 20102304<br>
          1120 Vienna, Austria &nbsp;·&nbsp; linkedin.com/in/abdelrhman-ahmed-8837681b9
        </div>
      </div>
      <div class="letter-body">
        <p>Dear Hiring Manager,</p>
        <p>
          I am a Mechatronics Engineer currently completing a Research Internship at the <strong>Institute for Production Engineering and Photonic Technologies (IFT), TU Wien</strong>, where I work on the <strong>GigaBot</strong> — a 5G-enabled autonomous mobile robot built on the DMG MORI WH-AMR 10 platform, developed in collaboration with DMG MORI, PHINE-TECH, and NVIDIA. I am simultaneously enrolled in the <strong>Master's programme in Autonomous Vehicle Engineering</strong> at the University of Naples Federico II, and I am eager to bring my combined experience in robotics software, computer vision, and embedded systems to a forward-thinking engineering team.
        </p>
        <p>
          Over the past six months at TU Wien I have built a full <strong>stereo vision pipeline</strong> (camera calibration, RANSAC-based image stitching, SGBM depth maps, and 3D point cloud generation in ROS 2), designed a custom <strong>SolidWorks camera mount</strong>, created a high-fidelity <strong>Gazebo Ignition digital twin</strong> of the IFT manufacturing lab, and implemented <strong>SLAM and Nav2 autonomous navigation</strong> on the GigaBot platform. Working hands-on with the NVIDIA Jetson Thor and a private 5G campus network has given me direct exposure to edge AI compute and industrial-grade connectivity requirements.
        </p>
        <p>
          Prior to this, as an <strong>Embedded Software Engineer at Cardoo</strong> I developed firmware for STM32-based systems in C/C++, integrating sensors and debugging CAN, UART, and I2C protocols at the hardware level. That foundation now informs how I approach full-system software architecture — from bare-metal microcontrollers through to ROS 2 node graphs and autonomous navigation stacks.
        </p>
        <p>
          I am detail-oriented, self-driven, and comfortable working in international, fast-moving engineering environments. I would welcome the opportunity to discuss how my background can contribute to your team.
        </p>
        <p>Thank you for your time and consideration.</p>
        <div class="letter-sign">Abdelrhman Mabrouk</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="section-label">Get in Touch</div>
    <h2>Contact</h2>
    <div class="contact-grid">
      <div class="contact-info">
        <div class="contact-row">
          <div class="contact-icon">✉</div>
          <div>
            <div class="contact-label">Email</div>
            <div class="contact-val"><a href="mailto:Abdelrhmanmabrouk11@gmail.com">Abdelrhmanmabrouk11@gmail.com</a></div>
          </div>
        </div>
        <div class="contact-row">
          <div class="contact-icon">📞</div>
          <div>
            <div class="contact-label">Phone</div>
            <div class="contact-val">(+43) 690 20102304</div>
          </div>
        </div>
        <div class="contact-row">
          <div class="contact-icon">📍</div>
          <div>
            <div class="contact-label">Location</div>
            <div class="contact-val">1120 Vienna, Austria</div>
          </div>
        </div>
        <div class="contact-row">
          <div class="contact-icon">🔗</div>
          <div>
            <div class="contact-label">LinkedIn</div>
            <div class="contact-val"><a href="https://www.linkedin.com/in/abdelrhman-ahmed-8837681b9" target="_blank">abdelrhman-ahmed-8837681b9</a></div>
          </div>
        </div>
      </div>
      <div class="contact-note">
        <h3>Open to Opportunities</h3>
        <p>
          Available from <strong>July 2026</strong> onwards. Interested in roles in autonomous robotics, embedded systems, ROS 2 development, and computer vision — ideally in Austria, Italy, or remote. Open to both industry positions and research-industry partnerships.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span class="footer-name">Abdelrhman Mabrouk</span>
  <span class="footer-copy">© 2026 · Mechatronics Engineer · Vienna, Austria</span>
</footer>

</body>
</html>
