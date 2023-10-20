<script>
  import btm3 from "../assets/btm3.webp";
  import jk from "../assets/jk.jpg";
  import int from "../assets/int.jpg";
</script>




<div id="carouselExampleIndicators" class="carousel slide">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1" />
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2" />
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3" />
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src={jk} class="d-block w-100" alt="..." />
    </div>
    <div class="carousel-item">
      <img src={btm3} class="d-block w-100" alt="..." />
    </div>
    <div class="carousel-item">
      <img src={int} class="d-block w-100" alt="..." />
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true" />
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true" />
    <span class="visually-hidden">Next</span>
  </button>
</div>



<style>
  input{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: black;
  }
  img {
    max-height: 800px;
    max-width: 100vw;
    border-radius: 8px;
    filter: brightness(50%);
    margin-bottom: 120px;
    flex-grow: 1;
    object-fit: cover;
    behavior: smoth;
    box-shadow: 20px 5px 25px 8px rgba(143, 22, 123, 0.5);
  }

  img:hover {
    cursor: grab;
  }
</style>
