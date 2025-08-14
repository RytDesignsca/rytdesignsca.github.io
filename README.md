
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0"/>
  <title>RYT DESIGNS | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@900;700;400&display=swap" rel="stylesheet">
  <link href="https://calendar.google.com/calendar/scheduling-button-script.css" rel="stylesheet">
  <script src="https://calendar.google.com/calendar/scheduling-button-script.js" async></script>
  <style>
    :root {
      --main-bg: #181c28;
      --panel-bg: #22243a;
      --neon: #23f0ff;
      --accent: #ffe066;
      --white: #fff;
      --hot: #ff4d97;
      --input-bg: #191a1f;
      --form-glow: 0 0 34px #13fff5aa;
      --panel-radius: 15px;
    }
    html,body {
      background: var(--main-bg);
      color: var(--white);
      font-family: 'Montserrat', Arial, sans-serif;
      margin: 0; padding: 0;
      min-height: 100vh;
    }
    body { letter-spacing: .01em; }
    .nav {
      max-width:1280px;width:100vw;padding:26px 38px 26px 38px;margin:auto;
      display:flex;align-items:center;justify-content:space-between;
      background:transparent;
    }
    .logo { 
      font-size: 2.1rem;
      font-weight: 900;
      color: var(--neon);
      letter-spacing: -2px;
      filter: drop-shadow(0 0 13px var(--neon));
      user-select:none;cursor:pointer;
      text-shadow: 0 0 18px #8ff;
    }
    .menu {
      display:flex;gap:34px;font-weight:700;font-size:1.13rem;user-select:none;
    }
    .menu a {
      color:var(--white);text-decoration:none;transition:.2s;padding:2px 10px;border-radius:6px;
    }
    .menu a.active,.menu a:hover { color:var(--neon); background:rgba(35,240,255,0.13);}
    @media(max-width:700px){ .nav {flex-direction:column;padding:13px 2vw;} .logo {font-size: 1.3rem;} .menu{gap:18px;}}

    .hero {
      text-align:center;margin-top:12px;margin-bottom:12px;
    }
    .hero-title {
      font-size: clamp(2.2rem,7vw,4.5rem);
      font-weight: 900;
      color: var(--neon);
      background: linear-gradient(90deg, #23f0ff 40%, #ffe066 95%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow:
        0 0 48px var(--neon),
        0 2px 8px #000f, 
        0 1px 1px #d9dcd6;
      filter: brightness(1.5) drop-shadow(0 0 22px #23f0ff);
      letter-spacing:0;
      animation: neonPulse 2.5s infinite alternate;
      margin-bottom: .5em;
      user-select:none;
      text-transform:uppercase;
    }
    @keyframes neonPulse {
      0% { filter: brightness(1.3) drop-shadow(0 0 18px #23f0ff);}
      100% { filter: brightness(1.8) drop-shadow(0 0 31px #ffe066);}
    }
    .hero-sub {
      font-size:1.26rem;font-weight:600;color:var(--accent);text-shadow: 0 1px 19px #ffe06644;
    }
    .gallerywrap {
      max-width: 1150px;
      margin:55px auto 38px auto;
    }
    .gallery-grid {
      display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
      gap:32px 22px;width:100%;
      margin:0 auto;
    }
    .gallery-card {
      background: #fff;
      border-radius: 13px;
      overflow: hidden;
      box-shadow: 0 7px 32px #181c2899;
      transition: transform .21s, box-shadow .23s;
      display: flex;
      flex-direction: column;
      align-items:center;
      cursor: pointer;
      position: relative;
      min-height: 224px;
    }
    .gallery-card:hover {
      transform: translateY(-9px) scale(1.04);
      box-shadow: 0 16px 43px #23f0ff33;
    }
    .gallery-card img {
      width:100%; display:block; min-height:210px;object-fit:cover;
      background: #e9f6f5;
      border-bottom: 2px solid var(--neon);
    }
    .gallery-card .caption {
      padding:12px 0 17px 0;font-size:1.13rem;font-weight:800;color:var(--main-bg);letter-spacing:.03em;text-align:center;text-shadow:0 1px 14px #ffe06655;
      width: 93%;
    }
    @media(max-width:650px){.gallery-grid{gap:13px 1vw;}.gallery-card{min-height:120px;}.gallery-card img{min-height:95px;}}

    .form-section {
      display: flex; flex-direction: column; align-items: center; margin-bottom:65px;
    }
    .form-panel {
      background: var(--panel-bg);
      border-radius: var(--panel-radius);
      box-shadow: var(--form-glow),0 6px 20px #000f;
      padding:36px 30px 19px 30px;
      max-width:400px; width:95vw; margin: 0 auto;
      animation: glowIn 1.3s;
      position:relative;
    }
    @keyframes glowIn {
      0% {filter: brightness(.6) blur(7px); opacity: .33;}
      100% {filter: none; opacity: 1;}
    }
    .project-inquiry-form label {
      font-size:1.03rem;font-weight:700;margin-top:1.09em;margin-bottom:7px;display:block;color:var(--accent);letter-spacing:0.04em;
    }
    .project-inquiry-form input, .project-inquiry-form textarea, .project-inquiry-form select {
      width:100%;margin-bottom:14px;border:none;border-radius:7px;
      background:var(--input-bg);color:#fff;font-size:1.08rem;
      padding:9px 11px;font-family:inherit;outline:none;transition:box-shadow .13s;
    }
    .project-inquiry-form input:focus,.project-inquiry-form textarea:focus{box-shadow:0 0 0 2px var(--neon) inset;}
    .project-inquiry-form textarea {min-height:66px;}
    .project-inquiry-form button {
      background: linear-gradient(90deg, var(--hot) 13%, var(--neon));
      color: #fff; border: none; border-radius:8px;
      padding:13px 0;font-size:1.17rem;width:100%;font-weight:800;
      margin-top:8px;transition:background .17s, filter .11s;
      box-shadow:0 3px 24px #23f0ff44;
      letter-spacing:.1em; cursor:pointer;
      filter: brightness(1.08);
    }
    .project-inquiry-form button:hover {
      background: linear-gradient(90deg, var(--neon) 20%, var(--hot));
      filter:brightness(1.15);
    }
    .form-success,.form-error {
      text-align:center;font-weight:800;font-size:1.05rem;padding:5px 0 7px 0;
    }
    .form-success{color:var(--neon);}
    .form-error{color:var(--hot);}
    .contact-or {text-align:center;margin:17px 0 9px 0;font-weight:700;color:var(--neon);}
    .form-panel .calendar-booking {display:flex;justify-content:center;margin-top:14px;margin-bottom:19px;}
    #gcal-button-container button, #gcal-button-container > div > button {
      font-size:1.10rem !important;
      padding:14px 31px !important;
      border-radius:10px !important;font-weight:900 !important;letter-spacing:0.09em !important;
      background:linear-gradient(90deg,#23f0ff 20%,#ffe066 99%)!important;color:#181c28!important;border:0!important;box-shadow:0 1px 9px #23f0ff44 !important;
      margin:auto !important;text-transform:uppercase;
    }
    .contact-info {
      color:var(--neon);margin:0.7em 0 0.3em 0;text-align:center;font-size: 1.09rem;
    }
    .social-row {
      display:flex; justify-content:center; gap:2.1em; margin-top:1.1em; font-weight:900; font-size:1.16rem; letter-spacing:.17em;
    }
    .social-row a { color: var(--accent); text-decoration:none;transition:color .19s; }
    .social-row a:hover { color:var(--hot);}
    footer {
      text-align:center; color:#bcccdc;padding:21px 0 15px 0;background:var(--panel-bg);font-size:1.08rem;margin-top:13vh;
    }
    footer a { color:var(--accent); font-weight:900; text-decoration:none;}
  </style>
</head>
<body>
  <nav class="nav">
    <div class="logo" onclick="window.scrollTo({top:0,behavior:'smooth'})">RYT DESIGNS</div>
    <div class="menu">
      <a href="#work" class="active">Work</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>
  <section class="hero">
    <div class="hero-title">Let's Make Something Cool.</div>
    <div class="hero-sub">Your vision, my creativity—custom work, always unique!</div>
  </section>
  <div class="gallerywrap" id="work">
    <div class="gallery-grid">
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Trip%20Itenirary%20.png" alt="Trip Itinerary"/>
        <div class="caption">Trip Itinerary</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Logo%204%20website.png" alt="Logo 4 website"/>
        <div class="caption">Logo 4 website</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Menu%204%20website.png" alt="Menu 4 website"/>
        <div class="caption">Menu 4 website</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Album%20cover.png" alt="Album Cover"/>
        <div class="caption">Album Cover</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/T-Shirt%20design.png" alt="T-Shirt Design"/>
        <div class="caption">T-Shirt Design</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Ryt%20Skin.png" alt="Branding"/>
        <div class="caption">Branding</div>
      </div>
      <div class="gallery-card">
        <img src="https://rytdesignsca.github.io/website%20prototype/Ryt%20Designs%20Poster.png" alt="Poster Design"/>
        <div class="caption">Poster Design</div>
      </div>
    </div>
  </div>
  <section id="about" style="max-width:580px;margin:64px auto 42px auto;text-align:center;color:var(--accent);font-size:1.17rem;line-height:1.7;">
    <b>
      Hey, I'm RYT—a teen designer and digital artist. <br>
      <span style="color:var(--neon)">Check my work. Hit up my form to collab. <br> Stay original, stay bold.</span>
    </b>
  </section>
  <section class="form-section" id="contact">
    <div class="form-panel">
      <form id="projectInquiryForm" class="project-inquiry-form" autocomplete="off" method="POST" action="https://formspree.io/f/mjkrwwpk">
        <div class="form-success" id="formSuccess" style="display:none;"></div>
        <div class="form-error" id="formError" style="display:none;"></div>
        <label for="name">Name *</label>
        <input type="text" name="name" placeholder="e.g. Jane Doe" required>
        <label for="email">Email *</label>
        <input type="email" name="email" placeholder="name@email.com" required>
        <label for="style">Project Style</label>
        <select name="style" required>
          <option value="">- Select -</option>
          <option>Modern & Minimalist</option>
          <option>Bold & Vibrant</option>
          <option>Classic & Elegant</option>
          <option>Fun & Playful</option>
          <option>Not sure / Surprise me</option>
        </select>
        <label for="vision">Tell me what you want</label>
        <textarea name="vision" required placeholder="Describe your vision/idea/project..."></textarea>
        <label for="requirements">Anything else?</label>
        <textarea name="requirements" placeholder="Colors, examples, logo ideas, must-haves..."></textarea>
        <button type="submit">Send Inquiry</button>
      </form>
      <div class="contact-or">or Book a 1-on-1 call now:</div>
      <div class="calendar-booking"><div id="gcal-button-container" style="width:100%;"></div></div>
      <div class="contact-info">
        <b>Phone:</b> +1 226-977-9311 <br>
        <b>Email:</b> <a href="mailto:rytdesignsca@gmail.com" style="color:var(--neon);text-decoration:underline;">rytdesignsca@gmail.com</a>
      </div>
      <div class="social-row">
        <a href="https://www.instagram.com/rytdesigns_/" target="_blank">Instagram</a>
        <a href="https://www.tiktok.com/@ryt.designs7" target="_blank">TikTok</a>
      </div>
    </div>
  </section>
  <footer>
    © 2025 RYT DESIGNS — All work original.
  </footer>
  <script>
    function navActive(){
      let y = window.scrollY || window.pageYOffset;
      let links = document.querySelectorAll('.menu a');
      let work = document.getElementById('work').offsetTop - 120;
      let about = document.getElementById('about').offsetTop - 120;
      let contact = document.getElementById('contact').offsetTop - 150;
      links.forEach(a=>a.classList.remove('active'));
      if(y<about) links[0].classList.add('active');
      else if(y<contact) links[1].classList.add('active');
      else links[2].classList.add('active');
    }
    window.addEventListener('scroll', navActive); navActive();

    document.addEventListener("DOMContentLoaded",function(){
      const form=document.getElementById('projectInquiryForm');
      const formSuccess=document.getElementById('formSuccess');
      const formError=document.getElementById('formError');
      if(form){
        form.addEventListener('submit',function(e){
          setTimeout(()=>{
            formSuccess.style.display='block';
            formSuccess.textContent="Thank you! I'll be in touch.";
            formError.style.display="none";
            form.reset();
          }, 300);
        });
      }
      function gcalBtnLoad() {
        var btnTarget=document.getElementById('gcal-button-container');
        if(btnTarget&&window.calendar&&window.calendar.schedulingButton){
          calendar.schedulingButton.load({
            url:'https://calendar.google.com/calendar/appointments/schedules/AcZssZ3VpIaEgD8-5JS2dBR-7XaOx9beJuvfUs5Fq7CtY0VZ1hQdcewcz0RyCSxQClVQWASiLuzz36AK?gv=true',
            color:'#23f0ff',label:'Book Now',target:btnTarget
          });
        } else setTimeout(gcalBtnLoad,400);
      }
      gcalBtnLoad();
    });
  </script>
</body>
</html>
