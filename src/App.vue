<template>
  <div id="app">
    <NavBar/>
    <Inicio/>
    <Nosotros/>
    <Servicio/>
    <Products/>
  </div>
</template>

<script>
import Inicio from './components/Inicio.vue'
import NavBar from '@/components/Navbar.vue'
import Nosotros from '@/components/Nosotros.vue'
import Servicio from '@/components/Servicio.vue'
import Products from '@/components/Products.vue'

export default {
  name: 'App',
  components: {
    Inicio,
    NavBar,
    Nosotros,
    Servicio,
    Products
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
