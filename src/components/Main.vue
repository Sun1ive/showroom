<template>
  <main>
    <section class="head">
      <h1>Открытие showroom</h1>
      <h2>В Виннице</h2>
      <h3>от производителя дизайнерской одежды</h3>
    </section>
  </main>
</template>

<script>
export default {};
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
}

h1 {
  font-size: responsive 2rem 10rem;
  color: #ccc;
  text-shadow: -1px -1px #000, 0px 1px 0px #444;
  font-weight: bold;
}
h2 {
  font-size: responsive 1.5rem 8rem;
  font-weight: bold;
}
h3 {
  font-size: responsive 1.1rem 4rem;
  font-weight: bold;
}
</style>