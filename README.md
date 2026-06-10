<title>Urvi Upadhyay – Portfolio</title>

<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --primary: #b85c1a;
    --primary-dark: #8c4010;
    --accent: #e07b30;
    --blue: #3d7fc1;
    --blue-light: #ddeeff;
    --blue-mid: #b3d4f0;
    --orange-light: #fff3ea;
    --orange-mid: #fde0c4;
    --orange-border: #f5c49a;
    --white: #ffffff;
    --bg: #fdfaf7;
    --card-bg: #ffffff;
    --border: #f0e4d4;
    --text: #2d2015;
    --muted: #7a6a5a;
    --radius: 14px;
    --shadow: 0 2px 18px rgba(180,90,30,0.07);
  }
  body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--text); min-height: 100vh; }
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(255,255,255,0.97);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
    padding: 0 2.5rem;
    display: flex; align-items: center; justify-content: space-between;
    height: 58px;
  }
  .nav-brand { font-family: 'Playfair Display', serif; font-size: 1.05rem; color: var(--primary); font-weight: 700; letter-spacing: .01em; }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a { font-size: .85rem; color: var(--muted); text-decoration: none; font-weight: 500; transition: color .2s; }
  .nav-links a:hover { color: var(--primary); }
  #hero {
    position: relative;
    background: linear-gradient(120deg, #fff8f2 0%, #ffeedd 45%, #e8f4fd 100%);
    border-bottom: 2px solid var(--orange-border);
    min-height: 340px;
    display: flex; align-items: center;
    overflow: hidden;
    padding: 3.5rem 2.5rem;
  }
  #hero::after {
    content: '';
    position: absolute; right: -60px; top: -60px;
    width: 360px; height: 360px; border-radius: 50%;
    background: radial-gradient(circle, rgba(224,123,48,0.08) 0%, transparent 70%);
    pointer-events: none;
  }
  #hero::before {
    content: '';
    position: absolute; left: 40%; bottom: -40px;
    width: 280px; height: 280px; border-radius: 50%;
    background: radial-gradient(circle, rgba(61,127,193,0.06) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-content { position: relative; z-index: 1; display: flex; align-items: center; gap: 2.5rem; max-width: 940px; flex-wrap: wrap; }
  #hero-photo {
    width: 140px; height: 140px; border-radius: 50%;
    border: 4px solid var(--orange-border);
    object-fit: cover; flex-shrink: 0; display: block;
    box-shadow: 0 4px 20px rgba(180,90,30,0.15);
  }
  .hero-badge {
    display: inline-block;
    background: var(--orange-mid); border: 1px solid var(--orange-border);
    color: var(--primary); font-size: .75rem; padding: .28rem .8rem; border-radius: 20px;
    margin-bottom: .6rem; font-weight: 600; letter-spacing: .05em;
  }
  .hero-name { font-family: 'Playfair Display', serif; font-size: 2.3rem; font-weight: 700; color: var(--text); line-height: 1.15; margin-bottom: .4rem; }
  .hero-title { font-size: 1rem; color: var(--muted); margin-bottom: .9rem; }
  .hero-meta { display: flex; gap: 1.5rem; flex-wrap: wrap; }
  .hero-meta span { font-size: .82rem; color: var(--muted); display: flex; align-items: center; gap: .3rem; }
  .hero-meta svg { width:13px; height:13px; flex-shrink:0; color: var(--accent); }
  .hero-meta a { color: var(--blue); text-decoration: none; }
  .hero-meta a:hover { text-decoration: underline; }
  #stats-strip {
    background: var(--white);
    border-bottom: 1px solid var(--border);
    padding: 1.1rem 2.5rem;
    display: flex; gap: 0; max-width: 100%;
    overflow-x: auto;
  }
  .stat-item {
    flex: 1; min-width: 120px; text-align: center;
    padding: .6rem 1.5rem; border-right: 1px solid var(--border);
  }
  .stat-item:last-child { border-right: none; }
  .stat-num { font-family: 'Playfair Display', serif; font-size: 1.9rem; font-weight: 700; color: var(--primary); display: block; }
  .stat-label { font-size: .75rem; color: var(--muted); font-weight: 500; }
  main { max-width: 1120px; margin: 0 auto; padding: 2.5rem 1.5rem; display: grid; grid-template-columns: 275px 1fr; gap: 2rem; }
  .sidebar { display: flex; flex-direction: column; gap: 1.2rem; }
  .card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.2rem 1.25rem;
    box-shadow: var(--shadow);
  }
  .card-title {
    font-family: 'Playfair Display', serif;
    font-size: .9rem; font-weight: 700; color: var(--primary-dark);
    margin-bottom: .8rem; padding-bottom: .45rem;
    border-bottom: 2px solid var(--orange-mid);
    display: flex; align-items: center; gap: .45rem;
  }
  .info-row { display: flex; flex-direction: column; gap: .5rem; }
  .info-item { font-size: .83rem; color: var(--muted); }
  .info-item strong { display: block; color: var(--text); font-weight: 600; font-size: .82rem; margin-bottom: .05rem; }
  .tag-list { display: flex; flex-wrap: wrap; gap: .4rem; }
  .tag { background: var(--blue-light); color: var(--blue); font-size: .73rem; padding: .22rem .6rem; border-radius: 20px; font-weight: 600; border: 1px solid var(--blue-mid); }
  .tag.orange { background: var(--orange-light); color: var(--primary); border-color: var(--orange-border); }
  .content-area { display: flex; flex-direction: column; gap: 1.5rem; }
  .section-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.5rem 1.75rem;
    box-shadow: var(--shadow);
  }
  .section-head {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-weight: 700; color: var(--primary-dark);
    margin-bottom: 1.1rem; padding-bottom: .55rem;
    border-bottom: 2px solid var(--orange-mid);
    display: flex; align-items: center; gap: .55rem;
  }
  #bio-text { font-size: .91rem; line-height: 1.8; color: #3d2e1e; }
  .edu-item { display: flex; gap: 1rem; padding: .8rem 0; border-bottom: 1px solid var(--border); }
  .edu-item:last-child { border-bottom: none; }
  .edu-dot { width: 10px; height: 10px; border-radius: 50%; background: var(--accent); flex-shrink:0; margin-top:.35rem; }
  .edu-body h4 { font-size: .9rem; font-weight: 600; color: var(--text); }
  .edu-body p { font-size: .8rem; color: var(--muted); margin-top: .12rem; }
  .research-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px,1fr)); gap: .85rem; }
  .research-card { background: var(--orange-light); border: 1px solid var(--orange-border); border-radius: 10px; padding: .9rem 1rem; }
  .research-card h4 { font-size: .86rem; font-weight: 600; color: var(--primary-dark); margin-bottom: .25rem; }
  .research-card p { font-size: .78rem; color: var(--muted); }
  .research-badge { display: inline-block; background: var(--blue-light); color: var(--blue); border: 1px solid var(--blue-mid); font-size: .7rem; padding: .15rem .5rem; border-radius: 10px; font-weight: 600; margin-bottom: .3rem; }
  .pub-item { padding: .9rem 0; border-bottom: 1px solid var(--border); }
  .pub-item:last-child { border-bottom: none; }
  .pub-item h4 { font-size: .87rem; font-weight: 500; color: var(--text); line-height: 1.55; }
  .pub-item p { font-size: .78rem; color: var(--muted); margin-top: .25rem; }
  .books-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px,1fr)); gap: .85rem; }
  .book-card { background: linear-gradient(135deg, var(--orange-light) 0%, #fff8f2 100%); border: 1px solid var(--orange-border); border-radius: 10px; padding: 1rem; }
  .book-card h4 { font-size: .85rem; font-weight: 600; color: var(--primary-dark); margin-bottom: .25rem; line-height: 1.4; }
  .book-card p { font-size: .75rem; color: var(--muted); }
  .grant-item { display: flex; gap: 1rem; align-items: flex-start; padding: .8rem 0; border-bottom: 1px solid var(--border); }
  .grant-item:last-child { border-bottom: none; }
  .grant-amount { background: var(--primary); color: #fff; font-size: .78rem; font-weight: 700; padding: .3rem .65rem; border-radius: 8px; white-space: nowrap; flex-shrink:0; }
  .grant-body h4 { font-size: .87rem; font-weight: 600; color: var(--text); }
  .grant-body p { font-size: .78rem; color: var(--muted); margin-top: .1rem; }
  .event-item { display: flex; gap: .85rem; align-items: flex-start; padding: .75rem 0; border-bottom: 1px solid var(--border); }
  .event-item:last-child { border-bottom: none; }
  .event-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--blue); flex-shrink:0; margin-top: .35rem; }
  .event-body h4 { font-size: .87rem; font-weight: 500; color: var(--text); }
  .event-body p { font-size: .77rem; color: var(--muted); margin-top: .08rem; }
  .courses-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(190px,1fr)); gap: .75rem; }
  .course-card { background: var(--blue-light); border: 1px solid var(--blue-mid); border-radius: 9px; padding: .8rem 1rem; }
  .course-card h4 { font-size: .83rem; font-weight: 600; color: #1a4a7a; margin-bottom: .15rem; }
  .course-card p { font-size: .75rem; color: #3a6090; }
  @media (max-width: 768px) {
    main { grid-template-columns: 1fr; }
    nav { padding: 0 1rem; }
    .hero-name { font-size: 1.75rem; }
    #hero { padding: 2.5rem 1.5rem; }
    #stats-strip { padding: 1rem 1rem; }
  }
</style>

<nav>
  <div class="nav-brand">Urvi Upadhyay</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#education">Education</a>
    <a href="#research">Research</a>
    <a href="#publications">Publications</a>
    <a href="#grants">Grants</a>
    <a href="#courses">Courses</a>
  </div>
</nav>

<div id="hero">
  <div class="hero-content">
    <img id="hero-photo" src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?q=80&w=200&h=200&fit=crop" alt="Urvi Upadhyay">
    <div>
      <span class="hero-badge">Civil Engineering · Academia</span>
      <h1 class="hero-name">Urvi Upadhyay</h1>
      <p class="hero-title">Assistant Professor | Civil Engineering — Transportation, Structures & Sustainable Infrastructure<br>Parul University, Vadodara, Gujarat</p>
      <div class="hero-meta">
        <span>urvi.bhatt2@gmail.com</span>
        <span>+91 9428694361</span>
        <span><a href="https://linkedin.com/in/urviupadhyay" target="_blank">linkedin.com/in/urviupadhyay</a></span>
      </div>
    </div>
  </div>
</div>

<div id="stats-strip">
  <div class="stat-item"><span class="stat-num">13+</span><span class="stat-label">Years Experience</span></div>
  <div class="stat-item"><span class="stat-num">10+</span><span class="stat-label">Publications</span></div>
  <div class="stat-item"><span class="stat-num">3</span><span class="stat-label">Authored Books</span></div>
  <div class="stat-item"><span class="stat-num">₹7L+</span><span class="stat-label">Research Grants</span></div>
  <div class="stat-item"><span class="stat-num">8+</span><span class="stat-label">Projects Supervised</span></div>
  <div class="stat-item"><span class="stat-num">5+</span><span class="stat-label">FDPs Organised</span></div>
</div>

<main>
  <div class="sidebar">
    <div class="card">
      <div class="card-title">Prime Expertise</div>
      <div class="tag-list">
        <span class="tag orange">Transportation & Highway Engg</span>
        <span class="tag orange">Concrete Technology</span>
      </div>
    </div>
    
    <div class="card">
      <div class="card-title">Core Competencies</div>
      <div class="tag-list">
        <span class="tag">Structural Engg</span>
        <span class="tag">Public Health Engg</span>
        <span class="tag">OBE / NEP 2020</span>
        <span class="tag">Curriculum Design</span>
        <span class="tag">Research Supervision</span>
        <span class="tag">FDP Organisation</span>
        <span class="tag">Grant Writing</span>
        <span class="tag">Entrepreneurship</span>
        <span class="tag">Innovation Ambassador</span>
      </div>
    </div>

    <div class="card">
      <div class="card-title">Software & Tools</div>
      <div class="tag-list">
        <span class="tag">AutoCAD</span>
        <span class="tag">Revit</span>
        <span class="tag">BIM-360</span>
        <span class="tag">GIS</span>
        <span class="tag">Python</span>
        <span class="tag">IoT Tools</span>
        <span class="tag">AR/VR/MR</span>
      </div>
    </div>

    <div class="card">
      <div class="card-title">Contact Details</div>
      <div class="info-row">
        <div class="info-item"><strong>Location</strong>Vadodara, Gujarat, India</div>
        <div class="info-item"><strong>IAENG Member ID</strong>517724</div>
      </div>
    </div>
  </div>

  <div class="content-area">
    <div id="about" class="section-card">
      <div class="section-head">About Me</div>
      <p id="bio-text">Dedicated Civil Engineering academician with 13+ years of teaching, research, and academic leadership experience at undergraduate and postgraduate levels. Holds an M.E. in Transportation Engineering (Distinction, 7.85 CGPA), currently pursuing Ph.D. (2023–present), with a strong record of Scopus/Web of Science indexed publications, three authored textbooks, and government-funded research grants totalling over ₹6 Lakhs. Experienced in Outcome-Based Education (OBE), NEP 2020 implementation, curriculum development, laboratory management, and student mentorship. Passionate about fostering research, innovation, and entrepreneurship among civil engineering students.</p>
    </div>

    <div id="education" class="section-card">
      <div class="section-head">Education</div>
      <div class="edu-item">
        <div class="edu-dot"></div>
        <div class="edu-body">
          <h4>Ph.D. Civil Engineering — Pursuing</h4>
          <p>Parul University, Vadodara · 2023 – Present</p>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-dot"></div>
        <div class="edu-body">
          <h4>M.E. Civil – Transportation Engineering</h4>
          <p>Parul University, Vadodara · 2018–2020 · Distinction, 7.85 CGPA · Thesis: Capacity Evaluation of NH48</p>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-dot"></div>
        <div class="edu-body">
          <h4>B.E. Civil Engineering</h4>
          <p>M.S. University of Baroda, Vadodara · 2008–2012 · 60.05% · Elective: Concrete Technology</p>
        </div>
      </div>
    </div>

    <div id="research" class="section-card">
      <div class="section-head">Research Interests</div>
      <div class="research-grid">
        <div class="research-card"><span class="research-badge">Active</span><h4>Transportation & Highway Engineering</h4><p>Capacity analysis, LOS studies, traffic flow on national highways</p></div>
        <div class="research-card"><span class="research-badge">Active</span><h4>AI/ML in NDT Systems</h4><p>Real-time non-destructive testing for concrete using artificial intelligence & ML</p></div>
        <div class="research-card"><span class="research-badge">Active</span><h4>AR/VR/MR in AEC Industry</h4><p>Extended reality applications for Architecture, Engineering & Construction (Industry 4.0)</p></div>
      </div>
    </div>

    <div id="publications" class="section-card">
      <div class="section-head">Publications & Books</div>
      <div class="pub-item"><h4>2024 · AR/VR/MR a demand of AEC Industries 4.0 <span class="research-badge">Scopus</span></h4><p>AIP Conference Proceedings, 3107(1) · Upadhyay, U.</p></div>
      <div class="pub-item"><h4>2025 · Sustainable thermal performance of pulsating heat pipe using ZnO-ethanol nanofluid <span class="research-badge">Scopus</span></h4><p>Journal of Environmental Nanotechnology, 14(3) · Savalia et al.</p></div>
    </div>

    <div id="grants" class="section-card">
      <div class="section-head">Grants & Funded Projects</div>
      <div class="grant-item">
        <span class="grant-amount">₹3,50,000</span>
        <div class="grant-body">
          <h4>ATAL BASIC FDP Grant — AICTE, June 2025</h4>
          <p>Organiser & Coordinator · FDP: Shaping Infrastructure with Industry 5.0</p>
        </div>
      </div>
    </div>

    <div id="courses" class="section-card">
      <div class="section-head">Courses Taught</div>
      <div class="courses-grid">
        <div class="course-card"><h4>Transportation Engineering</h4><p>UG / PG</p></div>
        <div class="course-card"><h4>Highway Engineering</h4><p>UG / Diploma</p></div>
        <div class="course-card"><h4>Prestressed Concrete</h4><p>PG</p></div>
      </div>
    </div>
  </div>
</main>
