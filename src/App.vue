<template>
  <div id="app">
    <Header />
    <!-- Invio props albums al main -->
    <Main :albums="albums"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import axios from "axios"

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data (){
    return {
      albums: [],
    }
  },
  created (){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((result) =>{
      this.albums = result.data.reponse;
    })
  }
}
</script>

<style lang="scss">
@import "./style/app.scss"
</style>
