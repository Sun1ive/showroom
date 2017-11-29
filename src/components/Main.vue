<template>
  <main>
    <section class="head">
      <h1>Открытие showroom</h1>
      <h2>В Виннице</h2>
      <h3>от производителя дизайнерской одежды</h3>
      <a class="button is-info is-large" @click="showForm">Узнать адресс</a>
      
    </section>

    <app-modal :active="active" @closeModal="closeModal"></app-modal>

    <app-Form @showModal="showModal" @closeForm="closeForm" :isActive="isActive"></app-Form>

  </main>
</template>

<script>
import Modal from '@/components/modal/Modal';
import Form from '@/components/modal/Form';

export default {
  components: {
    'app-modal': Modal,
    'app-Form': Form,
  },
  data() {
    return {
      isActive: false,
      active: false,
      count: null,
    };
  },
  methods: {
    showForm() {
      this.isActive = true;
    },
    closeForm() {
      this.isActive = false;
    },
    showModal() {
      this.active = true;
    },
    closeModal() {
      this.active = false;
    }
  }
};
</script>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-grow: 1;
  min-height: 85vh;
}
.head {
  font-weight: bold;
  text-transform: uppercase;
  color: #fff;
}

h1 {
  font-size: responsive 1.3rem 5rem;
  font-weight: 800;
  color: #333;
  line-height: 1.2;
}
h2 {
  font-size: responsive 1.1rem 3rem;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
  line-height: 1.2;
}
h3 {
  font-size: responsive 1rem 2rem;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
}
.button {
  margin-top: 2rem;
}
</style>