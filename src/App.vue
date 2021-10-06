<template>
  <v-app App>
    <Navbar />
    <v-flex d-flex>
      <v-layout wrap>
        <v-flex
          md4
          v-for="(personaje, index) in $store.state.personajes"
          :key="index"
        >
          <v-card class="container ma-4">
            <v-img height="350" :src="personaje.imagen"></v-img>
            <v-card-title>{{ personaje.nombre }}</v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue"

export default {
  name: "App",
  components:{
    Navbar
  },
  data: () => ({
    //
  }),
  
};
</script>
