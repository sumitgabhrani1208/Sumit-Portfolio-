# Sumit-Portfolio-
Hello Guys ! This Is Sumit Gabhrani &amp; This is my Latest Portfolio with attached Resume 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sumit Gabhrani — Computer Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet"/>
<style>
  :root{
    --blueprint:  #0a1a2f;
    --blueprint2: #0d2038;
    --panel:      #0f2744;
    --line:       #2c527c;
    --paper:      #f2eee2;
    --ink:        #eaf1fb;
    --cyan:       #64d4f0;
    --amber:      #ffb454;
    --muted:      #7fa0c4;
    --muted-dark: #4d6b8f;
  }
  *,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--blueprint);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    overflow-x:hidden;
  }
  ::selection{background:var(--amber);color:var(--blueprint);}

  /* blueprint grid wash on the whole page */
  .grid-wash{
    position:fixed;inset:0;z-index:0;pointer-events:none;
    background-image:
      linear-gradient(rgba(100,212,240,.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(100,212,240,.06) 1px, transparent 1px);
    background-size:44px 44px;
  }

  section, header, footer{position:relative;z-index:1;}

  /* ---- corner registration marks, used on key panels ---- */
  .crop{position:relative;}
  .crop::before,.crop::after,
  .crop .c2, .crop .c3{
    content:'';position:absolute;width:16px;height:16px;
    border-color:var(--cyan);opacity:.55;
  }
  .crop::before{top:-1px;left:-1px;border-top:2px solid;border-left:2px solid;}
  .crop::after{top:-1px;right:-1px;border-top:2px solid;border-right:2px solid;}
  .crop .c2{bottom:-1px;left:-1px;border-bottom:2px solid;border-left:2px solid;}
  .crop .c3{bottom:-1px;right:-1px;border-bottom:2px solid;border-right:2px solid;}

  /* ---- NAV ---- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    display:flex;align-items:center;justify-content:space-between;
    padding:22px 56px;
    background:rgba(10,26,47,.82);
    backdrop-filter:blur(12px);
    border-bottom:1px solid var(--line);
  }
  .logo{
    font-family:'JetBrains Mono',monospace;
    font-size:.78rem;color:var(--cyan);letter-spacing:.08em;
    display:flex;align-items:center;gap:10px;
  }
  .logo b{color:var(--ink);font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:.95rem;letter-spacing:0;}
  .logo::before{content:'';width:8px;height:8px;background:var(--amber);display:inline-block;}
  nav{display:flex;gap:34px;}
  nav a{
    font-family:'JetBrains Mono',monospace;font-size:.68rem;
    color:var(--muted);text-decoration:none;letter-spacing:.1em;text-transform:uppercase;
    transition:color .2s;
  }
  nav a:hover{color:var(--cyan);}
  @media(max-width:860px){ nav{display:none;} header{padding:18px 24px;} }

  /* ---- section label (drawing-sheet style) ---- */
  .sheet-label{
    display:flex;align-items:baseline;gap:14px;margin-bottom:52px;
  }
  .sheet-num{
    font-family:'JetBrains Mono',monospace;font-size:.7rem;color:var(--amber);
    letter-spacing:.1em;
  }
  .sheet-title{font-family:'Space Grotesk',sans-serif;font-size:1.9rem;font-weight:700;color:var(--ink);}
  .sheet-rule{flex:1;height:1px;background:linear-gradient(to right,var(--line),transparent);}

  /* ================= HERO ================= */
  #hero{
    min-height:100vh;display:flex;align-items:center;
    padding:140px 56px 90px;perspective:1400px;
  }
  .hero-wrap{
    width:100%;max-width:1280px;margin:0 auto;
    display:grid;grid-template-columns:1.15fr .85fr;gap:64px;align-items:center;
  }
  .eyebrow{
    display:inline-flex;align-items:center;gap:8px;
    font-family:'JetBrains Mono',monospace;font-size:.68rem;color:var(--cyan);
    letter-spacing:.15em;text-transform:uppercase;
    border:1px solid rgba(100,212,240,.35);padding:6px 14px;border-radius:2px;
    margin-bottom:26px;
  }
  .eyebrow::before{content:'';width:6px;height:6px;background:var(--cyan);animation:blink 2s infinite;}
  @keyframes blink{0%,100%{opacity:1}50%{opacity:.25}}

  .hero h1{
    font-family:'Space Grotesk',sans-serif;font-weight:700;
    font-size:clamp(2.6rem,5.4vw,4.6rem);line-height:1.04;letter-spacing:-.01em;
    color:var(--ink);
  }
  .hero h1 span{color:var(--cyan);}
  .hero-role{
    margin-top:18px;font-family:'JetBrains Mono',monospace;font-size:.95rem;
    color:var(--muted);letter-spacing:.02em;
  }
  .hero-role b{color:var(--amber);font-weight:500;}
  .hero p.summary{
    margin-top:24px;max-width:520px;font-size:1rem;line-height:1.75;color:#b7c9de;
  }
  .hero-cta{margin-top:40px;display:flex;gap:16px;flex-wrap:wrap;}
  .btn{
    font-family:'JetBrains Mono',monospace;font-size:.72rem;letter-spacing:.1em;text-transform:uppercase;
    padding:15px 30px;border-radius:2px;text-decoration:none;transition:transform .18s ease, box-shadow .2s, background .2s, border-color .2s;
    display:inline-flex;align-items:center;gap:10px;
  }
  .btn-fill{background:var(--cyan);color:var(--blueprint);font-weight:600;}
  .btn-fill:hover{transform:translateY(-2px);box-shadow:0 10px 30px rgba(100,212,240,.25);}
  .btn-line{border:1px solid var(--line);color:var(--ink);}
  .btn-line:hover{border-color:var(--cyan);color:var(--cyan);transform:translateY(-2px);}

  /* dimension row under hero */
  .dim-row{margin-top:56px;display:flex;gap:0;}
  .dim{
    flex:1;padding-right:24px;border-right:1px dashed var(--line);
  }
  .dim:last-child{border-right:none;padding-right:0;}
  .dim + .dim{padding-left:24px;}
  .dim-num{font-family:'Space Grotesk',sans-serif;font-size:1.6rem;font-weight:700;color:var(--amber);}
  .dim-label{font-family:'JetBrains Mono',monospace;font-size:.62rem;color:var(--muted-dark);letter-spacing:.1em;text-transform:uppercase;margin-top:4px;}

  /* ---- 3D spec card, signature element ---- */
  .card-stage{perspective:1200px;}
  .spec-card{
    background:linear-gradient(160deg,var(--panel),var(--blueprint2));
    border:1px solid var(--line);
    border-radius:6px;
    padding:34px;
    transform-style:preserve-3d;
    transform:rotateX(6deg) rotateY(-10deg);
    transition:transform .12s ease-out, box-shadow .3s;
    box-shadow:0 30px 60px -20px rgba(0,0,0,.6), 0 0 0 1px rgba(100,212,240,.05);
    position:relative;
  }
  .spec-card::before{
    content:'DATASHEET · SG-01';
    position:absolute;top:14px;right:18px;
    font-family:'JetBrains Mono',monospace;font-size:.58rem;color:var(--muted-dark);letter-spacing:.08em;
  }
  .spec-avatar{
    width:74px;height:74px;border-radius:6px;
    background:linear-gradient(135deg,var(--cyan),#3a7dab);
    display:flex;align-items:center;justify-content:center;
    font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.7rem;color:var(--blueprint);
    transform:translateZ(40px);
    box-shadow:0 20px 30px -10px rgba(100,212,240,.4);
  }
  .spec-name{
    margin-top:20px;font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.3rem;
    transform:translateZ(30px);
  }
  .spec-role{
    font-family:'JetBrains Mono',monospace;font-size:.72rem;color:var(--cyan);margin-top:4px;
    transform:translateZ(30px);
  }
  .spec-table{
    margin-top:26px;display:flex;flex-direction:column;gap:0;
    transform:translateZ(20px);
  }
  .spec-row{
    display:flex;justify-content:space-between;padding:11px 0;
    border-top:1px solid rgba(100,212,240,.12);
    font-family:'JetBrains Mono',monospace;font-size:.72rem;
  }
  .spec-row span:first-child{color:var(--muted);}
  .spec-row span:last-child{color:var(--ink);}
  .spec-footer{
    margin-top:22px;padding-top:16px;border-top:1px dashed var(--line);
    font-family:'JetBrains Mono',monospace;font-size:.62rem;color:var(--muted-dark);
    display:flex;justify-content:space-between;transform:translateZ(15px);
  }
  @media(max-width:900px){
    .hero-wrap{grid-template-columns:1fr;}
    .dim-row{flex-wrap:wrap;gap:20px;}
    .dim{flex:1 1 40%;border-right:none;padding:0;}
  }

  /* ================= ABOUT ================= */
  #about{padding:130px 56px;background:var(--blueprint2);}
  .about-grid{max-width:1280px;margin:0 auto;display:grid;grid-template-columns:1.3fr 1fr;gap:70px;}
  .about-panel{
    background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:44px;
  }
  .about-panel p{font-size:1.02rem;line-height:1.8;color:#b7c9de;margin-bottom:18px;}
  .about-panel p strong{color:var(--ink);}
  .contact-strip{margin-top:30px;display:flex;flex-direction:column;gap:14px;}
  .contact-row{
    display:flex;align-items:center;gap:14px;font-family:'JetBrains Mono',monospace;font-size:.8rem;color:var(--muted);
  }
  .contact-row a{color:var(--cyan);text-decoration:none;}
  .contact-row a:hover{text-decoration:underline;}
  .contact-tag{
    width:30px;height:30px;flex-shrink:0;border:1px solid var(--line);border-radius:4px;
    display:flex;align-items:center;justify-content:center;font-size:.85rem;
  }

  .skills-panel{display:flex;flex-direction:column;gap:26px;}
  .skill-group-label{
    font-family:'JetBrains Mono',monospace;font-size:.65rem;color:var(--amber);
    letter-spacing:.14em;text-transform:uppercase;margin-bottom:12px;
    display:flex;align-items:center;gap:10px;
  }
  .skill-group-label::after{content:'';flex:1;height:1px;background:var(--line);}
  .chip-row{display:flex;flex-wrap:wrap;gap:8px;}
  .chip{
    padding:7px 13px;border:1px solid var(--line);border-radius:3px;
    font-family:'JetBrains Mono',monospace;font-size:.7rem;color:var(--ink);
    background:var(--blueprint);transition:border-color .2s,transform .15s,color .2s;
  }
  .chip:hover{border-color:var(--cyan);color:var(--cyan);transform:translateY(-2px);}

  /* ================= ACADEMICS ================= */
  #academics{padding:130px 56px;}
  .acad-wrap{max-width:1280px;margin:0 auto;}
  .acad-card{
    background:var(--panel);border:1px solid var(--line);border-radius:6px;
    padding:40px 44px;display:grid;grid-template-columns:auto 1fr auto;gap:36px;align-items:center;
    max-width:900px;position:relative;
  }
  .acad-icon{
    width:60px;height:60px;border-radius:6px;
    background:linear-gradient(135deg,var(--cyan),#2c527c);
    display:flex;align-items:center;justify-content:center;font-size:1.6rem;
    box-shadow:0 15px 30px -10px rgba(100,212,240,.35);
  }
  .acad-degree{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.2rem;}
  .acad-field{color:var(--cyan);font-family:'JetBrains Mono',monospace;font-size:.75rem;margin-top:6px;}
  .acad-meta{font-family:'JetBrains Mono',monospace;font-size:.72rem;color:var(--muted);margin-top:8px;}
  .acad-cgpa{
    text-align:center;padding:20px 30px;background:var(--blueprint);
    border:1px solid var(--line);border-radius:6px;position:relative;
  }
  .acad-cgpa::before{
    content:'';position:absolute;top:-14px;left:50%;transform:translateX(-50%);
    width:1px;height:12px;background:var(--muted-dark);
  }
  .cgpa-val{font-family:'Space Grotesk',sans-serif;font-size:2.1rem;font-weight:700;color:var(--amber);}
  .cgpa-lbl{font-family:'JetBrains Mono',monospace;font-size:.58rem;color:var(--muted-dark);letter-spacing:.1em;text-transform:uppercase;margin-top:2px;}

  .acad-note{
    margin-top:26px;max-width:900px;font-family:'JetBrains Mono',monospace;font-size:.72rem;
    color:var(--muted-dark);padding-top:18px;border-top:1px dashed var(--line);
  }
  @media(max-width:700px){ .acad-card{grid-template-columns:1fr;text-align:left;} .acad-cgpa{justify-self:start;} }

  /* ================= EXPERIENCE ================= */
  #experience{padding:130px 56px;background:var(--blueprint2);}
  .exp-wrap{max-width:1280px;margin:0 auto;}
  .exp-card{
    background:var(--panel);border:1px solid var(--line);border-radius:6px;
    padding:44px;position:relative;overflow:hidden;max-width:900px;
    transition:transform .2s,border-color .3s;
  }
  .exp-card:hover{transform:translateY(-4px);border-color:rgba(100,212,240,.35);}
  .exp-card::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:linear-gradient(to bottom,var(--cyan),var(--amber));}
  .exp-top{display:flex;justify-content:space-between;flex-wrap:wrap;gap:14px;margin-bottom:20px;}
  .exp-title{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.25rem;}
  .exp-co{color:var(--cyan);font-family:'JetBrains Mono',monospace;font-size:.8rem;margin-top:6px;}
  .exp-date{
    font-family:'JetBrains Mono',monospace;font-size:.68rem;color:var(--muted);
    border:1px solid var(--line);padding:6px 14px;border-radius:20px;height:fit-content;white-space:nowrap;
  }
  .exp-badge{
    display:inline-block;font-family:'JetBrains Mono',monospace;font-size:.6rem;letter-spacing:.1em;
    text-transform:uppercase;color:var(--cyan);border:1px solid rgba(100,212,240,.3);
    padding:4px 10px;border-radius:3px;margin-bottom:18px;
  }
  .exp-list{list-style:none;display:flex;flex-direction:column;gap:11px;}
  .exp-list li{font-size:.95rem;color:#b7c9de;line-height:1.65;padding-left:20px;position:relative;}
  .exp-list li::before{content:'▸';position:absolute;left:0;color:var(--amber);font-size:.8rem;}

  /* ================= PROJECTS ================= */
  #projects{padding:130px 56px;perspective:1200px;}
  .proj-wrap{max-width:1280px;margin:0 auto;}
  .proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:26px;}
  .proj-card{
    background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:32px;
    transform-style:preserve-3d;transition:transform .15s ease-out,border-color .3s,box-shadow .3s;
    position:relative;overflow:hidden;
  }
  .proj-card:hover{border-color:rgba(100,212,240,.35);box-shadow:0 25px 45px -20px rgba(0,0,0,.55);}
  .proj-icon{font-size:1.7rem;margin-bottom:18px;display:block;transform:translateZ(20px);}
  .proj-name{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.08rem;margin-bottom:10px;transform:translateZ(20px);}
  .proj-desc{font-size:.87rem;color:#a9bdd6;line-height:1.6;margin-bottom:20px;transform:translateZ(10px);}
  .proj-tags{display:flex;flex-wrap:wrap;gap:6px;transform:translateZ(10px);}
  .proj-tag{padding:4px 10px;border:1px solid var(--line);border-radius:3px;font-family:'JetBrains Mono',monospace;font-size:.6rem;color:var(--muted);}

  /* ================= CERTIFICATIONS ================= */
  #certs{padding:130px 56px;background:var(--blueprint2);}
  .cert-wrap{max-width:1280px;margin:0 auto;}
  .cert-card{
    display:flex;align-items:center;gap:24px;background:var(--panel);border:1px solid var(--line);
    border-radius:6px;padding:28px 34px;max-width:640px;transition:transform .2s,border-color .3s;
  }
  .cert-card:hover{transform:translateY(-3px);border-color:rgba(100,212,240,.35);}
  .cert-icon{
    width:52px;height:52px;flex-shrink:0;border-radius:6px;
    background:linear-gradient(135deg,rgba(100,212,240,.2),rgba(255,180,84,.15));
    border:1px solid rgba(100,212,240,.25);display:flex;align-items:center;justify-content:center;font-size:1.35rem;
  }
  .cert-name{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.02rem;margin-bottom:4px;}
  .cert-issuer{font-family:'JetBrains Mono',monospace;font-size:.7rem;color:var(--cyan);}
  .cert-year{font-family:'JetBrains Mono',monospace;font-size:.64rem;color:var(--muted-dark);margin-top:4px;}

  /* ================= CONTACT / CTA ================= */
  #contact{padding:140px 56px 100px;text-align:center;}
  .contact-panel{
    max-width:760px;margin:0 auto;background:var(--panel);border:1px solid var(--line);
    border-radius:10px;padding:70px 50px;position:relative;overflow:hidden;
  }
  .contact-panel::before{
    content:'';position:absolute;top:-100px;left:50%;transform:translateX(-50%);
    width:340px;height:340px;background:radial-gradient(circle,rgba(100,212,240,.14),transparent 70%);
  }
  .contact-heading{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:2.3rem;letter-spacing:-.01em;margin-bottom:16px;}
  .contact-sub{font-size:.95rem;color:var(--muted);line-height:1.7;margin-bottom:44px;max-width:480px;margin-left:auto;margin-right:auto;}
  .link-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
  .clink{
    display:flex;flex-direction:column;align-items:center;gap:10px;padding:24px 16px;
    background:var(--blueprint);border:1px solid var(--line);border-radius:6px;text-decoration:none;color:var(--ink);
    transition:border-color .2s,transform .15s,background .2s;
  }
  .clink:hover{border-color:var(--cyan);transform:translateY(-4px);background:rgba(100,212,240,.06);}
  .clink .icon{font-size:1.4rem;}
  .clink .label{font-family:'JetBrains Mono',monospace;font-size:.72rem;color:var(--ink);}
  .clink .sub{font-family:'JetBrains Mono',monospace;font-size:.58rem;color:var(--muted-dark);text-transform:uppercase;letter-spacing:.08em;}
  @media(max-width:640px){ .link-grid{grid-template-columns:1fr;} .contact-panel{padding:50px 26px;} }

  footer{
    text-align:center;padding:34px;border-top:1px solid var(--line);
    font-family:'JetBrains Mono',monospace;font-size:.65rem;color:var(--muted-dark);letter-spacing:.1em;
  }
  footer span{color:var(--cyan);}

  /* ---- brand logo icons ---- */
  .clink svg{width:22px;height:22px;}
  .contact-tag svg{width:15px;height:15px;}
  .cert-icon svg, .acad-icon svg{width:26px;height:26px;}

  /* ---- CONTACT FORM ---- */
  .form-wrap{max-width:760px;margin:56px auto 0;text-align:left;}
  .form-panel{
    background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:44px;
  }
  .form-panel h3{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:1.3rem;margin-bottom:6px;}
  .form-panel .form-sub{font-family:'JetBrains Mono',monospace;font-size:.7rem;color:var(--muted);margin-bottom:28px;}
  .form-row{display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-bottom:18px;}
  .field{display:flex;flex-direction:column;gap:8px;}
  .field.full{grid-column:1/-1;}
  .field label{
    font-family:'JetBrains Mono',monospace;font-size:.62rem;color:var(--muted);
    letter-spacing:.1em;text-transform:uppercase;
  }
  .field input, .field textarea{
    background:var(--blueprint);border:1px solid var(--line);border-radius:4px;
    padding:13px 14px;color:var(--ink);font-family:'Inter',sans-serif;font-size:.88rem;
    resize:vertical;transition:border-color .2s;
  }
  .field input:focus, .field textarea:focus{outline:none;border-color:var(--cyan);}
  .field textarea{min-height:110px;}
  .form-submit{
    margin-top:6px;font-family:'JetBrains Mono',monospace;font-size:.72rem;letter-spacing:.1em;
    text-transform:uppercase;padding:15px 32px;background:var(--cyan);color:var(--blueprint);
    font-weight:600;border:none;border-radius:2px;cursor:pointer;transition:transform .18s,box-shadow .2s;
  }
  .form-submit:hover{transform:translateY(-2px);box-shadow:0 10px 30px rgba(100,212,240,.25);}
  .form-note{margin-top:14px;font-family:'JetBrains Mono',monospace;font-size:.64rem;color:var(--muted-dark);}
  @media(max-width:600px){ .form-row{grid-template-columns:1fr;} .form-panel{padding:30px 22px;} }

  /* reveal on scroll */
  .reveal{opacity:0;transform:translateY(28px);transition:opacity .6s ease,transform .6s ease;}
  .reveal.visible{opacity:1;transform:none;}
  .r1{transition-delay:.08s;} .r2{transition-delay:.16s;} .r3{transition-delay:.24s;}

  @media(prefers-reduced-motion:reduce){
    *{animation-duration:.001ms !important;transition-duration:.001ms !important;}
  }

  @media(max-width:768px){
    #hero,#about,#academics,#experience,#projects,#certs,#contact{padding:90px 24px;}
    .about-grid{grid-template-columns:1fr;gap:40px;}
  }
</style>
</head>
<body>
<div class="grid-wash"></div>

<header>
  <div class="logo"><b>Sumit Gabhrani</b><span>/ REV.2026</span></div>
  <nav>
    <a href="#about">Profile</a>
    <a href="#academics">Academics</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- HERO -->
<section id="hero">
  <div class="hero-wrap">
    <div class="hero">
      <div class="eyebrow">Open to internships &amp; full-time roles</div>
      <h1>Sumit Gabhrani<br><span>builds engineered, reliable software.</span></h1>
      <p class="hero-role">Computer Engineering Diploma Student &nbsp;·&nbsp; <b>Web Developer</b></p>
      <p class="summary">
        6th-semester Computer Engineering student in Ahmedabad, Gujarat, carrying a CGPA of 8.50/10 and hands-on internship experience shipping responsive web interfaces at Brainy Beam Pvt. Ltd.
      </p>
      <div class="hero-cta">
        <a href="#contact" class="btn btn-fill">Get in Touch →</a>
        <a href="#projects" class="btn btn-line">View Work</a>
      </div>
      <div class="dim-row">
        <div class="dim"><div class="dim-num">8.50</div><div class="dim-label">Diploma CGPA</div></div>
        <div class="dim"><div class="dim-num">02</div><div class="dim-label">Experiences</div></div>
        <div class="dim"><div class="dim-num">06+</div><div class="dim-label">Technologies</div></div>
        <div class="dim"><div class="dim-num">B.Tech</div><div class="dim-label">IT · In Progress</div></div>
      </div>
    </div>

    <div class="card-stage">
      <div class="spec-card" id="specCard">
        <div class="spec-avatar">SG</div>
        <div class="spec-name">Sumit Gabhrani</div>
        <div class="spec-role">Software / Web Engineer</div>
        <div class="spec-table">
          <div class="spec-row"><span>Pursuing</span><span>B.Tech, IT</span></div>
          <div class="spec-row"><span>Institute</span><span>LDRP-ITR, Gandhinagar</span></div>
          <div class="spec-row"><span>Diploma CGPA</span><span>8.50 / 10.00</span></div>
          <div class="spec-row"><span>Location</span><span>Ahmedabad, GJ</span></div>
          <div class="spec-row"><span>Status</span><span style="color:var(--amber)">Available</span></div>
        </div>
        <div class="spec-footer"><span>ID: SG-ENGG-2026</span><span>REV. 03</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="acad-wrap">
    <div class="sheet-label reveal"><span class="sheet-num">SHEET 01</span><h2 class="sheet-title">Profile</h2><div class="sheet-rule"></div></div>
  </div>
  <div class="about-grid">
    <div class="about-panel crop reveal">
      <span class="c2"></span><span class="c3"></span>
      <p>I'm <strong>Sumit Gabhrani</strong>, a Computer Engineering diploma student currently in my 6th semester in Ahmedabad, Gujarat, focused on writing clean, dependable code and building interfaces people actually enjoy using.</p>
      <p>Alongside a CGPA of <strong>8.50/10</strong>, I've completed a Web Developer internship at <strong>Brainy Beam Pvt. Ltd.</strong>, where I helped build and debug responsive, production-facing web applications.</p>
      <p>I work well in teams, enjoy breaking down complex problems into manageable pieces, and I'm always picking up new frameworks and tools.</p>
      <div class="contact-strip">
        <div class="contact-row"><span class="contact-tag">✉</span><a href="mailto:sumitgabhrani@gmail.com">sumitgabhrani@gmail.com</a></div>
        <div class="contact-row"><span class="contact-tag">☎</span>+91 9023925860 &nbsp;/&nbsp; +91 7433011203</div>
        <div class="contact-row"><span class="contact-tag">⌖</span>Ahmedabad, Gujarat, India</div>
      </div>
    </div>

    <div class="skills-panel reveal r2">
      <div>
        <div class="skill-group-label">Languages</div>
        <div class="chip-row">
          <span class="chip">Python</span><span class="chip">Java</span><span class="chip">C</span><span class="chip">C++</span>
        </div>
      </div>
      <div>
        <div class="skill-group-label">Web Technologies</div>
        <div class="chip-row">
          <span class="chip">HTML5</span><span class="chip">CSS3</span><span class="chip">JavaScript</span>
        </div>
      </div>
      <div>
        <div class="skill-group-label">Fundamentals</div>
        <div class="chip-row">
          <span class="chip">OS Concepts</span><span class="chip">Networking</span><span class="chip">Databases</span><span class="chip">MS Office</span>
        </div>
      </div>
      <div>
        <div class="skill-group-label">Working Style</div>
        <div class="chip-row">
          <span class="chip">Project Management</span><span class="chip">Teamwork</span><span class="chip">Problem Solving</span><span class="chip">Fast Learner</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ACADEMICS -->
<section id="academics">
  <div class="acad-wrap">
    <div class="sheet-label reveal"><span class="sheet-num">SHEET 02</span><h2 class="sheet-title">Academics</h2><div class="sheet-rule"></div></div>
    <div class="acad-card reveal" style="margin-bottom:22px;">
      <div class="acad-icon">🎓</div>
      <div>
        <div class="acad-degree">B.Tech in Information Technology</div>
        <div class="acad-field">Currently Pursuing</div>
        <div class="acad-meta">LDRP Institute of Technology &amp; Research &nbsp;·&nbsp; Gandhinagar, Gujarat</div>
      </div>
      <div class="acad-cgpa">
        <div class="cgpa-val">In Progress</div>
        <div class="cgpa-lbl">Status</div>
      </div>
    </div>
    <div class="acad-card reveal r1">
      <div class="acad-icon">📐</div>
      <div>
        <div class="acad-degree">Diploma in Computer Engineering</div>
        <div class="acad-field">Completed</div>
        <div class="acad-meta">Ahmedabad, Gujarat</div>
      </div>
      <div class="acad-cgpa">
        <div class="cgpa-val">8.50</div>
        <div class="cgpa-lbl">CGPA / 10</div>
      </div>
    </div>
    <p class="acad-note">// Full academic transcript (10th, 12th / prior qualifications) available on request — happy to add specific board, school, and year details here if you share them.</p>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="exp-wrap">
    <div class="sheet-label reveal"><span class="sheet-num">SHEET 03</span><h2 class="sheet-title">Experience</h2><div class="sheet-rule"></div></div>
    <div class="exp-card reveal" style="margin-bottom:26px;">
      <div class="exp-top">
        <div><div class="exp-title">Web Developer Intern</div><div class="exp-co">Brainy Beam Pvt. Ltd.</div></div>
        <div class="exp-date">May 2025 – June 2025</div>
      </div>
      <div class="exp-badge">Internship</div>
      <ul class="exp-list">
        <li>Developed and maintained web applications using HTML, CSS, and JavaScript.</li>
        <li>Collaborated with the development team to design responsive, user-friendly interfaces.</li>
        <li>Assisted in debugging and testing to ensure functionality and performance.</li>
        <li>Gained hands-on exposure to real-world software development workflows and best practices.</li>
      </ul>
    </div>

    <div class="exp-card reveal r1">
      <div class="exp-top">
        <div><div class="exp-title">Social Media Handler &amp; Content Creator</div><div class="exp-co">Manish Luggage House · Bapunagar, Ahmedabad</div></div>
        <div class="exp-date">Ongoing</div>
      </div>
      <div class="exp-badge">Content &amp; Social</div>
      <ul class="exp-list">
        <li>Manage the store's social media presence across platforms, planning and posting content on a regular schedule.</li>
        <li>Shoot, edit, and publish photo and reel content to showcase products and drive engagement.</li>
        <li>Write captions and respond to customer queries and comments to build community and trust.</li>
        <li>Track post performance and adjust content style to grow reach and followers.</li>
      </ul>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="proj-wrap">
    <div class="sheet-label reveal"><span class="sheet-num">SHEET 04</span><h2 class="sheet-title">Projects</h2><div class="sheet-rule"></div></div>
    <div class="proj-grid">
      <div class="proj-card tilt reveal">
        <span class="proj-icon">🌐</span>
        <div class="proj-name">Internship Web Builds</div>
        <div class="proj-desc">Production-facing web applications built during my internship at Brainy Beam Pvt. Ltd., focused on responsive layout and interactive UI.</div>
        <div class="proj-tags"><span class="proj-tag">HTML5</span><span class="proj-tag">CSS3</span><span class="proj-tag">JavaScript</span></div>
      </div>
      <div class="proj-card tilt reveal r1">
        <span class="proj-icon">🧮</span>
        <div class="proj-name">Academic Programming Labs</div>
        <div class="proj-desc">Coursework projects exploring algorithms, data structures, and systems-level programming across multiple languages.</div>
        <div class="proj-tags"><span class="proj-tag">Python</span><span class="proj-tag">C</span><span class="proj-tag">C++</span><span class="proj-tag">Java</span></div>
      </div>
      <div class="proj-card tilt reveal r2">
        <span class="proj-icon">🚧</span>
        <div class="proj-name">In Development</div>
        <div class="proj-desc">Currently building out full-stack projects with modern frameworks to round out this section — check back soon.</div>
        <div class="proj-tags"><span class="proj-tag">In Progress</span></div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certs">
  <div class="cert-wrap">
    <div class="sheet-label reveal"><span class="sheet-num">SHEET 05</span><h2 class="sheet-title">Certifications</h2><div class="sheet-rule"></div></div>
    <div class="cert-card reveal">
      <div class="cert-icon">🏅</div>
      <div>
        <div class="cert-name">Web Developer Internship Certificate</div>
        <div class="cert-issuer">Brainy Beam Pvt. Ltd.</div>
        <div class="cert-year">Issued 2025</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-panel reveal">
    <div class="contact-heading">Let's build something.</div>
    <p class="contact-sub">Open to internships, freelance work, and full-time roles. Reach out on any channel below — I reply quickly.</p>
    <div class="link-grid">
      <a class="clink" href="mailto:sumitgabhrani@gmail.com">
        <span class="icon">✉️</span><span class="label">Email</span><span class="sub">sumitgabhrani@gmail.com</span>
      </a>
      <a class="clink" href="https://www.linkedin.com/in/sumit-gabhrani/" target="_blank" rel="noopener">
        <span class="icon">💼</span><span class="label">LinkedIn</span><span class="sub">sumit-gabhrani</span>
      </a>
      <a class="clink" href="https://www.instagram.com/thesumitgabhrani" target="_blank" rel="noopener">
        <span class="icon">📷</span><span class="label">Instagram</span><span class="sub">@thesumitgabhrani</span>
      </a>
    </div>
  </div>
</section>

<footer>Designed &amp; built by <span>Sumit Gabhrani</span> · 2026</footer>

<script>
  // 3D tilt on hero spec card
  const card = document.getElementById('specCard');
  const stage = card.parentElement;
  stage.addEventListener('mousemove', e=>{
    const r = stage.getBoundingClientRect();
    const px = (e.clientX - r.left)/r.width - .5;
    const py = (e.clientY - r.top)/r.height - .5;
    card.style.transform = `rotateX(${(-py*14+4).toFixed(2)}deg) rotateY(${(px*18-6).toFixed(2)}deg)`;
  });
  stage.addEventListener('mouseleave', ()=>{
    card.style.transform = 'rotateX(6deg) rotateY(-10deg)';
  });

  // subtle tilt on project cards
  document.querySelectorAll('.proj-card.tilt').forEach(el=>{
    el.addEventListener('mousemove', e=>{
      const r = el.getBoundingClientRect();
      const px = (e.clientX - r.left)/r.width - .5;
      const py = (e.clientY - r.top)/r.height - .5;
      el.style.transform = `rotateX(${(-py*8).toFixed(2)}deg) rotateY(${(px*10).toFixed(2)}deg) translateY(-4px)`;
    });
    el.addEventListener('mouseleave', ()=>{ el.style.transform = ''; });
  });

  // scroll reveal
  const els = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver(entries=>{
    entries.forEach(en=>{ if(en.isIntersecting){ en.target.classList.add('visible'); io.unobserve(en.target); } });
  }, {threshold:.12});
  els.forEach(el=>io.observe(el));
</script>
</body>
</html>
