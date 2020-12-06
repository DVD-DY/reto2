<template>


    <div id="Peliculitas"  class="row "  >
        <div class="card col-md-6"  v-for="(movie,index) of movies" :key="index" > 
            
              <div class="d-flex justify-content-center p-2">
                    <img v-bind:src="movie.Poster"  alt="Movie Poster" width="250">

                </div>
              
              <div class="card-body">
                <h5 class="card-title text-center">{{movie.Title}}</h5>
                <p class="card-text text-center">Esta pelicual se estreno en el año: {{movie.Year}}</p>
                <a :href="'https://www.imdb.com/title/'+ movie.imdbID" class="btn btn-dark d-flex justify-content-center ">Informacion</a>
              </div>              
        </div>
    </div>
  
</template>

<script>

import axios from "axios"

export default {
    name: "SectionApi",
    data(){
        return{
            movies : null
        }
    },
    mounted(){
        axios.get(`http://www.omdbapi.com/?s=terminator&type=movie&apikey=81f84c2e`)
        .then(response => {
            (this.movies = response.data.Search.slice(0,4))
            console.log(this.movies)
        })
    }
}
</script>