<template>
  <div class="album">
      <div class="image">
          <img :src="info.poster" :alt="info.poster">
      </div>
      <div class="title">{{ info.title }}</div>
      <div class="author">{{ info.author }}</div>
      <div class="year">{{ info.year }}</div>
      <div class="genre">{{ info.genre }}</div>
  </div>
</template>

<script>
export default {
    name: 'Album',
    props: ['info'],
}
</script>

<style lang="scss" scoped>

.album {
    height: 300px;
    flex-basis: calc(100% / 8);
    background-color: #2e3a46;
    text-align: center;
    margin: 20px 10px;
    .image {
    height: 150px;
    padding: 10px;
        img {
            height: 100%;
        }
    }
    .title {
        text-transform: uppercase;
        color: #fff;
        margin: 10px 0;
    }
    .author,
    .year  {
        color: #4e5961;
    }
    .genre {
        color: #fff;
    }
}


</style>