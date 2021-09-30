<template>
  <section class="modal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Modal title</h5>
          <button type="button" class="btn-close" @click="$emit('close')" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <p>Modal body text goes here.</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" @click="$emit('close')">Close</button>
          <button type="button" class="btn btn-primary"></button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Modal',
}
</script>

<style scoped>
  .modal {
    display: block;
    background-color: #13151554;
  }
</style>