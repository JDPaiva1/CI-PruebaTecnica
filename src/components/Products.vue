<template>
  <!-- Products grid -->
  <section class="container-fluid products-grid mt-4 mb-5">
    <!-- Item -->
    <div v-for="product in products" :key="product.name" class="item">
      <img :src="require(`../assets/${product.image}`)" class="item-image rounded mb-2" alt="">
      <h4>{{ product.name }}</h4>
      <span class="badge text-end">{{ product.category }}</span>
      <p>€{{ product.price }}</p>
      <button type="button" class="btn btn-outline-primary" @click="addToCart(product)">Add to cart</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Products',
  data() {
    return {
      products: [
        {
          name: "Item Title 1",
          category: "Item Category 1",
          price: 88.00,
          image: 'mahosadha-ong-fVfKqivw8oM-unsplash.jpg',
        },
        {
          name: "Item Title 2",
          category: "Item Category 2",
          price: 88.00,
          image: 'tanner-geringer-EtVqF6-aqT4-unsplash.jpg',
        },
        {
          name: "Item Title 3",
          category: "Item Category 3",
          price: 88.00,
          image: 'yogesh-gosavi-lC90ji6ig18-unsplash.jpg',
        },
        {
          name: "Item Title 4",
          category: "Item Category 4",
          price: 88.00,
          image: 'samuel-robinson-ZunCOhHzcFo-unsplash.jpg',
        }
      ]
    }
  },
  methods: {
    addToCart(product) {
      this.$emit("addToCart", product);
    }
  }
}
</script>

<style scoped>
  .products-grid {
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
    display: block;
    color: var(--color-primary);
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
    .products-grid {
      grid-template-columns: repeat(2, minmax(100px, 293px));
    }
  }
</style>