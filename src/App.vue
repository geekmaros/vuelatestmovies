<template>
  <div id="app">
    <Header :title='movieTitle' />
    <transition name="fade">
    <router-view />
     </transition >
    <Footer :dev='dev'/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  data(){
  return{
    dev: 'geekmaros',
    movieTitle: 'MovieManiac 🎥'
    }
  },
  components: {
    Header,
    Footer,
  },

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
}
.fade-enter-active, .fade-leave-active{
 transition: all 0.3s ease;
}

.fade-enter, .fade-leave-to{
  opacity:0;
  transition: scale(0)
}
</style>
