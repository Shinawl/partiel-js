<template>
  <AddPanier msg=""/>
  <Image msg=""/>
  <Panier msg=""/>
  <Custom msg=""/>
</template>

<script>
import AddPanier from './components/AddPanier.vue'
import Image from './components/Image.vue'
import Panier from './components/Panier.vue'
import Custom from './components/Custom.vue'

export default {
  name: 'App',
  components: {
    AddPanier,
    Image,
    Panier,
    Custom
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
  margin-top: 60px;
  display: flex;
}
</style>
