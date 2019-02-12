<template>
  <div id="app">
    <h1>Les supers films</h1>
    <MovieList v-bind:movies="myMovies"/>
    <GenrePicker @genreSelected="filterMovies($event)" />
  </div>
</template>

<script>
import MovieList from './components/MovieList.vue'
import GenrePicker from './components/GenrePicker.vue'
import axios from 'axios'


export default {
  name: 'app',
  data() {
    return {
      myMovies: []
    }
  },
  methods:{
    filterMovies(g){
        alert("App.vue a bien reçu l'événement;, il faut filtrer les films " + g)
    }
  },
  components: {
    MovieList,
    GenrePicker
  },
  created(){
    axios.get('https://wt-902485dbb4fca4fccee3a0efcde5b34c-0.sandbox.auth0-extend.com/films')
    .then(response => {
        this.myMovies = response.data
    })
  }

}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
