<template>
    <div class="main">
        <div class="container">
            <div class="row">
                <!-- Spalmo il props per inviarlo al componente Album -->
                <Album class="album-container" v-for="(album, index) in albums" :key="index"
                :poster="album.poster"
                :title="album.title"
                :author="album.author"
                :year="album.year"
                />
            </div>
        </div>
    </div>
</template>

<script>
import Album from "./Album.vue"

export default {
  name: 'Main',
  components: {
      Album,
  },
  props:{
      albums: Array,
  }
}
</script>

<style lang="scss">
.main{
    height: calc(100vh - 50px);
    background-color: rgb(27, 39, 37);
    color: white;
}

</style>
