<template>
  <div id="carousel" class="carousel slide carousel-fade" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/ian-dooley-TT-ROxWj9nA-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="@/assets/brooke-cagle-z1B9f48F5dc-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="@/assets/felipe-galvan-AhfrA5VQNpM-unsplash.jpg" class="d-block w-100" alt="...">
      </div>
    </div>
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

<style scoped>
  .carousel-item img {
    height: 88vh;
  }
</style>