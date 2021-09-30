<template>
  <footer class="container-fluid">
    <section class="row justify-content-between py-3">
      <div class="col-12 col-md-2">
        <h4>Quick Links</h4>
        <nav class="nav flex-column">
          <a class="nav-link" href="#">Home</a>
          <a class="nav-link" href="#">Event</a>
          <a class="nav-link" href="#">Support</a>
          <a class="nav-link" href="#">Contact</a>
        </nav>
      </div>
      <div class="col-12 col-md-6">
        <h4>Announcements / Promoted Contect</h4>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quas rerum rem accusantium magnam laboriosam quos neque 
          beatae ex labore qui odit earum quasi, facere suscipit laudantium! Nemo officiis corrupti voluptate.
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quas rerum rem accusantium magnam laboriosam quos neque 
          beatae ex labore qui odit earum quasi.</p>
      </div>
      <div class="col-12 col-md-2">
        <h4>Coming Soon</h4>
        <img src="https://picsum.photos/200" class="footer-image rounded" alt="">
      </div>
    </section>
    <section class="row text-center">
      <p>©2021 AcmeWidgets. All Rights Reserved. Support: <a href="Support@AcmeWidgets.com">Support@AcmeWidgets.com</a></p>
    </section>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
  footer {
    background-color: var(--color-secondary);
  }
  .nav-link {
    color: var(--color-complementary);
  }
  .nav-link:hover {
    color: var(--color-dark);
    text-decoration: underline;
  }
  .footer-image {
    width: 100%;
  }
</style>