<template>
  <main class="container">
        <section id="album-container">
            <SectionAlbums/>
        </section>
      </main>
</template>

<script>
import axios from "axios";
import SectionAlbums from "@/components/SectionAlbums.vue";
export default {
components: {
    SectionAlbums,
},
created() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) => {
        console.log(res.data);
        // const albums = res.data.response
    });
}
}
</script>

<style>

</style>