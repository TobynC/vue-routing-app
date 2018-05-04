<template>
  <div id="app">   
    <NavbarComponent />
    <router-view/>
  </div>
</template>

<script>
import NavbarComponent from '@/components/Navbar'

export default {
  name: 'App',
  components: {
    NavbarComponent
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
a.router-link-exact-active{
  color: purple;
}
</style>
