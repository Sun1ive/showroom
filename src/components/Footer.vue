<template>
  <footer>
    <h4>Количество уже посетивших {{ count }}</h4>
  </footer>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      count: null,
    };
  },
  created() {
    const vm = this;
    async function getUsers() {
      try {
        const response = await axios.get('https://showroom-fc5ff.firebaseio.com/users.json');
        const result = Object.keys(response.data);
        vm.count = result.length + 1;
      } catch (error) {
        console.log(error);
      }
    }
    getUsers();
  },
};
</script>

<style scoped>
h4 {
  padding-bottom: 2rem;
  color: #fff;
  text-transform: uppercase;
  font-size: responsive 1rem 2rem;
  text-shadow: 1px 1px 1px #333;
  font-family: 'Open Sans', Arial, Helvetica, sans-serif;
}
</style>