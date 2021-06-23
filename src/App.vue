<template>
  <v-app>
    <v-app-bar app color="#343A40" max-height="65" style="border-bottom: 3px solid #FFC000;">
        <Header/>
    </v-app-bar>
      <router-view></router-view>        
    <v-footer>
      <Footer/>
    </v-footer>
  </v-app>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
