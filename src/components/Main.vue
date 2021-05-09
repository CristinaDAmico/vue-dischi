<template>
  <main>
      <section v-if="!loading" class="albums">
          <Album 
            v-for="(album, index) in albums" 
            :key="index" 
            :info="album"
            />
      </section>
      <Loader v-else />
  </main>
</template>

<script>
import axios from 'axios';
import Album from '@/components/Album.vue';
import Loader from '@/components/Loader.vue';

export default {
    name: 'Main',
    components: { 
        Album,
        Loader
        },
        data() {
            return {
                apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
                albums: [],
                loading: true,
            }
        },
        created() {
            this.getAlbums();
        },
        methods: {
            getAlbums() {
                // API call
                axios.get(this.apiURL)
                .then(res => {
                    //console.log( res.data );
                    this.albums = res.data.response;
                    this.loading = false;
                })
                .catch(err => {
                    console.log('Error', err);
                });
            },
        },
};
</script>

<style lang="scss" scoped>
main {
    background-color: #1d2d3c;
    .albums {
    padding: 50px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    }
}

</style>