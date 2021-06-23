<template>
  <div class="block latestPostBlock">
    <v-container>
      <h2 class="text-center">Servicios Adicionales</h2>
      <v-row>
        <v-col cols="12" md="4" v-for="item in items" :key="item.id">
          <v-card class="mx-auto" outlined>
            <v-img
              class="white--text align-end"
              height="200px"
              :src="item.src"
            >
              <v-card-title>{{item.title}}</v-card-title>
            </v-img>

            <v-card-subtitle class="pb-0"> {{item.subtitle}} </v-card-subtitle>

            <v-card-text class="text--primary">
              <div>{{item.description}}</div>
            </v-card-text>

            <v-card-actions>
              <v-btn color="#44546A" text> Share </v-btn>

              <v-btn color="#44546A" text> Explore </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>


<script>
export default {
  name: "LastPost",
  data: () => ({
    show: false,
    items: [
      {
        id: 1,
        title: "Techos de Madera",
        subtitle: "Una mirada al Cielo",
        description: "Los techos de madera o machiembrado nunca pasan de moda, brindan un toque de elegancia a su hogar. Carpenfred puede instalarlos usando una tonalidad del color de la madera a su gusto.",
        src: "http://www.sivilima.lk/img/ceiling/sivilima-b-groove-ceiling.jpg"
      },
      {
        id: 2,
        title: "Pisos Flotantes",
        subtitle: "Elegancia para sus pies",
        description: "Si desea dar un toque de modernidad a su hogar, los pisos flotantes son una excelente opción. Carpenfred puede ayudarlo en la instalación de sus pisos flotantes!",
        src: "https://www.carpet2go.com/wp-content/uploads/2019/02/FI-Background.jpg"
      },
      {
        id: 3,
        title: "Restauraciones",
        subtitle: "Modernidad para su Hogar",
        description: "¿Desea renovar puertas viejas, marcos, rodapies o cualquier tipo mueble? No dude en contactarnos para hacernos cargos de sus proyectos de renovación.",
        src: "https://www.safedepositsscotland.com/blog-admin/wp-content/uploads/2019/01/repairs-1200x675.jpg"
      }
    ]
  })

};
</script>