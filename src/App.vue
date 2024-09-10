<script setup>
import Card from "./components/Card.vue";
import Produtos from "./components/Produtos.vue";
</script>

<template>
  <main>
    <section>
      <Card />
      <Produtos />
    </section>
  </main>
</template>

<style lang="scss" scoped>
main {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

section {
  width: 60vw;
  display: flex;
  /* border: solid; */
  align-items: center;
  justify-content: space-evenly;
}
</style>
