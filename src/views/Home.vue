<template>
  <div class="container">
    <h1 class="text-center">Paises API</h1>
    <Continentes />
    <Buscador />
    <CardList />
  </div>
</template>

<script>
import CardList from "../components/CardList";
import Buscador from "../components/Buscador";
import Continentes from "../components/Continentes";

export default {
  components: {
    CardList,
    Buscador,
    Continentes
  },
  name: "Home"
};
</script>
