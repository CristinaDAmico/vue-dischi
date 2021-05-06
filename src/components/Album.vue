<template>
  <div class="album">
      <div class="image">
          <img :src="info.poster" :alt="info.poster">
      </div>
      <div>{{ info.title }}</div>
      <div>{{ info.author }}</div>
      <div>{{ info.year }}</div>
      <div>{{ info.genre }}</div>
  </div>
</template>

<script>
export default {
    name: 'Album',
    props: ['info'],
}
</script>

<style lang="scss" scoped>
img {
    height: 50px;
}
.album {
    flex-basis: calc(100% / 8);
}
</style>