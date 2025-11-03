<style>
.term-section {
  display: flex;
  justify-content: center;
  align-items: stretch;
  gap: 40px;
  margin: 80px auto;
  flex-wrap: nowrap;
  max-width: 1200px;
}

.term-card {
  width: 260px;
  height: 400px;
  border-radius: 25px;
  color: white;
  font-weight: 800;
  font-size: 36px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  transition: all 0.4s ease;
  position: relative;
}

.term-card:hover {
  transform: translateY(-10px);
}

.term1 { background-color: #3b2424; }  /* dark brown */
.term2 { background-color: #d4d60a; color: black; }  /* yellow-green */
.term3 { background-color: #4b1c45; }  /* purple */

.term-description {
  position: absolute;
  bottom: 20px;
  width: 80%;
  text-align: center;
  font-size: 14px;
  color: rgba(255, 255, 255, 0.85);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.term2 .term-description {
  color: rgba(0, 0, 0, 0.7); /* darker text on yellow */
}

.term-card:hover .term-description {
  opacity: 1;
}

.term-card a {
  color: inherit;
  text-decoration: none;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>

<div class="term-section">

  <div class="term-card term1">
    <a href="../term1/index.html">
      TERM<br>1
      <div class="term-description">
        Foundations, research interests, and early explorations.
      </div>
    </a>
  </div>

  <div class="term-card term2">
    <a href="../term2/index.html">
      TERM<br>2
      <div class="term-description">
        Prototyping, testing, and refining design concepts.
      </div>
    </a>
  </div>

  <div class="term-card term3">
    <a href="../term3/index.html">
      TERM<br>3
      <div class="term-description">
        Final outcomes, reflection, and project synthesis.
      </div>
    </a>
  </div>

</div>
