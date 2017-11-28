<template>
  <div id="app">
    <app-header/>
    <app-main/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Main from '@/components/Main'

export default {
  components: {
    'app-header': Header,
    'app-main': Main,
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
