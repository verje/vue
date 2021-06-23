<template>
  <v-main>
    <v-container>
      <div class="block text-center notFound">
        <h1>Lo sentimos, la página que busca no se encuentra en este sitio web</h1>
        <img src="../assets/images/notfound.gif" height="50px" />
        
      </div>
    </v-container>
  </v-main>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";

export default {
  name: "Home",
  components: {
    Header,
  },
};
</script>
