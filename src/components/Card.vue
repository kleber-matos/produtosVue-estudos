<script setup>
import { ref } from "vue";
const carrinho = ref(0);

function adicionar() {
  carrinho.value++;
}

function remover() {
  if (carrinho.value > 0) {
    carrinho.value--;
  }
}
</script>

<template>
  <main>
    <section>
      <div class="card">
        <figure>
          <img src="../assets/carrinho.png" alt="Carrinho" />
          <figcaption>Adicione ao carrtinho.</figcaption>
        </figure>

        <div>
          <button @click="adicionar">+</button>
          <h3>{{ carrinho }}</h3>
          <button @click="remover">-</button>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss">
@mixin flebox {
  display: flex;
  justify-content: center;
  align-items: center;
}

.card {
  /* border: solid; */
  border-radius: 10px;
  width: 25vw;
  height: 30vh;
  background-color: #f7e0ce;
  padding: 10px;
  @include flebox();
  flex-direction: column;
  justify-content: space-evenly;
  max-width: 200px;
}

.card figure {
  /* border: solid; */
  border-radius: 10px;
  @include flebox();
  flex-direction: column;
  background-color: #d3c5bb;
  padding: 10px;
  text-align: center;
}

.card div {
  @include flebox();
  justify-content: space-evenly;
  /* border: solid; */
  width: 50%;
  background-color: #d3c5bb;
  border-radius: 10px;
}

.card button {
  border-radius: 100%;
  width: 30%;
  cursor: pointer;
  border: none;
}
</style>
