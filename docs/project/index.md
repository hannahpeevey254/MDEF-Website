<style>
.term-section {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 40px;
  margin-top: 60px;
  flex-wrap: wrap;
}

.term-card {
  width: 240px;
  height: 360px;
  border-radius: 20px;
  color: white;
  font-weight: 700;
  font-size: 28px;
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
.term2 { background-color: #d4d60a; }  /* yellow-green */
.term3 { background-color: #4b1c45; }  /* purple */

.term-description {
  opacity: 0;
  color: #fff;
  font-size: 14px;
  text-align: center;
  margin-top: 10px;
  transition: opacity 0.3s ease;
  width: 220px;
  line-height: 1.4;
}

.term-card:hover .term-description {
  opacity: 1;
}

.term-card a {
  color: inherit;
  text-decoration: none;
  display: block;
  width: 100%;
  height: 100%;
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
