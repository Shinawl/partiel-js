<template>
  <div class="custom">
    <div class="etape-1">
      <h2>1/3  J’indique mes dimensions</h2>
      <label for="rail-lenght"><strong>Longueur du rail:</strong></label>
      <input type="number" placeholder="max. 200cm" id="number" name="rail-lenght"
       min="0" max="200">
    </div>
    <button>Valider</button>
    <!-- Ici j'essaye de montre l'étape d'après une fois le bouton cliquer -->
    <button v-on:click="show">Montrer</button>
  <div v-if="isDisplay">
    <p>Je suis visible !</p>
    <button v-on:click="hide">Cacher</button>
  </div>

    <div class="etape-2">
      <h2>2/3  J’indique mon type de rail</h2>
      <div class="option">
        <label for="color-b">
          <div class="white">
          <input type="radio" id="noir" name="color-b" value="blanc" checked>
          <img class="oui" src="../assets/modele_DS.png" alt="blanc">
        </div>
        <span>Blanc</span>
        </label>

        <label for="color-n">
          <div class="Black">
          <input type="radio" id="noir" name="color-n" value="noir" checked>
          <img class="oui" src="../assets/modele_CS.png" alt="noir">
        </div>
        <span>Noir</span>
        </label>

      </div>
      <button>Valider</button>

    </div>
    <div class="etape-3">
      <h2>3/3  Je sélectionne ma couleur</h2>
      <div class="option">
        <label for="color-b">
          <div class="white">
          <input type="radio" id="blanc" name="color-b" value="blanc" checked>
          <img src="../assets/Blanc.png" alt="blanc">
        </div>
        <span>Blanc</span>
        </label>

        <label for="color-n">
          <div class="Black">
          <input type="radio" id="noir" name="color-n" value="noir" checked>
          <img src="../assets/Noir.png" alt="noir">
        </div>
        <span>Noir</span>
        
        </label>
      </div>
    </div>
    <button>Valider</button>
  </div>
</template>

<script>
export default {
  name: 'Custom',
  props: {
    msg: String
  } data: { // La j'essaye de créé un évènement pour afficher la troisième étape avec un bouton
    let etape3 = document.getElementsByClassName("etape-3");

    etape3.addEventListener("mouseclick", () => {etape3.style.visibility = "show";});
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
#number {
  padding: 1em;
  width: 7em;
  height: 1em;
}
.etape-1 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  padding: 1em;
}
/* Je fait disparaître le bouton radio */
[type=radio] { 
  position: absolute;
  opacity: 0;
  width: 0;
  height: 0;
}

/* Je remplace le bouton cacher par l'image */
[type=radio] + img {
  cursor: pointer;
}

/* Ici le but est d'avoir un style quand le bouton est clicker */
[type=radio]:checked + img {
  outline: 2px solid rgb(0, 0, 0);
}

.option {
  display: flex;
  justify-content: center;
}

label {
  margin: 1em;
}

.etape-1 {
  padding: 1em;
  border-bottom: 1px solid #000000;
}
.etape-2 {
  padding: 1em;
  border-bottom: 1px solid #000000;
}
.etape-3 {
  padding: 1em;
  border-bottom: 1px solid #000000;
  visibility: hidden;
}

.oui {
  width: 40%;
}

.custom {
  width: 25%;
}
</style>