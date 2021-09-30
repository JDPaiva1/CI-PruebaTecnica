<template>
  <Navbar/>
  <Slider/>
  <section class="container-fluid">
    <h1>Intro Copy Headline</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius, cumque nesciunt expedita commodi fuga sed!
      Nisi laudantium accusamus voluptate aliquid omnis. Ratione autem praesentium, asperiores facere quis sint at. Laudantium.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius, cumque nesciunt expedita commodi fuga sed!
      Nisi laudantium accusamus voluptate aliquid omnis. Ratione autem praesentium, asperiores facere quis sint at. Laudantium.</p>
  </section>
  <Items/>
  <Footer/>
  <Modal v-if="showModal" @close="showModal = false"/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Slider from './components/Slider.vue'
import Items from './components/Items.vue'
import Footer from './components/Footer.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Slider,
    Items,
    Footer,
    Modal
  },
  data() {
    return { showModal: false }
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
