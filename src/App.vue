<template>
  <div id="app">
    <Header @search="searchAlbums" />
    <!-- Invio props albums al main -->
    <Main :albums="filteredAlbums"/>
  </div>
</template>

<script>
import axios from "axios"
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data (){
    return {
      albums: [],
      //Creo un altro array
      filteredAlbums: [],
    }
  },
  created (){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((result) =>{
      this.albums = result.data.response;
      this.filteredAlbums = result.data.response;
    })
  },
  computed: {
  },
  methods: {
    //invio nel nuovo array le parole che sono incluse nell'array albums
    //e faccio tornare gli elementi che sono inclusi.
    searchAlbums(searchText){
      this.filteredAlbums = this.albums.filter((element)=>{
        return element.title.includes(searchText);
      })
    }
  }
}
</script>

<style lang="scss">
@import "./style/app.scss"
</style>
