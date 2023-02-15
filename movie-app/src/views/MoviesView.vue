<template>
  <h1>movies page</h1>

  <form class="d-flex" role="search">
    <input id="userInput" class="form-control me-2" type="search" placeholder="Search for a movie" aria-label="Search" autofocus>
    <button class="btn btn-outline-success" type="submit">Search</button>
  </form>

  <card>
    <img :src="movies.poster">
<!--    <p :src="movies."></p>-->
  </card>



</template>

<script>
// import movieApi from "../services/movieApi";
import { ref } from "vue"
// import fetchData from "../services/FetchData";

let input =ref("");

function filteredList() {
  movie.toLowerCase()
}

export default {

  data() {
    return {
    movies: []
    }
  },
  mounted() {
   this.getMovie();
  },
  methods: {
    // addmovie(title, director, rating, genre) {
    //
    // }
    getMovie() {
      return fetch('http://www.omdbapi.com/?i=tt3896198&apikey=f119b9f9').then((res) => res.json()).then(res => {
        this.movies = res;
        console.log(this.movies);
      })
    }
  },
  computed: {
   // formattedMovies() {
   //   return this.getMovie()
   // }
  }
}
</script>