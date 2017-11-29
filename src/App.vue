<template>
  <div id="app">
    <app-header/>
    <app-main/>

    <app-modal/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Main from '@/components/Main'
import Modal from '@/components/modal/Modal'

export default {
  components: {
    'app-header': Header,
    'app-main': Main,
    'app-modal': Modal,
  },
};
</script>

<style>
#app {
  font-family: 'PT Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url('./assets/background.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
}
</style>
