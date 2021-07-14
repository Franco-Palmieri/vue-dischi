<template>
    <div class="nav">
      <div class="logo">
        <img src="../assets/spotify-logo.png" alt="">
      </div>
    </div>
</template>

<script>

export default {
  name: 'Header',
  components: {
  }
}
</script>

<style lang="scss">
.nav{
  height: 50px;
  background-color: rgb(47, 47, 85);
  display: flex;
  align-items: center;
  .logo{
    display: flex;
    align-items: center;
    img{
      width: 50px;
    }
  }
}
</style>
