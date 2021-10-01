<template>
  <section class="modal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <!-- Modal title -->
          <h5 class="modal-title">Shopping Cart</h5>
          <!-- Close button -->
          <button type="button" class="btn-close" @click="$emit('closeModal')" aria-label="Close"></button>
        </div>

        <div class="modal-body">
          <!-- Empty cart message -->
          <p v-if="cart.length == 0">The cart is empty. Please add a product</p>
          <!-- Products in cart -->
          <template v-else>
            <div v-for="product in cart" :key="product.name" class="card mb-3">
            <div class="row g-0 justify-content-between">
              <div class="col-4">
                <img :src="require(`../assets/${product.image}`)" class="img-fluid rounded-start" alt="...">
              </div>
              <div class="col-7 col-md-8">
                <div class="card-body">
                  <h5 class="card-title">{{ product.name }}</h5>
                  <p class="card-text">€{{ product.price }}</p>
                  <p class="card-text"><small class="text-muted">{{ product.category }}</small></p>
                </div>
              </div>
            </div>
            </div>
          </template>
        </div>

        <!-- Modal footer -->
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" @click="$emit('closeModal')">Close</button>
          <button type="button" class="btn btn-primary">Buy</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Modal',
  props: ["cart"],
}
</script>

<style scoped>
  .modal {
    display: block;
    background-color: #13151554;
  }
  .img-fluid {
    object-fit: cover;
    width: 8rem;
    height: 8rem;
  }
  .btn.btn-primary {
    background-color: var(--color-primary);
    border-color: var(--color-primary);
  }
  .btn.btn-primary:hover {
    background-color: var(--color-complementary);
    border-color: var(--color-complementary);
  }
</style>