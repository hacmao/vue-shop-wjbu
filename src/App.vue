<template>
  <v-app>
    <Header/>
    <router-view></router-view>
    <Footer/>
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: "App",
  components: {
    'Header': Header,
    'Footer': Footer
  }
}
</script>
