<template>
      <div class="album">
        <div class="inner">
          <div class="album-picture">
            <img :src="poster" alt="">
          </div>
          <div class="album-title">
            {{title}}
          </div>
          <div class="album-info">
            <div class="album-author">
              {{author}}
            </div>
            <div class="year">
              {{year}}
            </div>
          </div>  
        </div>
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
.album{
    text-align: center;
    width: calc(100% / 5);
    padding: 15px;
    .inner{
      height: 100%;
      padding: 15px;
      background-color: rgb(47, 47, 85);
      .album-picture{
        img{
          width: 100%;
        }
      }
      .album-title{
        margin: 10px 0;
      }
      .album-info{
        font-size: 12px;
        color: #ccc
      }
    }
  }
</style>
