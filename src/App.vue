<template>
  <div id="app">
    <app-header/>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    'app-header': Header,
  },
};
</script>

<style>
#app {
  font-family: 'PT Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
