<template>
   <header>
        <div class="container">
          <img src="@//assets/img/logo.png" />
          <select v-model="selecteGenre">
            <option>All</option>
            <option v-for="(genre, index) in genreList" :key="index">{{ genre }}</option>
          </select>
        </div>
      </header>
</template>

<script>
export default {
name: 'Header',
}
</script>

<style>

</style>