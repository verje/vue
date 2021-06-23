<template>
  <v-main>
    <Hero/>
    <Gallery/>
    <LastPost/>
  </v-main>
</template>

<script>
import Hero from '../components/Hero.vue';
import Gallery from '../components/Gallery.vue';
import LastPost from '../components/LastPost.vue';
export default {
  name: 'Home',
  components: {
    Hero,
    Gallery,
    LastPost
  }
}
</script>
