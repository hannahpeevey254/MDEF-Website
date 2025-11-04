<!-- Hide sidebar navigation only on the home page -->
<style>
  /* Hide the left sidebar and right TOC only on this page */
  .md-sidebar--primary,
  .md-sidebar--secondary {
    display: none !important;
  }

  /* Let content take full width */
  .md-content {
    max-width: 100% !important;
  }

  /* Center the main section */
  .md-main__inner {
    margin: 0 auto !important;
    padding: 0 !important;
  }

  /* Optional: remove top margin for cleaner look */
  .md-content__inner {
    margin-top: 0 !important;
  }
</style>

<div class="homepage-container">

  <!-- Top Grid -->
  <div class="top-grid">
    <div class="image-box">
      <img src="../images/HomePage_Graphic.png" alt="HomePage_Graphic">
    </div>
    <a href="mdef/index.html" class="grid-box purple">MASTERS<br>PROJECTS</a>
  </div>

  <!-- Bottom Grid -->
  <div class="bottom-grid">
    <a href="index.html" class="grid-box red">HOME</a>
    <a href="about/index.html" class="grid-box orange">ABOUT<br>ME</a>
    <a href="mdef/index.html" class="grid-box brown">MDEF</a>
    <a href="archive/index.html" class="grid-box yellow">ARCHIVE</a>
  </div>

</div>

<style>
/* overall layout */
.homepage-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  margin: 0;
}

/* top section */
.top-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  width: 100%;
  gap: 2rem;
  align-items: stretch;
  margin-bottom: 2rem;
}

.image-box {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-box img {
  width: 100%;
  height: auto;
  max height: 100%
  object-fit: contain;
  display: block;
  transform: scale(1.2);
}

/* bottom section */
.bottom-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
  width: 100%;
}

/* box styling */
.grid-box {
  border-radius: 25px;
  color: #ffffff !important;                /* FORCE white text */
  font-size: 1.8rem;
  font-weight: 700;
  font-family: sans-serif;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 4rem 0;
  text-decoration: none !important;         /* remove underline overrides */
  text-transform: uppercase;
  transition: all 0.3s ease;
}

.grid-box:hover {
  transform: scale(1.05);
  opacity: 0.9;
}

/* color themes */
.purple { background-color: #4A164D !important; }
.red    { background-color: #B3302D !important; }
.orange { background-color: #E38E00 !important; }
.brown  { background-color: #2E1B1B !important; }
.yellow { background-color: #C9D200 !important; }

/* make links stay white when hovered */
a.grid-box:link,
a.grid-box:visited,
a.grid-box:hover,
a.grid-box:active {
  color: #ffffff !important;
}

/* responsive */
@media (max-width: 900px) {
  .bottom-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .grid-box {
    font-size: 1.4rem;
    padding: 3rem 0;
  }
}
</style>
