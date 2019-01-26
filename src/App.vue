<template>
  <div id="app">
    <Navbar/>
    <Test/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './components/partials/Navbar.vue'
import Test from './components/Test.vue'
import Footer from './components/partials/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Test,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
