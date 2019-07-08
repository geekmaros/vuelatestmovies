<template>
	<header>
		<h3><router-link to="/"> {{ title }} </router-link>
    </h3>
    <transition name="fade">
      <h1 v-if="show">Checkout Our Latest Movies</h1>
  </transition >
   <button @click="show = !show">🎥 show/hide</button>
	</header>
</template>

<script>
export default {

  name: 'Header',

  data() {
    return {
      show: false
    };
  },
  props:{
   title:String
  }
};
</script>

<style lang="css" scoped>
header{
	background-color: #111;
	padding: 20px;
	color: white;
}
.fade-enter-active, .fade-leave-active{
 transition: all 0.3s ease;
}

.fade-enter, .fade-leave-to{
  opacity:0;
  transition: scale(0)
}
a:link, a:hover, a:visited, a:active{
  color: rgb(255, 2, 221);
  text-decoration: none
}
</style>
