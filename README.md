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
  .nav-links { display: flex; gap: 1.5rem; }
  .nav-links a { font-size: .85rem; color: var(--muted); text-decoration: none; font-weight: 500; transition: color .2s; }
  .nav-links a:hover { color: var(--primary); }
  #hero {
    position: relative;
    background: linear-gradient(120deg, #fff8f2 0%, #ffeedd 45%, #e8f4fd 100%);
    border-bottom: 2px solid var(--orange-border);
    min-height: 300px;
    display: flex; align-items: center;
    overflow: hidden;
    padding: 3rem 2.5rem;
  }
  .hero-content { position: relative; z-index: 1; display: flex; align-items: center; gap: 2.5rem; max-width: 940px; flex-wrap: wrap; }
  .hero-badge {
    display: inline-block;
    background: var(--orange-mid); border: 1px solid var(--orange-border);
    color: var(--primary); font-size: .75rem; padding: .28rem .8rem; border-radius: 20px;
    margin-bottom: .6rem; font-weight: 600; letter-spacing: .05em;
  }
  .hero-name { font-family: 'Playfair Display', serif; font-size: 2.3rem; font-weight: 700; color: var(--text); line-height: 1.15; margin-bottom: .4rem; }
  .hero-title { font-size: 1rem; color: var(--muted); margin-bottom: .9rem; line-height: 1.5; }
  .hero-meta { display: flex; gap: 1.5rem; flex-wrap: wrap; }
  .hero-meta span { font-size: .82rem; color: var(--muted); display: flex; align-items: center; gap: .3rem; }
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
  main { max-width: 1160px; margin: 0 auto; padding: 2.5rem 1.5rem; display: grid; grid-template-columns: 290px 1fr; gap: 2rem; }
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
  }
  .info-row { display: flex; flex-direction: column; gap: .6rem; }
  .info-item { font-size: .83rem; color: var(--muted); line-height: 1.4; }
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
  }
  .bio-text { font-size: .91rem; line-height: 1.8; color: #3d2e1e; }
  .edu-item, .exp-item { padding: .9rem 0; border-bottom: 1px solid var(--border); }
  .edu-item:last-child, .exp-item:last-child { border-bottom: none; }
  .item-title-row { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: .5rem; }
  .item-title { font-size: .92rem; font-weight: 600; color: var(--text); }
  .item-meta { font-size: .8rem; color: var(--muted); margin-top: .15rem; }
  .item-desc { font-size: .83rem; color: #4a3e35; margin-top: .4rem; line-height: 1.5; padding-left: .5rem; }
  .research-grid, .courses-grid, .books-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px,1fr)); gap: .85rem; }
  .research-card, .course-card, .book-card { background: var(--orange-light); border: 1px solid var(--orange-border); border-radius: 10px; padding: .9rem 1rem; }
  .research-card h4, .course-card h4, .book-card h4 { font-size: .86rem; font-weight: 600; color: var(--primary-dark); margin-bottom: .25rem; }
  .research-card p, .course-card p, .book-card p { font-size: .78rem; color: var(--muted); line-height: 1.4; }
  .research-badge { display: inline-block; background: var(--blue-light); color: var(--blue); border: 1px solid var(--blue-mid); font-size: .7rem; padding: .15rem .5rem; border-radius: 10px; font-weight: 600; margin-bottom: .3rem; }
  .pub-item { padding: .9rem 0; border-bottom: 1px solid var(--border); }
  .pub-item:last-child { border-bottom: none; }
  .pub-item h4 { font-size: .87rem; font-weight: 500; color: var(--text); line-height: 1.55; }
  .pub-item p { font-size: .78rem; color: var(--muted); margin-top: .25rem; }
  .pub-link { color: var(--blue); text-decoration: none; }
  .pub-link:hover { text-decoration: underline; }
  .table-responsive { width: 100%; overflow-x: auto; margin-top: .5rem; }
  table { width: 100%; border-collapse: collapse; font-size: .82rem; text-align: left; }
  th { background: var(--orange-light); color: var(--primary-dark); font-weight: 600; padding: .6rem .8rem; border: 1px solid var(--border); }
  td { padding: .6rem .8rem; border: 1px solid var(--border); color: #4a3e35; line-height: 1.4; }
  tr:nth-child(even) { background-color: #fdfcfb; }
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
    <a href="#experience">Experience</a>
    <a href="#publications">Publications</a>
    <a href="#projects">Research & Consultancy</a>
    <a href="#events">Events</a>
  </div>
</nav>

<div id="hero">
  <div class="hero-content">
    <div>
      <span class="hero-badge">Civil Engineering · Academia & Industry</span>
      <h1 class="hero-name">Urvi Upadhyay</h1>
      <p class="hero-title">Assistant Professor | Civil Engineering — Transportation, Structures & Sustainable Infrastructure<br>Founder, Paramarsh Consultancy · Parul University, Vadodara</p>
      <div class="hero-meta">
        <span>📧 urvi.bhatt2@gmail.com</span>
        <span>📞 +91 9428694361</span>
        <span>🌐 <a href="https://linkedin.com/in/urviupadhyay" target="_blank">linkedin.com/in/urviupadhyay</a></span>
      </div>
    </div>
  </div>
</div>

<div id="stats-strip">
  <div class="stat-item"><span class="stat-num">13+</span><span class="stat-label">Years Experience</span></div>
  <div class="stat-item"><span class="stat-num">10</span><span class="stat-label">Indexed Publications</span></div>
  <div class="stat-item"><span class="stat-num">3</span><span class="stat-label">Authored Books</span></div>
  <div class="stat-item"><span class="stat-num">₹7.5L+</span><span class="stat-label">Total Grants & Funds</span></div>
  <div class="stat-item"><span class="stat-num">8+</span><span class="stat-label">Projects Supervised</span></div>
  <div class="stat-item"><span class="stat-num">5+</span><span class="stat-label">FDPs Organised</span></div>
</div>

<main>
  <div class="sidebar">
    <div class="card">
      <div class="card-title">Research Interests</div>
      <div class="tag-list">
        <span class="tag orange">Transportation Engineering</span>
        <span class="tag orange">Traffic Engineering</span>
        <span class="tag orange">Structural Health Monitoring</span>
        <span class="tag">Advanced & Sustainable Concrete</span>
        <span class="tag">Nanotechnology in Civil</span>
        <span class="tag">Infrastructure Sustainability</span>
      </div>
    </div>
    
    <div class="card">
      <div class="card-title">Core Competencies</div>
      <div class="tag-list">
        <span class="tag">Structural Design</span>
        <span class="tag">Public Health Engg</span>
        <span class="tag">OBE / NEP 2020</span>
        <span class="tag">Curriculum Design</span>
        <span class="tag">Research Supervision</span>
        <span class="tag">Grant Writing</span>
        <span class="tag">Entrepreneurship Coordination</span>
        <span class="tag">Innovation Ambassador</span>
      </div>
    </div>

    <div class="card">
      <div class="card-title">Software & Tools</div>
      <div class="tag-list">
        <span class="tag">AutoCAD</span>
        <span class="tag">REVIT</span>
        <span class="tag">BIM - 360</span>
        <span class="tag">MS Office</span>
      </div>
    </div>

    <div class="card">
      <div class="card-title">Personal Details</div>
      <div class="info-row">
        <div class="info-item"><strong>Date of Birth</strong>17/05/1988</div>
        <div class="info-item"><strong>Location</strong>Vadodara, Gujarat, India</div>
        <div class="info-item"><strong>IAENG Member ID</strong>517724 (Professional Member)</div>
      </div>
    </div>
  </div>

  <div class="content-area">
    <div id="about" class="section-card">
      <div class="section-head">About Me</div>
      <p class="bio-text">Dedicated Civil Engineering academician and entrepreneur with over 13 years of blend experience across teaching, advanced structural drafting, laboratory development, and research leadership. Currently pursuing a Ph.D. in Civil Engineering, holds an M.E. in Transportation Engineering with Distinction. Proven track record in securing government and institutional funding, including AICTE ATAL and Intramural R&D grants. Published author of three civil engineering textbooks and multiple indexed research papers. Active Institutional Innovation Ambassador, student mentor, and founder of Paramarsh Consultancy specializing in residential infrastructure and local municipal corporation liaisoning.</p>
    </div>

    <div id="education" class="section-card">
      <div class="section-head">Educational Qualifications</div>
      <div class="edu-item">
        <div class="item-title-row">
          <span class="item-title">Ph.D. Civil Engineering — Pursuing</span>
          <span class="item-meta">2023 – Present</span>
        </div>
        <div class="item-meta">Parul University, Vadodara</div>
      </div>
      <div class="edu-item">
        <div class="item-title-row">
          <span class="item-title">M.E. Civil – Transportation Engineering</span>
          <span class="item-meta">2018 – 2020</span>
        </div>
        <div class="item-meta">Parul University, Vadodara · <strong>Distinction (7.85 CGPA)</strong></div>
        <div class="item-desc">Thesis Title: <em>“Capacity Evaluation of NH48”</em></div>
      </div>
      <div class="edu-item">
        <div class="item-title-row">
          <span class="item-title">B.E. Civil Engineering</span>
          <span class="item-meta">2008 – 2012</span>
        </div>
        <div class="item-meta">The M. S. University of Baroda, Vadodara · <strong>60.05%</strong></div>
        <div class="item-desc">Elective Focus: Concrete Technology</div>
      </div>
      <div class="edu-item">
        <div class="item-title-row">
          <span class="item-title">Diploma in Civil Engineering</span>
          <span class="item-meta">2003 – 2006</span>
        </div>
        <div class="item-meta">The M. S. University of Baroda, Vadodara · <strong>64.70%</strong></div>
      </div>
    </div>

    <div id="experience" class="section-card">
      <div class="section-head">Professional Experience</div>
      
      <div class="exp-item">
        <div class="item-title-row">
          <span class="item-title">Founder</span>
          <span class="item-meta">Feb 2025 – Ongoing</span>
        </div>
        <div class="item-meta">Paramarsh Consultancy, Vadodara | <a href="https://sites.google.com/view/cparamarsh/home" target="_blank" class="pub-link">Consultancy Website</a></div>
        <div class="item-desc">Manages end-to-end statutory workflows, handling building layout permissions from the Vadodara Municipal Corporation (VMC). Oversees complete residential design, structural compliance, and execution tracking from initial excavation to structural finish.</div>
      </div>

      <div class="exp-item">
        <div class="item-title-row">
          <span class="item-title">Assistant Professor</span>
          <span class="item-meta">Dec 2022 – Apr 2026</span>
        </div>
        <div class="item-meta">Faculty of Technology and Engineering, Parul University</div>
        <div class="item-desc">Delivered advanced curriculum tracks for degree modules, guided postgraduate research theses, engineered updated course mapping models matching Outcome-Based Education frameworks, and executed departmental innovation activities.</div>
      </div>

      <div class="exp-item">
        <div class="item-title-row">
          <span class="item-title">Lecturer</span>
          <span class="item-meta">Aug 2014 – Dec 2022</span>
        </div>
        <div class="item-meta">Faculty of Technology and Engineering, Parul University</div>
        <div class="item-desc">Instructed fundamental engineering core courses across diploma and graduate divisions. Orchestrated physical setup profiles for core concrete technology, hydraulics, engineering mechanics, and highway testing labs. Managed student mentorship workflows.</div>
      </div>

      <div class="exp-item">
        <div class="item-title-row">
          <span class="item-title">Civil CAD Draftsman</span>
          <span class="item-meta">Aug 2007 – Feb 2011</span>
        </div>
        <div class="item-meta">Rumadri Associates</div>
        <div class="item-desc">Produced comprehensive structural working layouts for multiple complex residential setups. Conducted manual structural load computations alongside DOS-based analysis tools to generate detail reinforcement schematics.</div>
      </div>

      <div class="exp-item">
        <div class="item-title-row">
          <span class="item-title">Junior Civil Engineer</span>
          <span class="item-meta">Aug 2006 – Aug 2007</span>
        </div>
        <div class="item-meta">Kadam Environment Consultancy</div>
        <div class="item-desc">Drafted precise land-use and land-cover AutoCAD schematics for Environmental Impact Assessment (EIA) field datasets. Conducted daily structural site supervision for main commercial workspace developments in tandem with Architect Shital Kadam & Associates.</div>
      </div>
    </div>

    <div id="publications" class="section-card">
      <div class="section-head">Publications & Books</div>
      
      <h3 style="font-size:0.95rem; margin-bottom:0.5rem; color:var(--primary);">Authored Textbooks</h3>
      <div class="books-grid" style="margin-bottom:1.5rem;">
        <div class="book-card">
          <h4>Fundamental of Transportation Engineering</h4>
          <p>Published: Dec 2022</p>
        </div>
        <div class="book-card">
          <h4>Public Health Engineering</h4>
          <p>Published: Sep 2025</p>
        </div>
        <div class="book-card">
          <h4>Estimation, Costing and Valuation</h4>
          <p>Published: Oct 2025</p>
        </div>
      </div>

      <h3 style="font-size:0.95rem; margin-bottom:0.5rem; color:var(--primary);">Journal & Conference Research Papers</h3>
      
      <div class="pub-item">
        <h4>1. Sustainable thermal performance analysis of a pulsating heat pipe using zinc oxide-ethanol nanofluid <span class="research-badge">Scopus</span></h4>
        <p>Journal of Environmental Nanotechnology (2025), 14(3), 179-188 · Savalia, D. V., Anadani, P. A., Kokate, R., & Upadhyay, U. P. <a href="https://doi.org/10.13074/jent.2025.09.2531603" target="_blank" class="pub-link">[DOI Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>2. AR/VR/MR a demand of AEC industries 4.0 <span class="research-badge">Scopus</span></h4>
        <p>AIP Conference Proceedings (2024), 3107(1), 040003 · Upadhyay, U. <a href="https://doi.org/10.10374/sample" target="_blank" class="pub-link">[Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>3. Capacity analysis of traffic on NH48 Vadodara-Bharuch</h4>
        <p>IJTIMES (2020), 6(6), 46 · Upadhyay, U. <a href="https://www.ijtimes.com/index.php/ijtimes/article/view/214" target="_blank" class="pub-link">[Journal Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>4. The fencing in creek area face decaying and rusting problem combating it by using cathodic protection method</h4>
        <p>IJRASET (2020), 8(XII), 815-822 · Upadhyay, U.</p>
      </div>

      <div class="pub-item">
        <h4>5. Analyzing capacity and level of service of unsignalized roundabout</h4>
        <p>International Journal of Engineering Research and Reviews (2019), 7(2), 38-43 · Bhatt, U., Lalwani, V., & Sharma, A.</p>
      </div>

      <div class="pub-item">
        <h4>6. Use of recycled concrete aggregate</h4>
        <p>IJRDO - Journal of Mechanical and Civil Engineering (2015), 1(4), 86 · Upadhyay, U. <a href="https://doi.org/10.53555/mce.v1i8.1086" target="_blank" class="pub-link">[DOI Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>7. Engineering biomechanics of human motion</h4>
        <p>IJRDO - Journal of Mechanical and Civil Engineering (2015), 1(4), 88 · Upadhyay, U. <a href="https://doi.org/10.53555/mce.v1i4.581" target="_blank" class="pub-link">[DOI Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>8. Cooling by natural ventilation</h4>
        <p>IJRDO (2018), 4(1), 1 · Upadhyay, U. <a href="https://doi.org/10.53555/mce.v4i1.1789" target="_blank" class="pub-link">[DOI Link]</a></p>
      </div>

      <div class="pub-item">
        <h4>9. Modeling, simulation and optimization techniques in electrical discharge machining: A comprehensive review <span class="research-badge">Indexed</span></h4>
        <p>Pre-print Status · Patel, N. J., Shrivastava, S., Padhiyar, M., & Upadhyay, U.</p>
      </div>

      <div class="pub-item">
        <h4>10. Public transport status in rural area of Gujarat, Karjan <span class="research-badge">Indexed</span></h4>
        <p>Pre-print Status · Upadhyay, U., & Lalwani, V.</p>
      </div>
    </div>

    <div id="projects" class="section-card">
      <div class="section-head">Research Grants & Consultancy</div>
      
      <div class="table-responsive">
        <table>
          <thead>
            <tr>
              <th>Project Type & Title</th>
              <th>Funding Agency / Client</th>
              <th>Grant Value</th>
              <th>Duration / Status</th>
              <th>My Role</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>R&D Project:</strong> Development of Real-time Nondestructive Testing System for Concrete Using AI/ML</td>
              <td>Research and Development Cell (PU)</td>
              <td><strong>₹2,51,000</strong></td>
              <td>Aug 2025 · Completed</td>
              <td>Principal Investigator</td>
            </tr>
            <tr>
              <td><strong>Consultancy Work:</strong> Procuring Completion, Plinth Check, & Occupation Certificates</td>
              <td>Kuchh Chemical (VMC Authority boundary)</td>
              <td><strong>₹1,51,000</strong></td>
              <td>Aug 2025 – Apr 2026 · Completed</td>
              <td>Lead Civil Consultant</td>
            </tr>
            <tr>
              <td><strong>National FDP Grant:</strong> ATAL BASIC FDP Training Program</td>
              <td>AICTE, New Delhi</td>
              <td><strong>₹3,50,000</strong></td>
              <td>June 2025 · Completed</td>
              <td>Chief Coordinator</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

    <div id="events" class="section-card">
      <div class="section-head">Technical Events & Programs Organized</div>
      <div class="table-responsive">
        <table>
          <thead>
            <tr>
              <th>Event Description / Topic</th>
              <th>Venue / Institute</th>
              <th>Year</th>
              <th>Assigned Role</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>Faculty Coordinator Vadodara Hackathon 6.0</td><td>Parul University</td><td>2025</td><td>Chief Coordinator</td></tr>
            <tr><td>Organized ATAL FDP on Shaping Infrastructure with Industry 5.0</td><td>AICTE Sponsored</td><td>2025</td><td>Program Director</td></tr>
            <tr><td>Application of Python in Civil Engineering</td><td>Parul University</td><td>2024</td><td>Event Coordinator</td></tr>
            <tr><td>STTP on Water Reclamation</td><td>Parul University</td><td>2024</td><td>STTP Coordinator</td></tr>
            <tr><td>4 Days FDP on Application of IoT in Civil Engineering</td><td>Parul University</td><td>2023</td><td>Co-Coordinator</td></tr>
            <tr><td>National Startup Day Celebration Expert Talk Series</td><td>Parul University</td><td>2025</td><td>Event Chair</td></tr>
            <tr><td>Smart Structural Design with AutoCAD & Revit Structure</td><td>Parul University</td><td>2023</td><td>Technical Organizer</td></tr>
            <tr><td>“SketchUp” – A New Era of Drafting Startup</td><td>Parul University</td><td>2023</td><td>Expert Talk Convener</td></tr>
            <tr><td>Innovative Construction Chemistry (CEO Branco Buildsmart)</td><td>Parul University</td><td>2022</td><td>Coordinator</td></tr>
            <tr><td>Webinar: Design of R.C.C. Structure (Mr. B.P. Karamchandani)</td><td>Parul University</td><td>2022</td><td>Main Organizer</td></tr>
            <tr><td>World Water Day Celebration & Technical Training Outreach</td><td>Shankarpura Village School</td><td>2025</td><td>Community Liaison</td></tr>
            <tr><td>Earth Day Celebration Environmental Awareness Campaign</td><td>Shankarpura School</td><td>2024</td><td>Field Organizer</td></tr>
          </tbody>
        </table>
      </div>
    </div>

    <div id="academic-summary" class="section-card">
      <div class="section-head">Academic & Operational Extensions</div>
      <div class="research-grid">
        <div class="research-card">
          <h4>Laboratory Management</h4>
          <p>Supervised and organized testing frameworks for Engineering Mechanics, Concrete Technology, Surveying, and Highway Engineering labs.</p>
        </div>
        <div class="research-card">
          <h4>Student Innovation</h4>
          <p>Institutional Innovation Ambassador. Managed student registration setups for National Hackathons, Toycathons, and final tier presentation panels.</p>
        </div>
        <div class="research-card">
          <h4>Field Outreach</h4>
          <p>Organized experiential educational site transits to Bliss Darshanam project zones, Municipal Sewage Treatment Facilities, and local FabLabs.</p>
        </div>
      </div>
    </div>
  </div>
</main>
