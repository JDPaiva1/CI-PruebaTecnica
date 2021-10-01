<template>
  <Navbar @openModal="showModal = true" :itemsInCart="cart.length"/>
  <Slider/>
  <Intro/>
  <Products @addToCart="addToCart($event)"/>
  <Footer/>
  <Modal v-if="showModal" @closeModal="showModal = false" :cart="cart"/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Slider from './components/Slider.vue'
import Intro from './components/Intro.vue'
import Products from './components/Products.vue'
import Footer from './components/Footer.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Slider,
    Intro,
    Products,
    Footer,
    Modal
  },
  data() {
    return { 
      showModal: false,
      cart: []
    }
  },
  methods: {
    addToCart(product) {
      this.cart.push(product);
    }
  }
}
</script>

<style>
:root {
  --color-primary: #339989;
  --color-secondary: #7DE2D1;
  --color-complementary: #22665C;
  --color-dark: #131515;
  --color-light: #FFFAFB;
}
body {
  background-color: var(--color-light);
  color: var(--color-dark);
}
</style>
