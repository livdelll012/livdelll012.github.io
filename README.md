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
     A botanical academic palette drawn from ivy, matcha, and stone —
     with a dusty rose pulled directly from the regalia in the portrait.
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
    --muted:      #556149;   /* darkened from original for AA contrast on cream/foam */
    --gold:       #c7ad75;
    --rose:       #c98f86;   /* pulled from the graduation hood in the portrait */
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
    'data:image/jpeg;base64,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';
</script>
</body>
</html>
