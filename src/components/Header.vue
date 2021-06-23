<template>
  <v-container>
    <v-toolbar
      flat
      class="mainHeader"
      color="#343A40"
      style="border-bottom: 3px solid #ffc000"
    >
      <v-toolbar-title style="color: #ffc000">
        <v-row justify="center" align="center">
          <v-col cols="3">
            <router-link to="/">
              <v-img
                max-height="80"
                max-width="80"
                src="../assets/images/LogoCarpenfred.png"
                alt="Carpenfed"
              ></v-img> </router-link
          ></v-col>
          <v-col cols="9"><span class="title-logo">Carpenfred</span></v-col>
        </v-row>
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn text>
          <router-link to="/" style="color: #ffc000">Inicio</router-link>
        </v-btn>
        <v-btn text color="#719D5A">
          <router-link to="/about" style="color: #ffc000">Quienes Somos</router-link>
        </v-btn>
        <v-btn text color="#719D5A">
          <router-link to="/contact" style="color: #ffc000"
            >Contáctenos</router-link
          >
        </v-btn>
      </v-toolbar-items>
      <div class="hidden-sm-and-up">
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
          </template>
          <v-list class="responsiveMenu">
            <v-list-item>
              <v-list-item-title
                ><router-link to="/">Inicio</router-link></v-list-item-title
              >
            </v-list-item>
            <v-list-item>
              <v-list-item-title
                ><router-link to="/about">Quienes Somos</router-link></v-list-item-title
              >
            </v-list-item>
            <v-list-item>
              <v-list-item-title
                ><router-link to="/contact"
                  >Contáctenos</router-link
                ></v-list-item-title
              >
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
  name: "Header",

  data: () => ({}),
  computed: {
    fontSize() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return "3em";
        default:
          return "5em";
      }
    },
  },
};
</script>

<style lang="css" scoped>
@media screen and (max-width: 600px) {
  .title-logo {
    font-size: 0.8rem;
  }
}
</style>
