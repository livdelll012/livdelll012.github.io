# liv-delgado-site
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Liv Delgado, MPH — Public Health Educator &amp; Policy Scholar</title>
<meta name="description" content="Liv Delgado, MPH is an Adjunct Professor of Health Policy at York College, CUNY, and a public health scholar working on health policy, infectious disease equity, and digital pedagogy." />
<meta name="author" content="Liv Delgado" />
<meta name="theme-color" content="#263b2a" />

<!-- Open Graph / social preview -->
<meta property="og:type" content="profile" />
<meta property="og:title" content="Liv Delgado, MPH — Public Health Educator & Policy Scholar" />
<meta property="og:description" content="Adjunct Professor of Health Policy at York College, CUNY. Working on health policy, infectious disease equity, digital pedagogy, and health justice." />
<meta property="og:image" content="portrait.jpg" />
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Liv Delgado, MPH" />
<meta name="twitter:description" content="Public health educator and scholar — health policy, infectious disease equity, digital pedagogy." />
<meta name="twitter:image" content="portrait.jpg" />

<!-- Favicon: simple ivy-on-foam monogram, no extra file needed -->
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Ccircle cx='32' cy='32' r='32' fill='%23eef4df'/%3E%3Ctext x='32' y='42' font-family='Georgia,serif' font-size='28' font-weight='700' fill='%23263b2a' text-anchor='middle'%3ELD%3C/text%3E%3C/svg%3E" />

<!-- Type system: Fraunces (display) + Source Serif 4 (reading) + Inter (UI) -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,600;9..144,700&family=Source+Serif+4:opsz,wght@8..60,400;8..60,500;8..60,600&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />

<!-- Structured data for search engines -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Liv Delgado",
  "honorificSuffix": "MPH",
  "jobTitle": "Adjunct Professor, Department of Health Professions",
  "worksFor": {
    "@type": "CollegeOrUniversity",
    "name": "York College, City University of New York"
  },
  "alumniOf": {
    "@type": "CollegeOrUniversity",
    "name": "Yale School of Public Health"
  },
  "email": "mailto:liv.delgado@aya.yale.edu",
  "sameAs": ["https://orcid.org/0009-0001-8448-7797"],
  "knowsAbout": ["Health Policy", "Infectious Disease Equity", "Disability Justice", "Digital Pedagogy", "Health Communication"]
}
</script>

<style>
  /* ============================================================
    
  TOKENS
     A botanical academic palette.
  
  ============================================================ */
  :root {
    --ivy:        #263b2a;
    --ivy2:       #3f5f42;
    --matcha:     #8da66b;
    --matcha2:    #c9d7ad;
    --foam:       #eef4df;
    --stone:      #d8d1bf;
    --stone2:     #b7ad99;
    --cream:      #fbf8ef;
    --paper:      #fffdf7;
    --ink:        #233124;
    --muted:      #556149;
    --gold:       #c7ad75;
    --rose:       #c98f86;
    --shadow:     rgba(35, 49, 36, .16);

    --font-display: "Fraunces", Georgia, serif;
    --font-body:    "Source Serif 4", Georgia, serif;
    --font-ui:      "Inter", Arial, sans-serif;
  }

  /* ============================================================
     RESET & BASE
  ============================================================ */
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font-body);
    color: var(--ink);
    line-height: 1.62;
    background:
      radial-gradient(circle at 18% 12%, rgba(141,166,107,.22), transparent 26%),
      radial-gradient(circle at 78% 8%, rgba(216,209,191,.55), transparent 28%),
      linear-gradient(135deg, #fbf8ef 0%, #eef4df 45%, #f7f2e6 100%);
    overflow-x: hidden;
  }

  body::before {
    content: "";
    position: fixed; inset: 0; z-index: -2;
    background-image:
      linear-gradient(90deg, rgba(38,59,42,.035) 1px, transparent 1px),
      linear-gradient(rgba(38,59,42,.035) 1px, transparent 1px);
    background-size: 42px 42px;
  }

  body::after {
    content: "";
    position: fixed; inset: 0; z-index: -1; pointer-events: none;
    background:
      radial-gradient(circle at 8% 78%, rgba(63,95,66,.18), transparent 18%),
      radial-gradient(circle at 92% 62%, rgba(199,173,117,.16), transparent 20%);
  }

  a { color: inherit; }
  img { max-width: 100%; display: block; }

  /* Visible keyboard focus everywhere */
  a:focus-visible,
  button:focus-visible {
    outline: 2px solid var(--ivy);
    outline-offset: 3px;
    border-radius: 4px;
  }

  /* Skip link for keyboard / screen-reader users */
  .skip-link {
    position: absolute;
    left: -999px;
    top: auto;
    background: var(--ivy);
    color: var(--paper);
    font-family: var(--font-ui);
    font-weight: 700;
    padding: 12px 18px;
    border-radius: 8px;
    z-index: 100;
  }
  .skip-link:focus {
    left: 20px;
    top: 20px;
  }

  section { scroll-margin-top: 96px; }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    * { animation-duration: .001ms !important; transition-duration: .001ms !important; }
  }

  /* ============================================================
     NAVIGATION
  ============================================================ */
  nav {
    position: sticky; top: 14px; z-index: 20;
    width: min(1180px, 92%);
    margin: 18px auto 0;
    padding: 14px 20px;
    display: flex; align-items: center; justify-content: space-between; gap: 18px;
    background: rgba(255,253,247,.8);
    border: 1px solid rgba(63,95,66,.25);
    border-radius: 999px;
    box-shadow: 0 16px 38px var(--shadow);
    backdrop-filter: blur(15px);
  }
  .brand {
    font-family: var(--font-display);
    font-weight: 700;
    color: var(--ivy);
    letter-spacing: .01em;
    font-size: 1.05rem;
    white-space: nowrap;
  }
  .nav-links { display: flex; gap: 4px; flex-wrap: wrap; justify-content: flex-end; }
  .nav-links a {
    font-family: var(--font-ui);
    text-decoration: none;
    font-size: .83rem;
    font-weight: 500;
    color: var(--muted);
    padding: 8px 12px;
    border-radius: 999px;
    transition: background .18s ease, color .18s ease;
  }
  .nav-links a:hover { background: var(--foam); color: var(--ivy); }

  /* ============================================================
     HERO
  ============================================================ */
  .hero {
    width: min(1180px, 92%);
    margin: 62px auto 34px;
    display: grid;
    grid-template-columns: 1.05fr .95fr;
    gap: 42px;
    align-items: center;
  }

  .eyebrow {
    display: inline-flex; gap: 10px; align-items: center;
    font-family: var(--font-ui);
    font-size: .78rem; letter-spacing: .12em; text-transform: uppercase;
    color: var(--ivy);
    background: rgba(238,244,223,.86);
    border: 1px solid rgba(141,166,107,.42);
    border-radius: 999px;
    padding: 8px 13px;
    margin-bottom: 19px;
  }
  .eyebrow i {
    width: 10px; height: 10px; border-radius: 50%;
    background: var(--matcha);
    box-shadow: 0 0 0 7px rgba(141,166,107,.18);
  }

  h1 {
    font-family: var(--font-display);
    font-weight: 600;
    font-size: clamp(2.9rem, 6.6vw, 6.4rem);
    line-height: .92;
    letter-spacing: -.03em;
    color: var(--ivy);
  }

  /* Signature element: a ribbon accent echoing the graduation hood in the portrait */
  .regalia-accent {
    width: 68px; height: 4px; border-radius: 999px;
    margin: 18px 0 20px;
    background: linear-gradient(90deg, var(--ivy2), var(--rose) 55%, var(--gold));
  }

  .role-line {
    font-family: var(--font-ui);
    font-weight: 600;
    font-size: 1.02rem;
    color: var(--ivy2);
    margin-bottom: 14px;
  }
  .role-line span { color: var(--muted); font-weight: 400; }

  .lede { font-size: 1.18rem; color: var(--muted); max-width: 680px; }

  .actions { display: flex; gap: 12px; flex-wrap: wrap; margin-top: 26px; }
  .button {
    display: inline-block; text-decoration: none;
    font-family: var(--font-ui); font-weight: 700; font-size: .9rem;
    padding: 13px 20px; border-radius: 999px;
    transition: transform .18s ease, box-shadow .18s ease;
  }
  .primary { background: var(--ivy); color: var(--paper); }
  .secondary { border: 1px solid rgba(38,59,42,.25); background: rgba(255,253,247,.58); color: var(--ivy); }
  .button:hover { transform: translateY(-2px); box-shadow: 0 13px 25px rgba(35,49,36,.16); }

  /* Portrait panel */
  .portrait-panel {
    position: relative;
    min-height: 560px;
    border-radius: 42px;
    padding: 22px;
    background: linear-gradient(145deg, rgba(216,209,191,.7), rgba(238,244,223,.8));
    box-shadow: 0 24px 70px var(--shadow);
    border: 1px solid rgba(63,95,66,.25);
    overflow: hidden;
  }
  .portrait-panel::before {
    content: "";
    position: absolute; inset: 15px;
    border-radius: 32px;
    border: 1px solid rgba(255,253,247,.7);
    pointer-events: none;
  }
  .portrait {
    width: 100%; height: 485px;
    object-fit: cover; object-position: 50% 22%;
    border-radius: 30px; display: block;
    filter: saturate(.97) contrast(.99);
  }
  .immuno-orbit {
    position: absolute; right: -65px; top: -65px;
    width: 220px; height: 220px;
    border: 1px solid rgba(63,95,66,.22);
    border-radius: 50%;
  }
  .immuno-orbit::before,
  .immuno-orbit::after {
    content: ""; position: absolute; border-radius: 50%;
    background: rgba(141,166,107,.35);
    border: 2px solid rgba(63,95,66,.28);
  }
  .immuno-orbit::before { width: 52px; height: 52px; left: 22px; bottom: 30px; }
  .immuno-orbit::after  { width: 30px; height: 30px; right: 42px; top: 40px; }

  /* ============================================================
     SECTIONS
  ============================================================ */
  section {
    width: min(1180px, 92%);
    margin: 0 auto 30px;
    padding: 42px;
    background: rgba(255,253,247,.78);
    border: 1px solid rgba(63,95,66,.18);
    border-radius: 34px;
    box-shadow: 0 18px 46px rgba(35,49,36,.09);
  }
  .section-head {
    display: flex; align-items: end; justify-content: space-between; gap: 22px;
    margin-bottom: 24px;
    border-bottom: 1px solid rgba(63,95,66,.18);
    padding-bottom: 18px;
  }
  h2 {
    font-family: var(--font-display);
    font-weight: 600;
    font-size: clamp(1.8rem, 4vw, 2.9rem);
    color: var(--ivy);
    letter-spacing: -.02em;
    line-height: 1.05;
  }
  .kicker {
    font-family: var(--font-ui);
    text-transform: uppercase; letter-spacing: .12em;
    color: var(--ivy2); font-weight: 700; font-size: .75rem;
    margin-bottom: 8px;
  }

  .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; }
  .two { grid-template-columns: repeat(2, 1fr); }

  .card {
    background: linear-gradient(180deg, rgba(255,253,247,.9), rgba(238,244,223,.6));
    border: 1px solid rgba(141,166,107,.26);
    border-radius: 26px;
    padding: 22px;
    min-height: 170px;
  }
  .card h3 { font-family: var(--font-display); font-weight: 600; color: var(--ivy); font-size: 1.16rem; margin-bottom: 9px; }
  .card p, .card li { color: var(--muted); font-size: .98rem; }
  .card ul { padding-left: 18px; }

  .timeline { display: grid; gap: 14px; }
  .item {
    display: grid; grid-template-columns: 130px 1fr; gap: 18px;
    padding: 18px; border-radius: 24px;
    background: rgba(238,244,223,.48);
    border: 1px solid rgba(141,166,107,.22);
  }
  .item .year { font-family: var(--font-ui); font-weight: 800; color: var(--ivy2); }
  .item strong { font-family: var(--font-display); font-weight: 600; color: var(--ivy); font-size: 1.02rem; }

  .honor-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 14px; }
  .honor {
    display: flex; flex-direction: column; gap: 4px;
    padding: 16px 18px; border-radius: 20px;
    background: rgba(238,244,223,.42);
    border: 1px solid rgba(141,166,107,.22);
  }
  .honor-year {
    font-family: var(--font-ui); font-weight: 800; font-size: .72rem;
    letter-spacing: .08em; text-transform: uppercase;
    color: var(--ivy2);
  }
  .honor strong { font-family: var(--font-display); font-weight: 600; color: var(--ivy); font-size: 1rem; }
  .honor .org { font-family: var(--font-ui); color: var(--muted); font-size: .85rem; }

  .pub-list { display: grid; gap: 16px; }
  .pub {
    padding: 22px; border-radius: 26px;
    background: rgba(255,253,247,.82);
    border: 1px solid rgba(63,95,66,.2);
    position: relative; overflow: hidden;
  }
  .pub::before {
    content: ""; position: absolute; left: 0; top: 0; bottom: 0; width: 8px;
    background: linear-gradient(var(--matcha), var(--rose));
  }
  .pub h3 { font-family: var(--font-display); font-weight: 600; color: var(--ivy); font-size: 1.1rem; margin-bottom: 7px; }
  .pub p { color: var(--muted); font-family: var(--font-ui); font-size: .93rem; }

  .tag {
    display: inline-block;
    font-family: var(--font-ui); font-size: .72rem; font-weight: 700;
    text-transform: uppercase; letter-spacing: .09em;
    color: var(--ivy);
    background: var(--foam);
    border: 1px solid rgba(141,166,107,.35);
    border-radius: 999px;
    padding: 6px 10px; margin-top: 12px; margin-right: 6px;
  }

  .quote {
    font-family: var(--font-display);
    font-weight: 500;
    font-size: 1.5rem;
    color: var(--ivy);
    max-width: 920px; line-height: 1.35;
  }

  footer {
    width: min(1180px, 92%);
    margin: 0 auto 36px;
    padding: 28px;
    color: var(--muted);
    font-family: var(--font-ui);
    font-size: .88rem;
    text-align: center;
  }

  /* ============================================================
     RESPONSIVE
  ============================================================ */
  @media (max-width: 850px) {
    nav { border-radius: 26px; align-items: flex-start; flex-direction: column; }
    .nav-links { justify-content: flex-start; }
    .hero, .grid, .two, .honor-grid { grid-template-columns: 1fr; }
    .portrait-panel { min-height: auto; }
    .portrait { height: 420px; }
    .item { grid-template-columns: 1fr; }
    section { padding: 28px; }
  }

  /* ============================================================
     PRINT — for CV files, tenure binders, etc.
  ============================================================ */
  @media print {
    body { background: #fff; }
    body::before, body::after { display: none; }
    nav, .actions, .immuno-orbit { display: none; }
    section {
      box-shadow: none; border: none; background: #fff;
      padding: 0; margin: 0 0 24px; break-inside: avoid;
    }
    .portrait-panel { box-shadow: none; }
    a { text-decoration: underline; }
  }
</style>
</head>
<body>

<a class="skip-link" href="#main">Skip to content</a>

<nav aria-label="Primary">
  <div class="brand">Liv Delgado, MPH</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#teaching">Teaching</a>
    <a href="#research">Research</a>
    <a href="#publications">Publications</a>
    <a href="#honors">Honors</a>
    <a href="#speaking">Speaking</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<header class="hero">
  <div>
    <div class="eyebrow"><i></i> Adjunct Professor · Public Health Educator</div>
    <h1>Liv Delgado, MPH</h1>
    <div class="regalia-accent"></div>
    <p class="role-line">Department of Health Professions <span>· York College, CUNY</span></p>
    <p class="lede">Public health educator and scholar working across health policy, infectious disease equity, disability justice, digital pedagogy, and community-centered public health communication.</p>
    <div class="actions">
      <a class="button primary" href="#publications">View publications</a>
      <a class="button secondary" href="mailto:liv.delgado@aya.yale.edu">Email me</a>
    </div>
  </div>
  <div class="portrait-panel">
    <div class="immuno-orbit"></div>
    <img class="portrait" id="portrait-img" width="702" height="818" alt="Liv Delgado wearing academic regalia, standing in front of a Gothic stone building on a tree-lined walkway" />
  </div>
</header>

<main id="main">

<section id="about">
  <div class="section-head">
    <div>
      <div class="kicker">About</div>
      <h2>Scholarship with a public-facing purpose.</h2>
    </div>
  </div>
  <p class="quote">I bring together classroom teaching, accessible communication, and public health practice to help students understand how policy, power, place, and prevention shape community health.</p>
  <div class="grid two" style="margin-top:24px">
    <div class="card">
      <h3>Public health focus</h3>
      <p>Vaccine equity, infectious disease outcomes, rural health, disability justice, LGBTQ+ health, and health policy education.</p>
    </div>
    <div class="card">
      <h3>Teaching identity</h3>
      <p>Adjunct Professor in Health Professions teaching undergraduate health policy with a student-centered, applied, and creative approach.</p>
    </div>
  </div>

  <div class="kicker" style="margin-top:32px">Education</div>
  <div class="timeline">
    <div class="item">
      <div class="year">2023–2025</div>
      <div>
        <strong>Yale School of Public Health, Yale University</strong><br>
        MPH, Social and Behavioral Sciences, <em>summa cum laude</em> · New Haven, CT<br>
        Capstone: "Translating Global Health Frameworks and Tailoring the Community Health Worker (CHW) Model to Improve Vaccine Equity and Infectious Disease Outcomes in Rural Appalachia."
      </div>
    </div>
    <div class="item">
      <div class="year">2025</div>
      <div>
        <strong>Poorvu Center for Teaching and Learning, Yale Graduate School of Arts and Sciences</strong><br>
        Certificate in Public Communication · New Haven, CT
      </div>
    </div>
    <div class="item">
      <div class="year">2022</div>
      <div>
        <strong>Magdalen College, University of Oxford</strong><br>
        Oxford Consortium for Human Rights Scholar · Oxford, England
      </div>
    </div>
    <div class="item">
      <div class="year">2019–2023</div>
      <div>
        <strong>College of Health Professions, Sacred Heart University</strong><br>
        B.S., Health Science, Healthcare Administration Track, <em>magna cum laude</em> · Fairfield, CT<br>
        Minors in Women's, Gender, &amp; Sexuality Studies; Human Rights &amp; Social Justice; and Management. Dean's List, 2019–2023.<br>
        Capstone: "The Role of Doulaship in Addressing Maternal Mortality in the United States."
      </div>
    </div>
  </div>
</section>

<section id="teaching">
  <div class="section-head">
    <div>
      <div class="kicker">Teaching</div>
      <h2>Courses, guest lectures, and pedagogy.</h2>
    </div>
  </div>
  <!--
    Draft teaching philosophy -- written from what's established elsewhere
    on this page (student-centered, applied, digital-pedagogy, equity-
    minded). Edit this to sound like you before publishing; a philosophy
    statement is one of the few places a reader expects your own voice.
  -->
  <p class="quote" style="margin-bottom:28px">I teach health policy as something students will use, not just study: real case material, tools they can carry into practice, and space for the students furthest from the center of the room — disabled, first-generation, working — to see their own communities in the material.</p>
  <div class="timeline">
    <div class="item">
      <div class="year">2026</div>
      <div><strong>Adjunct Professor, York College, City University of New York</strong><br>HS 302 Health Policy, Department of Health Professions.</div>
    </div>
    <div class="item">
      <div class="year">2025</div>
      <div><strong>Guest Teach-in Lecturer, Yale School of Public Health</strong><br>Bodies, Barriers, and Biopolitics: Disability Praxis in Public Health.</div>
    </div>
    <div class="item">
      <div class="year">2024</div>
      <div><strong>Guest Teach-in Lecturer, Yale School of Public Health</strong><br>Understanding Dynamics of Power and Social Change for Health Policy Reform.</div>
    </div>
    <div class="item">
      <div class="year">2024</div>
      <div><strong>Tutor, Yale School of Public Health</strong><br>Health Disparities by Race &amp; Social Class; Social Justice &amp; Health Equity.</div>
    </div>
  </div>
</section>

<section id="research">
  <div class="section-head">
    <div>
      <div class="kicker">Research</div>
      <h2>Current areas of inquiry.</h2>
    </div>
  </div>
  <div class="grid two">
    <div class="card">
      <h3>Infectious disease prevention</h3>
      <p>Rural vaccine equity, community health worker models, airborne disease prevention, and public health communication around prevention practices.</p>
    </div>
    <div class="card">
      <h3>Digital health and pedagogy</h3>
      <p>Gamified learning, digital interventions, adolescent chronic disease management, and interactive tools for health policy education.</p>
    </div>
    <div class="card">
      <h3>Health equity and justice</h3>
      <p>Disability justice, LGBTQ+ public health, maternal health, menstrual equity, and the structural determinants of health.</p>
    </div>
    <div class="card">
      <h3>Methods and tools</h3>
      <p>Scoping reviews, public-facing scholarship, curriculum design, HTML/CSS/JavaScript educational projects, R, SAS, SPSS, REDCap, and Qualtrics.</p>
    </div>
  </div>
</section>

<section id="publications">
  <div class="section-head">
    <div>
      <div class="kicker">Publications</div>
      <h2>Publications and scholarly contributions.</h2>
    </div>
  </div>
  <div class="pub-list">
    <article class="pub">
      <h3>Points for Persistence: A Scoping Review of Game-Based Interventions for Pediatric Medication Adherence</h3>
      <p>Delgado, L. ResearchGate.</p>
      <span class="tag">Medication adherence</span><span class="tag">Pediatric chronic disease</span><span class="tag">Game-based interventions</span>
    </article>
    <article class="pub">
      <h3>Addressing Period Poverty: The Cost of Menstruating in America and the Ethical Responsibility to Provide Free Menstrual Care</h3>
      <p>Tabor, J., &amp; Delgado, L. (2022). Academic Festival.</p>
      <span class="tag">Menstrual equity</span><span class="tag">Ethics</span>
    </article>
    <article class="pub">
      <h3>The Sociocultural Determinants of Health and Wellness for Two-Spirit Indigenous North American Populations</h3>
      <p>Delgado, L. (2021). DigitalCommons@SHU.</p>
      <span class="tag">Health equity</span><span class="tag">Indigenous health</span>
    </article>
    <article class="pub">
      <h3>Integrated Social Work Practice</h3>
      <p>Student contributor for Cross-Denny, B. (2023). Cognella Academic Publishing. Chapters 15, 22, 24.</p>
      <span class="tag">Contributorship</span>
    </article>
    <article class="pub">
      <h3>Global Health Foundations: Principles and Applications</h3>
      <p>Student contributor for Yale Global Health Faculty Working Group EPH-595 syllabus.</p>
      <span class="tag">Curriculum</span><span class="tag">Global health</span>
    </article>
  </div>
</section>

<section id="honors">
  <div class="section-head">
    <div>
      <div class="kicker">Honors</div>
      <h2>Honors &amp; awards.</h2>
    </div>
  </div>
  <div class="honor-grid">
    <div class="honor"><div class="honor-year">2024</div><strong>YSPH Summer Fellowship Award</strong><span class="org">Yale School of Public Health</span></div>
    <div class="honor"><div class="honor-year">2023</div><strong>Dorothy Horstmann Scholar</strong><span class="org">Yale School of Public Health</span></div>
    <div class="honor"><div class="honor-year">2023</div><strong>Pioneer Pride Award</strong><span class="org">Sacred Heart University, Office for Inclusive Excellence</span></div>
    <div class="honor"><div class="honor-year">2023</div><strong>Nomination, John Croffy Outstanding Leader Award</strong><span class="org">Sacred Heart University</span></div>
    <div class="honor"><div class="honor-year">2023</div><strong>Best Capstone Paper</strong><span class="org">Sacred Heart University, College of Health Professions</span></div>
    <div class="honor"><div class="honor-year">2022</div><strong>Annual Student Scholarship</strong><span class="org">Triangle Community Center</span></div>
    <div class="honor"><div class="honor-year">2022</div><strong>Dean's Prize</strong><span class="org">Sacred Heart University Academic Festival</span></div>
    <div class="honor"><div class="honor-year">2022</div><strong>Honorable Mention, Best Multidisciplinary Research</strong><span class="org">Sacred Heart University Academic Festival</span></div>
    <div class="honor"><div class="honor-year">2022</div><strong>Honorable Mention, Most Scholarly Impact</strong><span class="org">Sacred Heart University Academic Festival</span></div>
    <div class="honor"><div class="honor-year">2021</div><strong>Nomination, Junior Pioneer Leader Award</strong><span class="org">Sacred Heart University</span></div>
    <div class="honor"><div class="honor-year">2021</div><strong>Top Capstone Presenter, Cohort II</strong><span class="org">General Intelligences</span></div>
  </div>
</section>

<section id="speaking">
  <div class="section-head">
    <div>
      <div class="kicker">Speaking</div>
      <h2>Invited speaking engagements &amp; presentations.</h2>
    </div>
  </div>

  <div class="kicker">Moderator</div>
  <div class="timeline" style="margin-bottom:28px">
    <div class="item"><div class="year">2025</div><div><strong>"Organizing Within and Beyond Academia with Yale Healthcare Workers"</strong><br>Health, Equity, and Anti-Colonial Liberation Coalition · New Haven, CT</div></div>
    <div class="item"><div class="year">2024</div><div><strong>"Do No Harm: LGBTQ+ Psychotherapy, Policy, and Politics with Dr. Judith Glassgold"</strong><br>LGBTQ+ Public Health Faculty Working Group · New Haven, CT</div></div>
    <div class="item"><div class="year">2024</div><div><strong>"Medical Student Burnout at the Intersections of Disability, Race, and Ethnicity"</strong><br>Disability Empowerment in Public Health at Yale · New Haven, CT</div></div>
    <div class="item"><div class="year">2023</div><div><strong>"National Council Strategy Session with Presidential Candidate Marianne Williamson"</strong><br>College Democrats of America · Remote</div></div>
    <div class="item"><div class="year">2023</div><div><strong>"College Democrats of Connecticut Strategy Session with Senate Majority Leader Bob Duff"</strong><br>College Democrats of Connecticut · Remote</div></div>
    <div class="item"><div class="year">2023</div><div><strong>"2023 National Council Chair Debate"</strong><br>College Democrats of America · Little Rock, AR</div></div>
    <div class="item"><div class="year">2022</div><div><strong>"Q&amp;A with CT Governor Ned Lamont"</strong><br>Sacred Heart University College Democrats · Fairfield, CT</div></div>
    <div class="item"><div class="year">2022</div><div><strong>"Democratic Candidates Panel with Tim Gavin and Sarah Keitt"</strong><br>Sacred Heart University Political Science &amp; Global Affairs Department · Fairfield, CT</div></div>
  </div>

  <div class="kicker">Guest Speakerships</div>
  <div class="timeline">
    <div class="item"><div class="year">2025</div><div><strong>"The Bold Beauty Project: Yale Edition, Visual-Audio Art Exhibition"</strong><br>Yale Program for Recovery and Community Health · New Haven, CT</div></div>
    <div class="item"><div class="year">2025</div><div><strong>"Leveraging Public Health Data for Disability Justice: Tools, Gaps, and Possibilities"</strong><br>Disability Empowerment in Public Health at Yale · New Haven, CT</div></div>
    <div class="item"><div class="year">2024</div><div><strong>"Words for Liberation: Poetry &amp; Dialogue on Anti-Blackness and Imperialism"</strong><br>Black @ YSPH Student Association; Health, Equity, and Anti-Colonial Liberation Coalition · New Haven, CT</div></div>
    <div class="item"><div class="year">2022</div><div><strong>"Art for Advocacy Exhibition"</strong><br>The Center for Family Justice · Bridgeport, CT</div></div>
    <div class="item"><div class="year">2022</div><div><strong>"Social Justice Week Microaggressions Panel"</strong><br>The Center for Family Justice · Bridgeport, CT</div></div>
    <div class="item"><div class="year">2021</div><div><strong>"Underrepresented Student Leaders Panel"</strong><br>Sacred Heart University, Office for Inclusive Excellence · Fairfield, CT</div></div>
  </div>
</section>

<section id="projects">
  <div class="section-head">
    <div>
      <div class="kicker">Projects</div>
      <h2>Educational technology and public health design.</h2>
    </div>
  </div>
  <div class="grid two">
    <div class="card">
      <h3>Global Health Policy Passport</h3>
      <p>Interactive health policy education platform using HTML5, CSS3, JavaScript, Web APIs, gamified modules, policy simulations, achievements, local storage, and certificate generation.</p>
    </div>
    <div class="card">
      <h3>Working papers</h3>
      <ul>
        <li>Digital Health Interventions for Endometriosis Education and Self-Management: A Systematic Review. <em>In progress.</em></li>
        <li>Normalized Noncompliance and Airborne Disease Prevention: The Continued Danger of "Droplet Dogma."</li>
      </ul>
    </div>
  </div>
</section>

<section id="contact">
  <div class="section-head">
    <div>
      <div class="kicker">Contact</div>
      <h2>Connect.</h2>
    </div>
  </div>
  <div class="grid">
    <div class="card">
      <h3>Email</h3>
      <p><a href="mailto:liv.delgado@aya.yale.edu">liv.delgado@aya.yale.edu</a><br><a href="mailto:livdelgado131@gmail.com">livdelgado131@gmail.com</a></p>
    </div>
    <div class="card">
      <h3>ORCID</h3>
      <p><a href="https://orcid.org/0009-0001-8448-7797" target="_blank" rel="noopener me">orcid.org/0009-0001-8448-7797</a></p>
    </div>
    <div class="card">
      <h3>Affiliations</h3>
      <p>American Public Health Association · Society for the Advancement of Chicanos/Hispanics and Native Americans in Science · Delta Alpha Pi</p>
    </div>
  </div>
</section>

</main>

<footer>© 2026 Liv Delgado, MPH</footer>

<!--
  Portrait is embedded as base64 below so the photo always displays,
  even if this file is opened, emailed, or hosted on its own without
  a sibling image file. When you move this to real hosting, you can
  swap this for a normal <img src="portrait.jpg"> and drop the JPEG
  in next to index.html instead -- slightly smaller page weight and
  the browser can cache the image separately.
-->

<script>
  document.getElementById('portrait-img').src =
   
