<template>
  <div id="app">
    <app-header/>
    <app-main/>
    <app-footer/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Main from '@/components/Main'
import Footer from '@/components/Footer'

export default {
  components: {
    'app-header': Header,
    'app-main': Main,
    'app-footer': Footer,
  },
};
</script>

<style>
html {
  overflow-y: hidden;
}
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  min-height: 100vh;
  background: url('./assets/background.jpg') no-repeat center center;
  background-size: cover;
  background-position: center center;
}
</style>
