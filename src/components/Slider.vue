<template>
  <div id="carousel" class="carousel slide carousel-fade d-none d-md-block" data-bs-ride="carousel">
    <!-- Carousel indicators -->
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <!-- Carousel images -->
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/karsten-wurth-karsten-wuerth-IMU55XrxS4E-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="@/assets/j-scott-rakozy-CNLKEp0WY4g-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="@/assets/nathan-anderson-kujXUuh1X0o-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
    </div>
    <!-- Carousel controls -->
    <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Slider',
}
</script>