<template>
  <v-footer padless>
    <v-card
      flat
      tile
      class="lighten-1 white--text text-center"
      style="background-color: #f4f0cb"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon.id"
          class="mx-4"
          icon
        >

            <a :href="icon.target" :target="icon.target"><v-icon style="color: #343A40" size="24px">{{ icon.icon }}</v-icon></a>
        </v-btn>
      </v-card-text>

      <v-card-text class="pt-0" style="color: #44546a">
        Carpenfred ofrece servicios de carpintería en general. Estamos ubicados
        en el km 13 vía el Junquito, Caracas-Venezuela. Con gusto atenderemos su
        solicitud de forma personalizada, solo póngase en contacto con nosotros
        a través de nuestros diferentes medios.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text style="color: #44546a">
        {{ new Date().getFullYear() }} — <strong>Carpenfred</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: [
      {
        id: 1,
        target: "https://instagram.com",
        icon: "mdi-instagram",
      },
      {
        id: 2,
        target: "https://whatsapp.com",
        icon: "mdi-whatsapp",
      },
      {
        id: 3,
        target: "https://twitter.com",
        icon: "mdi-twitter",
      },
    ],
  }),
};
</script>
