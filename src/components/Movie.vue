<template>
	<div>
		 
		<router-link :to="moviePath">
      <img :src="posterImage" :alt="indMovies.title">
    </router-link>
		<h4>{{ indMovies.title }}</h4>

	</div>
</template>

<script>
const POSTER_PATH = 'http://image.tmdb.org/t/p/w154'

export default {

  name: 'Movie',

  data() {
    return { 

    };
  },
  props: ['indMovies'],

  computed:{
  posterImage: function () {

   return `${POSTER_PATH}/${this.indMovies.poster_path}`
  },
  moviePath: function () {
     return `/movie/${this.indMovies.id}`;
  }
 
 }
};
</script>

<style lang="css" scoped>
img{
	box-shadow: 0 0 35px black;
}
</style>
