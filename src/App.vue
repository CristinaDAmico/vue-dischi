<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'App',
  components: {
      Header,
      Main,
  }
}
</script>

<style lang="scss">
@import "~@fontsource/lato/index.css";
@import "~@fontsource/lato/700.css";

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Lato', sans-serif;
}

</style>
