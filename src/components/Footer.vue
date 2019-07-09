<template>
	<footer>
		<h3> ☕ & code by 😎       <a href="https://github.com/geekmaros">geekmaros</a>
 </h3>
			
	</footer>
</template>

<script>
export default {

  name: 'Footer',

  data() {
    return {
    };
  },
  props:{
  dev: String
  }
};
</script>

<style lang="css" scoped>
footer{
	background-color: #111;
	padding: 20px;
	color: white;
}
a:link, a:hover, a:visited, a:active{
  color: rgb(255, 2, 221);
  text-decoration: none
}
</style>
