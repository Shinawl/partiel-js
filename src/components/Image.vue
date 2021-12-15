<template>
  <!-- Ici dans la classe image je met l'inmage et un titre pour la prévisualisation de la tringle à rideau. -->
  <div class="Image">
    <h2>Tringle Rail</h2>
    <img src="../assets/logo.png" alt="tringle">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Image',
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
/* Je met un width à 70% pour réduire l'image */
img {
  width: 70%;
}
</style>
