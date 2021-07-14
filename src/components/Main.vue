<template>
    <div class="main">
        <!-- Spalmo il props per inviarlo al componente Album -->
        <Album v-for="(album, index) in albums" :key="index"
        :poster="album.poster"
        :title="album.title"
        :author="album.author"
        :year="album.year"
        />
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

</style>
