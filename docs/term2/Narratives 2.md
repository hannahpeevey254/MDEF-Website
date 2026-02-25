## ★ Narratives 2
<p style="text-align:center; max-width:800px; margin:auto;">
The first draft to my Narratives Publication.

This will be a flip book style broken up into 3 segments horizontally. As you chose which to flip, different connections and ideas are revealed. The concept lies behind an idea of a playful, exploratory approach to my research throughout MDEF. 
</p>


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Image Carousel</title>

  <style>
    /* Image size you showed: 1275 × 1650 (portrait) */
    :root{
      --slide-max-width: 1275px;
      --slide-aspect: 1275 / 1650;
    }

    .slideshow-container {
  /* 50% of screen, but never larger than the image */
  width: min(50vw, 500px); /* adjust 650px if you want bigger or smaller */
  aspect-ratio: var(--slide-aspect);
  position: relative;
  margin: 50px auto 0;
  border: 1px solid #ddd;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  background: #000;
}

    .mySlides { display: none; height: 100%; }

    .mySlides img {
      width: 100%;
      height: 100%;
      object-fit: contain; /* preserves full image (no crop) */
      display: block;
    }

    .prev, .next {
      cursor: pointer;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      padding: 16px;
      color: white;
      font-weight: bold;
      font-size: 20px;
      transition: 0.6s ease;
      user-select: none;
      background-color: rgba(0, 0, 0, 0.5);
    }

    .prev { left: 0; border-radius: 0 3px 3px 0; }
    .next { right: 0; border-radius: 3px 0 0 3px; }

    .prev:hover, .next:hover { background-color: rgba(0, 0, 0, 0.8); }

    .text {
      color: #f2f2f2;
      font-size: 15px;
      padding: 8px 12px;
      position: absolute;
      bottom: 8px;
      width: 100%;
      text-align: center;
      text-shadow: 0 2px 6px rgba(0,0,0,0.9);
    }
  </style>
</head>

<body>
  <div class="slideshow-container">
    <div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0001.jpg" alt="Image 1">
      <div class="text">Image 1 of 7</div>
    </div>

<div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0002.jpg" alt="Image 2">
      <div class="text">Image 2 of 7</div>
    </div>

<div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0003.jpg" alt="Image 3">
      <div class="text">Image 3 of 7</div>
    </div>

 <div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0004.jpg" alt="Image 4">
      <div class="text">Image 4 of 7</div>
    </div>

<div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0005.jpg" alt="Image 5">
      <div class="text">Image 5 of 7</div>
    </div>

 <div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0006.jpg" alt="Image 6">
      <div class="text">Image 6 of 7</div>
    </div>

 <div class="mySlides">
      <img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_page-0007.jpg" alt="Image 7">
      <div class="text">Image 7 of 7</div>
    </div>

 <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
    <a class="next" onclick="plusSlides(1)">&#10095;</a>
  </div>

  <script>
    let slideIndex = 1;
    showSlides(slideIndex);

    function plusSlides(n) {
      showSlides(slideIndex += n);
    }

    function showSlides(n) {
      const slides = document.getElementsByClassName("mySlides");

      if (n > slides.length) slideIndex = 1;
      if (n < 1) slideIndex = slides.length;

      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slides[slideIndex - 1].style.display = "block";
    }
  </script>
</body>
</html>

---
</div>
<h2 style="margin-top:20; text-align:center;"> Peer Poster Swarna</h2>
<!-- FULL-WIDTH IMAGE -->
<div style="width:100%; margin: 30px 0; text-align:center;">
<img src="../images/PEER POSTER 2.jpg" style="width:50%; height:auto; border-radius:6px;">
</div>

---

</div>
<h2 style="margin-top:20; text-align:center;"> Peer Poster Hannah</h2>
<!-- FULL-WIDTH IMAGE -->
<div style="width:100%; margin: 30px 0; text-align:center;">
<img src="../images/HANNAH PEEVEY NARRATIVES PROGRESS_peer poster.jpg" style="width:50%; height:auto; border-radius:6px;">
</div>
