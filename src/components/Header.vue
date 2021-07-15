<template>
    <div class="nav">
      <div class="logo">
        <img src="../assets/spotify-logo.png" alt="">
      </div>
      <div class="input-search">
        <input type="text" placeholder="Search" v-model="searchText">
        <button @click="$emit('search', searchText)">Search</button>
        <!-- Quando clicca il bottone l'input invia il search all'app.vue attraverso l'emit -->
      </div>
    </div>
</template>

<script>

export default {
  name: 'Header',
  components: {
  },
  data(){
    return {
      searchText: "",
    }
  },
}
</script>

<style lang="scss">
.nav{
  height: 50px;
  background-color: rgb(47, 47, 85);
  display: flex;
  align-items: center;
  justify-content: space-between;
  .logo{
    display: flex;
    align-items: center;
    img{
      width: 50px;
    }
  }
}
</style>
