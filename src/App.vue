<template>
  <div id="app">
    <headerPrincipal />
    <bannerPrincipal />
    <buscaResultado />
    <detalhesEstatisticas />
    <footerChamada />
  </div>
</template>

<script>
import headerPrincipal from "./components/headerPrincipal.vue";
import bannerPrincipal from "./components/bannerPrincipal.vue";
import buscaResultado from "./components/buscaResultado.vue";
import detalhesEstatisticas from "./components/detalhesEstatisticas.vue";
import footerChamada from "./components/footerChamada.vue";

export default {
  components: {
    headerPrincipal,
    bannerPrincipal,
    buscaResultado,
    detalhesEstatisticas,
    footerChamada,
  },
  name: "App",
  data() {
    return {};
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

ul,
li {
  list-style-type: none;
}

a {
  text-decoration: none;
}
#app {
  overflow-x: hidden;
}
.container {
  max-width: 1110px;
  margin: 0 auto;
}
</style>
