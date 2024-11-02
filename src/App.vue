<template>
  
  <Menu />
  <router-view/>
  
  <Footer/>

</template>

<script>
import Menu from './components/Menu.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Menu,
    Footer
  }

}
</script>





<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center; 
  color: #291e8fcc;
}


</style>
