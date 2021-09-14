<template>
  <div id="app">
    <Navbar></Navbar>
    <router-view/>
    <Footer></Footer>
  </div>
</template>

<script>
import axios from 'axios'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',

  components: {
    Navbar,
    Footer,
  },

  beforeCreate(){
    this.$store.commit('initializeStore')

    const token = this.$store.state.user.token

    if(token){
      axios.defaults.headers.common['Authorization'] = "Token " + token
    } else {
      axios.defaults.headers.common['Authorization'] = ""
    }
  }
}
</script>

<style lang="scss">
@import '../node_modules/bulma';

</style>
