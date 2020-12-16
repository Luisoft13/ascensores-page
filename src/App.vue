<template>
  <div id="app">
    <NavBar/>
    <Inicio id="inicio"/>
    <Nosotros id="nosotros"/>
    <Servicio id="service"/>
    <Products id="products"/>
    <Proovedores/>
    <Form id="contacto"/>
    <Footer/>
    <Whatsapp/>
  </div>
</template>

<script>
import Inicio from './components/Inicio.vue'
import NavBar from '@/components/Navbar.vue'
import Nosotros from '@/components/Nosotros.vue'
import Servicio from '@/components/Servicio.vue'
import Products from '@/components/Products.vue'
import Form from '@/components/ContactForm.vue'
import Footer from '@/components/Footer.vue'
import Proovedores from '@/components/Proovedores.vue'
import Whatsapp from '@/components/Whatsapp.vue'


export default {
  name: 'App',
  components: {
    Inicio,
    NavBar,
    Nosotros,
    Servicio,
    Products,
    Form,
    Footer,
    Proovedores,
    Whatsapp
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
