<template>
<div :class="{ 'is-active': isActive }" class="modal">
  <div class="modal-background"></div>
  <div class="modal-content">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Mollitia consequuntur obcaecati adipisci quae earum similique, impedit, non at dolores enim doloremque facilis odit quam magnam fugit, labore expedita blanditiis reprehenderit autem quaerat voluptates molestias repellat. Dolores quos mollitia ut tempore, quibusdam tenetur similique ex deleniti voluptate suscipit? Voluptates, iste at!
  </div>
  <button class="modal-close is-large" aria-label="close"></button>
</div>
</template>

<script>
  export default {
    data() {
      return {
        isActive: false,
      }
    }
  }
</script>

<style scoped>
.modal-content {
  background-color: #fff;
  padding: 2rem;
}
</style>