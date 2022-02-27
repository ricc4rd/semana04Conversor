<template>

<div class="fondo">
   <navbar/>
   <convertidor />
</div>
  
  
</template>

<script>
import navbar from './components/navbar.vue';
import convertidor from './components/convertidor.vue';

export default {
  name: 'App',
  components: {
   navbar,
   convertidor
  }
}
</script>

<style>
.fondo{
  background-image: url('./assets/fondo3pared.jpg');
  height: 300vh;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
