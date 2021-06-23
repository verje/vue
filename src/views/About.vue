<template>
  <v-main>
    <div class="staticHero">
      <v-img
        src="https://s3-ap-south-1.amazonaws.com/muqawiloon/category_metadata/banners/000/000/354/original/Wood-Carpentry.png?1472945903"
      >
        <v-row align="end" class="ligthbox white--text pa-2 fill-height">
          <v-col cols="12">
            <v-container>
              <div class="headline">About Us</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <p>
          <h4>Carpenfred es una carpintería con mas de 25 años de experiencia en el
          mercado venezolano, por eso entendemos lo valioso de su tiempo y
          sabemos que para ud, cualquier trabajo de carpintería es mas que un
          Proyecto, es un sueño que desea hacer realidad… Cuente con nosotros
          para hacer su proyecto, su sueño una realidad!</h4>
        </p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Equipo de Trabajo</h2>
        <v-row>
          <v-col cols="12" md="3" sm="6" v-for="item in items" :key="item.id">
            <v-card class="mx-auto" max-width="400">
              <v-img
                class="white--text align-end"
                height="200px"
                :src="item.src"
              >
              </v-img>

              <v-card-text class="text--primary">
                <div class="title">{{ item.name }}</div>
                <p>{{ item.title }}</p>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="block">
      <h2 class="text-center">Ubicación Carpenfred</h2>
      <div class="googlemap">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1961.6491476001631!2d-67.01860014504017!3d10.477134549953119!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8c2a6016edcdb61b%3A0x3167dd64336fffd!2sCentro%20comercial%20el%20castillo!5e0!3m2!1ses!2sco!4v1616634601061!5m2!1ses!2sco"
          width="100%"
          height="450"
        ></iframe>
      </div>
    </div>
  </v-main>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/carpenfred.png"),
          name: "Freddy",
          title: "Maestro Carpintero",
        },
        {
          id: 2,
          src: require("../assets/images/emp1.png"),
          name: "Jimmy",
          title: "Carpintero",
        },
        {
          id: 3,
          src: require("../assets/images/emp3.png"),
          name: "Alvaro",
          title: "Ayudante de Carpintería",
        },
        {
          id: 4,
          src: require("../assets/images/emp4.png"),
          name: "Alexis",
          title: "Ayudante de Carpintería",
        },
      ],
    };
  },
};
</script>
