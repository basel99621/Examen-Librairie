<script setup>
import { ref, defineEmits } from "vue";
// -- donnée réactive pour la saisie du titre
const titre = ref("");
const titreR = ref("");
const prix = ref(0);
const qtestock = ref(0);
const emit = defineEmits(["addC"]);
</script>

<template>
  <body>
    <form
      id="buttonAjouter"
      @submit.prevent="$emit('addC', titre, prix, qtestock)"
    >
      <input type="text" v-model="titre" placeholder="Nom du livre" />
      <input type="text" v-model="prix" placeholder="Prix du livre" />
      <input
        type="text"
        v-model="qtestock"
        placeholder="La quantité en stock"
      />
      <input type="submit" value="Ajouter" />
    </form>
    <form class="buttonRechercher" @submit.prevent="$emit('addR', titreR)">
      <input type="text" v-model="titreR" placeholder="Livre Rechercher " />
      <input type="submit" value="Rechercher" />
    </form>
  </body>
  <h1>Mes livres</h1>
</template>

<style scoped>
h1 {
  display: flex;
  justify-content: center;
  font-family: Arial, Helvetica, sans-serif; /* Changer la police */
  font-size: 3em; /* Changer la taille de la police */
  text-align: center; /* Centrer le texte */
  color: rgba(255, 64, 0, 0.826); /* Changer la couleur du texte */
  text-shadow: 2px 2px 0 #fff, 4px 4px 0 #999; /* Ajouter un effet d'ombre portée */
  letter-spacing: 0.05em; /* Ajouter un espacement entre les lettres */
  text-transform: uppercase;
}
h1:hover {
  color: rgba(255, 217, 0, 0.751);
}
body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 10vh;
  background-color: rgba(255, 255, 255, 0.847);
}

form {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 80%;
  max-width: 800px;
  margin: 1em 0;
}

input {
  margin: 0.5em;
  padding: 0.5em;
  font-size: 1em;
  border: none;
  border-radius: 0.25em;
  box-shadow: 0 0 0.5em rgba(0, 0, 0, 0.1);
}
</style>
