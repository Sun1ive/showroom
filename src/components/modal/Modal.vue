<template>
<div :class="{ 'is-active': active }" class="modal">
  <div class="modal-background"></div>
    <div class="modal-content">
      <h2>Спасибо! <br> Наш менеджер скоро свяжется с Вами!</h2>
      <i class="fa fa-map-marker"></i>
      <h1>ул. Николая оводова 49</h1>
      <p>вход со двора</p>
      <div class="close" @click="closeModal"></div>
  </div>
</div>
</template>

<script>
export default {
/*   props: {
    active: {
      type: Boolean,
      required: true,
    },
  }, */
  data() {
    return {
      // active: true,
    }
  },
  methods: {
    closeModal() {
      this.$emit('closeModal');
    },
  },
};
</script>

<style scoped>
i {
  font-size: responsive 1rem 4rem;
  color: #3273dc;
}
h1 {
  font-size: responsive 1rem 3.5rem;
  line-height: 1;
}
h2 {
  font-size: responsive 1rem 2rem;
}
p {
  font-size: responsive 1rem 2rem;
}
.modal-content {
  background-color: #fff;
  padding: 2rem;
  position: relative;
  border-radius: 15px;
  color: #000;
}
.modal-content .close {
  position: absolute;
  top: 10px;
  right: 10px;
  background: url('../../assets/close.svg') no-repeat center center;
  width: 25px;
  height: 25px;
  cursor: pointer;
}
</style>