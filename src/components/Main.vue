<template>
  <main class="container">
        <section id="album-container">
            <div class="card" v-for="(album, index) in albums" :key="index">
                <SectionAlbums :album="album"/>
            </div>
        </section>
      </main>
</template>

<script>
import axios from "axios";
import SectionAlbums from "@/components/SectionAlbums.vue";
export default {
    data() {
        return{
            albums: []
        }
    },
components: {
    SectionAlbums,
},
created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) => {
        this.albums = res.data.response;
    });
}
}
</script>

<style>

</style>