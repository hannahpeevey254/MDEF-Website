<div class="hero-wrapper" id="hero-wrapper" markdown="block">
<canvas id="grain-canvas"></canvas>

<div class="hero-nav">
<span class="logo">Hannah Peevey</span>
<div class="nav-links">
<a href="../term1/index.md" class="nav-pill">Term 1</a>
<a href="../term2/index.md" class="nav-pill">Term 2</a>
<a href="../term3/index.md" class="nav-pill active">Term 3</a>
<a href="../Personal Work/" class="nav-pill">Personal Work</a>
<a href="../about/" class="nav-pill nav-icon">About me</a>
<a href="../contact/" class="nav-pill nav-icon">Contact me</a>
</div>
</div>

<div class="hero-title">
<span class="title-line">PORTFOLIO</span>
<span class="title-line">WEBSITE</span>
</div>

<div class="tags-field" id="tags-field">
<div class="tag tag-outline tag-sm t1">ARCHITECT</div>
<div class="tag tag-filled tag-lg t2">HANNAH PEEVEY</div>
<div class="tag tag-outline tag-sm t3">3D</div>
<div class="tag tag-filled tag-xl t4">DESIGNER</div>
<div class="tag tag-outline tag-md t5">VIBE CODING</div>
<div class="tag tag-outline tag-sm t6">CONTACT</div>
<div class="tag tag-outline tag-md t7">MDEF</div>
<div class="tag tag-outline tag-sm t8">BCN</div>
<div class="tag tag-filled tag-lg t9">VISUAL ARTIST</div>
</div>

</div>

<style>
  /* Hide MkDocs default header on home page */
  .md-content__inner > h1 { display: none !important; }
  .md-content__inner { padding: 0 !important; margin: 0 !important; }
  .md-content { padding: 0 !important; }

  .hero-wrapper {
    position: relative;
    width: 100vw;
    left: 50%;
    transform: translateX(-50%);
    min-height: 100vh;
    background: #111111;
    overflow: hidden;
    font-family: 'Arial Black', 'Helvetica Neue', Arial, sans-serif;
    display: flex;
    flex-direction: column;
  }

  #grain-canvas {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 1;
    opacity: 0.55;
    mix-blend-mode: overlay;
  }

  .hero-wrapper::before,
  .hero-wrapper::after {
    content: '';
    position: absolute;
    border-radius: 50%;
    filter: blur(120px);
    z-index: 0;
  }
  .hero-wrapper::before {
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(180,220,0,0.18) 0%, transparent 70%);
    top: -100px; left: -100px;
  }
  .hero-wrapper::after {
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(80,160,80,0.12) 0%, transparent 70%);
    bottom: 0; right: 100px;
  }

  .hero-nav {
    position: relative;
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 24px 48px;
  }

  .hero-nav .logo {
    color: white !important;
    font-size: 28px;
    font-weight: 900;
    font-style: italic;
    letter-spacing: -1px;
    line-height: 1;
    user-select: none;
    font-family: serif;
  }

  .hero-nav .nav-links {
    display: flex !important;
    gap: 10px;
    align-items: center;
    list-style: none;
    margin: 0; padding: 0;
  }

  .hero-nav .nav-pill {
    display: inline-block !important;
    padding: 10px 22px;
    border-radius: 999px;
    border: 1.5px solid rgba(255,255,255,0.35);
    color: white !important;
    font-size: 14px;
    font-weight: 700;
    text-decoration: none !important;
    letter-spacing: 0.02em;
    transition: all 0.2s ease;
    background: transparent !important;
    cursor: pointer;
    font-family: 'Arial Black', sans-serif;
  }
  .hero-nav .nav-pill:hover {
    border-color: #d4f500 !important;
    color: #d4f500 !important;
    background: transparent !important;
  }
  .hero-nav .nav-pill.active {
    background: #d4f500 !important;
    border-color: #d4f500 !important;
    color: #111 !important;
  }
  .hero-nav .nav-pill.nav-icon { padding: 10px 16px; font-size: 16px; }

  .hero-title {
    position: relative;
    z-index: 5;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px 48px 0;
    line-height: 0.92;
    pointer-events: none;
  }

  .title-line {
    display: block;
    font-size: clamp(80px, 12vw, 160px);
    font-weight: 900;
    color: #d4f500;
    letter-spacing: -0.03em;
    text-transform: uppercase;
    font-family: 'Arial Black', 'Impact', 'Helvetica Neue', sans-serif;
    opacity: 0;
    transform: translateY(40px);
    animation: slideUp 0.7s cubic-bezier(0.22,1,0.36,1) forwards;
  }
  .title-line:nth-child(1) { animation-delay: 0.05s; }
  .title-line:nth-child(2) { animation-delay: 0.18s; }

  .tags-field {
    position: relative;
    z-index: 10;
    flex: 1;
    min-height: 320px;
    margin: 0 48px;
  }

  .tag {
    position: absolute;
    border-radius: 999px;
    font-weight: 900;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    white-space: nowrap;
    cursor: default;
    transition: transform 0.3s cubic-bezier(0.34,1.56,0.64,1), box-shadow 0.3s ease;
    user-select: none;
    opacity: 0;
    animation: popIn 0.5s cubic-bezier(0.34,1.56,0.64,1) forwards;
  }

  /* Position each tag individually since CSS custom properties aren't reliable here */
  .t1 { left: 5%;   top: 5%;  transform: rotate(-8deg); animation-delay: 0.40s; }
  .t2 { left: 28%;  top: 25%; transform: rotate(-4deg); animation-delay: 0.50s; }
  .t3 { left: 12%;  top: 50%; transform: rotate(5deg);  animation-delay: 0.55s; }
  .t4 { left: 48%;  top: 10%; transform: rotate(10deg); animation-delay: 0.62s; }
  .t5 { left: 70%;  top: 5%;  transform: rotate(-6deg); animation-delay: 0.68s; }
  .t6 { left: 32%;  top: 58%; transform: rotate(-12deg);animation-delay: 0.72s; }
  .t7 { left: 52%;  top: 52%; transform: rotate(3deg);  animation-delay: 0.78s; }
  .t8 { left: 76%;  top: 48%; transform: rotate(8deg);  animation-delay: 0.83s; }
  .t9 { left: 2%;   top: 65%; transform: rotate(6deg);  animation-delay: 0.88s; }

  .tag:hover { transform: rotate(0deg) scale(1.06) !important; z-index: 20; }

  .tag-filled {
    background: #d4f500;
    color: #111;
    box-shadow: 0 4px 32px rgba(212,245,0,0.25);
  }
  .tag-filled:hover { box-shadow: 0 8px 48px rgba(212,245,0,0.45); }

  .tag-outline {
    background: transparent;
    color: white;
    border: 1.5px solid rgba(255,255,255,0.5);
  }
  .tag-outline:hover { border-color: #d4f500 !important; color: #d4f500 !important; }

  .tag-sm  { font-size: 14px; padding: 12px 26px; }
  .tag-md  { font-size: 17px; padding: 14px 32px; }
  .tag-lg  { font-size: 20px; padding: 17px 38px; }
  .tag-xl  { font-size: 22px; padding: 18px 40px; }

  @keyframes slideUp {
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes popIn {
    to { opacity: 1; }
  }

  @media (max-width: 768px) {
    .hero-nav { padding: 18px 24px; flex-wrap: wrap; gap: 12px; }
    .hero-title { padding: 16px 24px 0; }
    .tags-field { margin: 0 24px; min-height: 400px; }
    .nav-links { gap: 6px; }
    .nav-pill { padding: 8px 14px; font-size: 12px; }
  }
</style>

<script>
(function() {
  function renderGrain() {
    var canvas = document.getElementById('grain-canvas');
    if (!canvas) return;
    var w = canvas.width  = canvas.offsetWidth  || window.innerWidth;
    var h = canvas.height = canvas.offsetHeight || window.innerHeight;
    var ctx = canvas.getContext('2d');
    var img = ctx.createImageData(w, h);
    var d = img.data;
    for (var i = 0; i < d.length; i += 4) {
      var v = Math.random() * 255 | 0;
      d[i] = d[i+1] = d[i+2] = v;
      d[i+3] = 60;
    }
    ctx.putImageData(img, 0, 0);
  }
  var last = 0;
  function loop(ts) {
    if (ts - last > 80) { renderGrain(); last = ts; }
    requestAnimationFrame(loop);
  }
  requestAnimationFrame(loop);

  document.addEventListener('mousemove', function(e) {
    var tags = document.querySelectorAll('.tag');
    var cx = window.innerWidth / 2, cy = window.innerHeight / 2;
    var dx = (e.clientX - cx) / cx, dy = (e.clientY - cy) / cy;
    tags.forEach(function(tag, i) {
      var depth = (i % 3 + 1) * 3;
      tag.style.marginLeft = (dx * depth) + 'px';
      tag.style.marginTop  = (dy * depth) + 'px';
    });
  });
})();
</script>
