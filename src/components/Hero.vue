<template>
  <div class="heroBlock">
    <v-carousel :height="height" :show-arrows="arrows" cycle>
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row class="title fill-height" align="center" justify="center">
          <div class="white--text"  align="center" justify="center">
            <p class="title-hero">{{ slides[i] }}</p>
          </div>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      items: [
        {
          src:
            "https://demo.mikado-themes.com/onyx24/wp-content/uploads/2015/03/b-img-top-10-locations.jpg",
        },
        {
          src:
            "https://hausratversicherungkosten.info/wp-content/uploads/2019/01/Design-Tv-Cabinet-Living-Room-Surprising-Designs-Simple.jpg",
        },
        {
          src:
            "https://image.freepik.com/foto-gratis/hombre-carpintero-lijando-madera-lijadora-orbital-taller_23-2147944826.jpg",
        },
        {
          src:
            "https://images.unsplash.com/photo-1598546720078-8659863bc47d?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
        },
        {
          src:
            "https://image.freepik.com/foto-gratis/sala-trabajo-lujo-oficina-ejecutiva_105762-1725.jpg",
        },
      ],
      slides: [
        "Carpenfred es Carpintería",
        "Modernidad y Elegancia",
        "Somos Profesionales",
        "Diseños a medida",
        "Calidad",
      ],
    };
  },
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return "auto";
        case "sm":
          return "auto";
        case "md":
          return "auto";
        case "lg":
          return 500;
        case "xl":
          return 500;
      }
    },
    arrows() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return false;
        case "sm":
          return false;
        case "md":
          return false;
        case "lg":
          return true;
        case "xl":
          return true;
      }
    },
  },
};
</script>

<style lang="css" scoped>
@media screen and (max-width: 600px) {
  .title-hero {
    font-size: 1.4rem;
  }
}
</style>
