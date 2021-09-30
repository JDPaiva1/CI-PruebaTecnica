<template>
  <section class="container-fluid items-grid my-4">
    <div class="item">
      <img src="@/assets/photo-1616578492900-ea5a8fc6c341.jpeg" class="item-image rounded mb-2" alt="">
      <h4>Item Title <span class="badge rounded-pill">Item Category</span></h4>
      <p>Price</p>
      <button type="button" class="btn btn-outline-primary">Add to cart</button>
    </div>
    <div class="item">
      <img src="@/assets/photo-1616578492900-ea5a8fc6c341.jpeg" class="item-image rounded mb-2" alt="">
      <h4>Item Title <span class="badge rounded-pill">Item Category</span></h4>
      <p>Price</p>
      <button type="button" class="btn btn-outline-primary">Add to cart</button>
    </div>
    <div class="item">
      <img src="@/assets/photo-1616578492900-ea5a8fc6c341.jpeg" class="item-image rounded mb-2" alt="">
      <h4>Item Title <span class="badge rounded-pill">Item Category</span></h4>
      <p>Price</p>
      <button type="button" class="btn btn-outline-primary">Add to cart</button>
    </div>
    <div class="item">
      <img src="@/assets/photo-1616578492900-ea5a8fc6c341.jpeg" class="item-image rounded mb-2" alt="">
      <h4>Item Title <span class="badge rounded-pill">Item Category</span></h4>
      <p>Price</p>
      <button type="button" class="btn btn-outline-primary">Add to cart</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Navbar',
}
</script>

<style scoped>
  .items-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(100px, 293px));
    justify-content: center;
    gap: 1em;
  }
  .item {
    position: relative;
    display: block;
  }
  .item-image {
    width: 100%;
    vertical-align: top;
  }
  span.badge {
    background-color: var(--color-primary);
  }
  .btn-outline-primary {
    width: 100%;
    color: var(--color-primary);
    border-color: var(--color-primary);
  }
  .btn-outline-primary:hover {
    color: var(--color-light);
    background-color: var(--color-primary);
    border-color: var(--color-primary);
  }
  @media screen and (max-width: 420px) {
    .items-grid {
      grid-template-columns: repeat(2, minmax(100px, 293px));
    }
  }
</style>