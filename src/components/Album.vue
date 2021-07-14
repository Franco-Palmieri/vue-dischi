<template>
    <div class="album">
        {{author}}
    </div>
</template>

<script>

export default {
  name: 'Album',
  components: {
  },
  props: {
    author: String,
    year: String,
    title: String,
    poster: String
  }
}
</script>

<style lang="scss">

</style>
