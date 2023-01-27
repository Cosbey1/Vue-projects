<template>
  <h1>movies page</h1>


</template>

<script>
import movieApi from "../services/movieApi";

export default {

  data() {
    return {
    movies: []
    }
  },
  mounted() {
    movieApi.getMovie().then((response) => {
      console.log(response);
    })
        .catch((e) => {
          console.log(e);
        });
    // fetch('http://www.omdbapi.com/?i=tt3896198&apikey=f119b9f9')
    //     .then(response => response.json())
    //     .then(data => this.movies = data)
    //     .catch(err => console.log(err.message))
  },
  methods: {
    addmovie(title, director, rating, genre) {

    }
  },
  computed: {
   // formattedMovies() {
   //   return this.getMovie()
   // }
  }
}
</script>