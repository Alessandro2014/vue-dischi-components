<template>
    <div> 
        <img :src="album.poster" :alt="album.title" />
        <h2  class="title">{{ album.title }}</h2>
        <address class="author">{{ album.author }}</address>
        <time :datetime="album.year" class="year">{{ album.year }}</time>
    </div>
   
</template>

<script>
export default {
name: "SectionAlbums",
props: ['album']
};
</script>

<style>

</style>