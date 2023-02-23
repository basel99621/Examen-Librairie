<script setup>
import { defineEmits, defineProps } from "vue";
const props = defineProps(["livre"]);
const emit = defineEmits(["deleteC", "augmenter", "diminuer"]);

const diminuer = () => {
  emit("diminuer", props.livre);
};
const augmenter = () => {
  emit("augmenter", props.livre);
};
</script>

<template>
  <li>
    <div class="book">
      <h2>Titire : {{ livre._titre }}</h2>
      <h2>La quantité : {{ livre._qtestock }}</h2>
      <h2>Le prix : {{ livre._prix }} €</h2>
    </div>
    <!-- cette fois en param du handler 
          on n'utilise pas l'index dans le tableau
          mais directement l'id du livre
          {{ livre.pourAfficher() }}
    -->

    <div class="buttonBas">
      <button class="buttonSup" @click="$emit('deleteC', livre.id)">
        Supprimer
      </button>
      <!-- cette fois sen param du handler 
          on n'utilise pas l'index dans la tableau 
          mais directement la chose à modifier
    -->
      <button class="buttonDim" type="button" @click="diminuer">-</button>
      <span class="qt">{{ livre._qtestock }}</span>
      <button class="buttonAug" type="button" @click="augmenter">+</button>
    </div>
  </li>
</template>

<style>
.book {
  width: 200px;
  height: 250px;
  background-color: rgba(38, 123, 183, 0.703);
  box-shadow: 10px 10px 10px rgba(227, 227, 227, 0.724);
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  margin: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to bottom right, #d6a504, #030202);
  font-family: Arial, Helvetica, sans-serif;
  color: rgba(255, 251, 19, 0.553);
  text-shadow: 0px 0px 5px whitesmoke;
}

.qt {
  border: solid;
  background-color: rgb(243, 210, 0);
  color: rgba(255, 0, 0, 0.607);
  padding: 5px;
}
.qt:hover {
  transform: scale(1.1);
}
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex; /* afficher les livres en tant que flex container */
  flex-wrap: wrap; /* permettre à la ligne de se casser pour les écrans plus petits */
  justify-content: center; /* centrer les livres horizontalement sur la page */
}
li {
  margin: 10px; /* ajouter un peu d'espace entre les livres */
}
.buttonBas {
  list-style: none;
  display: flex; /* afficher les livres en tant que flex container */
  flex-wrap: wrap; /* permettre à la ligne de se casser pour les écrans plus petits */
  justify-content: center; /* centrer les livres horizontalement sur la page */
  display: flex;

  gap: 10px;
}
.buttonAug,
.buttonSup,
.buttonDim {
  background-color: rgb(243, 210, 0);
  color: rgba(255, 0, 0, 0.607);
  border: 1px solid #ccc;
  padding: 3px 5px;
  border-radius: 5px;
  text-decoration: none;
  font-size: 16px;
  text-transform: uppercase;
}
.buttonSup:hover {
  transform: scale(1.1);
}
.buttonAug:hover {
  transform: scale(1.1);
}
.buttonDim:hover {
  transform: scale(1.1);
}
</style>
