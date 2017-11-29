<template>
  <main>
    <section class="head">
      <h1>Открытие showroom</h1>
      <h2>В Виннице</h2>
      <h3>от производителя дизайнерской одежды</h3>
      <a class="button is-link is-outlined is-large" @click="showModal">Узнать адресс</a>
    </section>

    <app-modal :isActive="isActive" @closeModal="closeModal"></app-modal>
  </main>
</template>

<script>
import Modal from '@/components/modal/Modal';

export default {
  components: {
    'app-modal': Modal,
  },
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    showModal() {
      this.isActive = true;
    },
    closeModal() {
      this.isActive = false;
    },
  },
};
</script>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-grow: 1;
  min-height: 100vh;
}
.head {
  font-weight: bold;
  text-transform: uppercase;
  color: #fff;
}

h1 {
  font-size: responsive 2rem 9rem;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
  line-height: 1;
}
h2 {
  font-size: responsive 1.5rem 7rem;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
  line-height: 1;
}
h3 {
  font-size: responsive 1.1rem 4rem;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
}
</style>