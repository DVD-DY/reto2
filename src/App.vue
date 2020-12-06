<template>
  <div id="app">

    <menu-superior></menu-superior>
    <carrusel-imagenes></carrusel-imagenes>
    <section-api></section-api>
    

    <div class="row justify-content-center mb-4">
      <div class="col mt-5" v-for="(item, index) of team" :key="index">
        <team-card v-bind:member="item"></team-card>
      </div>
    </div>
    <nuestro-footer></nuestro-footer>

  </div>
</template>

<script>

import NuestroFooter from './components/NuestroFooter.vue';
import TeamCard from './components/TeamCard.vue';
import MenuSuperior from './components/MenuSuperior.vue';
import CarruselImagenes from './components/CarruselImagenes.vue'
import SectionApi from './components/SectionApi.vue';

export default {
  name: 'App',
  components:{
    NuestroFooter,
    TeamCard,
    MenuSuperior,
    CarruselImagenes,
    SectionApi,
  },
  data(){
    return{
      team:[
        {
          codigo: 1,
          nombre: "Eduer Cardenas",
          descripcion: "27 años, docente tecnico, me gusta el airsoft, los computadores y los videojuegos.",
          rol: "Desarrolador Frontend y tester",
          imagen: "./images/f1.jpg",
        },
        {
          codigo: 2,
          nombre: "Oscar Medrano",
          descripcion: "29 años, analista financiero en sun valley, me gustan las caminatas al aire libre, correr, los deportes,aprender cosas nuevas y los animales.",
          rol: "Desarrolador backend y tester",
          imagen: "./images/f2.jpg",
        },
        {
          codigo: 3,
          nombre: "Diego Acosta",
          descripcion: "34 años, profesor de primaria, me gustan los deportes sobre todo el micro futbol.",
          rol: "Analista de Software",
          imagen: "./images/f3.jpg",
        },
        {
          codigo: 4,
          nombre: "Amaury Yepes",
          descripcion: "46 años, Eléctrico y Electrónico Industrial, me gusta practicar baloncesto y natación.",
          rol: "Arquitecto de Software",
          imagen: "./images/f4.jpg",
        },
      ]
    }
  }
}
</script>

