<script>
  import btm from "../assets/btm2.jpg";
  import saw from "../assets/saw.webp";
  import int from "../assets/int.jpg";
</script>

<div id="carouselExampleIndicators" class="carousel slide">
  <div class="carousel-indicators">
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="0"
      class="active"
      aria-current="true"
      aria-label="Slide 1"
    />
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="1"
      aria-label="Slide 2"
    />
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="2"
      aria-label="Slide 3"
    />
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src={saw} class="d-block w-100" alt="..." />
    </div>
    <div class="carousel-item">
      <img src={btm} class="d-block w-100" alt="..." />
    </div>
    <div class="carousel-item">
      <img src={int} class="d-block w-100" alt="..." />
    </div>
  </div>
  <button
    class="carousel-control-prev"
    type="button"
    data-bs-target="#carouselExampleIndicators"
    data-bs-slide="prev"
  >
    <span class="carousel-control-prev-icon" aria-hidden="true" />
    <span class="visually-hidden">Previous</span>
  </button>
  <button
    class="carousel-control-next"
    type="button"
    data-bs-target="#carouselExampleIndicators"
    data-bs-slide="next"
  >
    <span class="carousel-control-next-icon" aria-hidden="true" />
    <span class="visually-hidden">Next</span>
  </button>
</div>

<style>
  img {
    max-height: 800px;
    max-width: 100vw;
    z-index: 0;
    filter: brightness(50%);
    margin-bottom: 120px;
    flex-grow: 6;
    object-fit: cover;
    opacity: 0.6;
    transition: 0.5s ease;
    box-shadow: 20px 5px 25px 8px rgba(143, 22, 123, 0.5);
  }

  img:hover {
    cursor: grab;
    width: 600px;
    opacity: 0.7;
    box-shadow: inset 0 -3em 3em rgba(0, 0, 0, 0.1), 0 0 0 2px rgb(76, 13, 94),
      0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
    filter: contrast(100%);
  }
</style>
