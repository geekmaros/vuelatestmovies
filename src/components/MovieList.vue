<template>
	<div >
		<ul>
			<li v-for="movie in movies">
				<Movie :indMovies="movie"/>
				
			</li>
		</ul>
	</div>
</template>

<script>
import Movie from './Movie.vue'
export default {

  name: 'MovieList',

  data() {
    return {
    movies:[],
    maker:'cruz'
    };
  },
  created: function (){
   this.fetchData()
  },
  methods:{
   fetchData: async function(){
    try{
     const res = await fetch('https://api.themoviedb.org/3/discover/movie?sort_by=popularity.desc&api_key=549f1372691531cd712f4460b0e1798a')
     const movie = await res.json()
     this.movies = movie.results

    }catch(e){
       console.log(e)
    }
   }
  },
  components:{
  Movie
  }

};
</script>

<style lang="css" scoped>
ul{
	display: grid;
	list-style: none;
	padding: 1rem; 
	margin: 0;
	grid-row-gap: 1rem;
	grid-template-columns: repeat(5, 1fr);
  justify-content: center;
}
</style>
