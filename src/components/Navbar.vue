<template>
  <nav class="navbar navbar-light nav-first justify-content-center justify-content-md-end">
    <!-- Cart button -->
    <button class="btn btn-outline-secondary position-relative cart-buttom me-3" @click="$emit('openModal')">
      <svg xmlns="http://www.w3.org/2000/svg" width="20" fill="currentColor" class="bi bi-cart" viewBox="0 0 16 16">
        <path d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z" />
      </svg>
      <span class="position-absolute top-0 start-100 translate-middle badge rounded-pill bg-danger">
        {{ itemsInCart }}
        <span class="visually-hidden">unread messages</span>
      </span>
    </button>
    <a class="btn-my-account" href="#">My Account</a>
    <!-- Search -->
    <div class="d-flex mx-3">
      <form class="input-group">
        <input class="form-control" type="search" placeholder="Search" aria-label="Search" aria-describedby="Search">
        <button class="btn btn-outline-secondary" type="button" id="Search">Search</button>
      </form>
    </div>
  </nav>

  <nav class="navbar navbar-expand-lg navbar-light nav-second">
    <div class="container-fluid">
      <!-- Tittle -->
      <a class="navbar-brand" href="#">A Big Title</a>
      <!-- Toggle button -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <!-- Navbar -->
      <div class="collapse navbar-collapse justify-content-end" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
          <a class="nav-link" href="#">Event</a>
          <a class="nav-link" href="#">Accesories</a>
          <a class="nav-link" href="#">Apparel</a>
          <a class="nav-link" href="#">Featured Items</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: ["itemsInCart"],
  emits: ['openModal']
}
</script>

<style scoped>
  .nav-first {
    background-color: var(--color-primary);
    padding-top: .75rem;
    padding-bottom: .6rem;
  }
  .nav-second {
    background-color: var(--color-secondary);
  }
  .btn-outline-secondary {
    color: var(--color-dark);
    border-color: var(--color-dark);
  }
  .btn-outline-secondary:hover {
    color: var(--color-light);
    background-color: var(--color-complementary);
    border-color: var(--color-dark);
  }
  .btn-my-account {
    color: var(--color-dark);
  }
  @media screen and (max-width: 420px) {
    .nav-first .cart-buttom {
      margin-bottom: .5rem;
    }
  }
</style>