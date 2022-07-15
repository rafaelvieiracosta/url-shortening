<template>
  <div id="app">

    <header-principal />
    <banner-principal />
    
  </div>
</template>

<script>
import headerPrincipal from './components/headerPrincipal.vue'
import bannerPrincipal from './components/bannerPrincipal.vue'

export default {
  components: { 
    headerPrincipal,
    bannerPrincipal 
  },
  name: 'App',
  data(){
    return{

    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

ul,li{
  list-style-type: none;
}

a{
  text-decoration: none;
}
#app{
  padding: 0 24px;
  overflow-x: hidden;
}
.container{
  max-width: 1110px;
  margin: 0 auto;
}


</style>
