<template>
  <div id="app">
    <v-toolbar extended class="mb-3" color="pink">
      <v-toolbar-side-icon></v-toolbar-side-icon>
      <v-toolbar-title>Desafio</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn text>Inicio</v-btn>
        <v-btn text>Buscar</v-btn>
        <v-btn text>Acerca de</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-card
      mt4 ma3
      max-width="374"
      v-for="(personaje, index) in $store.state.personajes"
      :key="index"
    >
      <v-img height="250" :src="personaje.imagen"></v-img>
      <v-card-title>{{ personaje.nombre }}</v-card-title>
    </v-card>

    <v-flex d-flex>
      <v-layout wrap>
        <v-flex md4 v-for="(personaje, index) in $store.state.personajes"
            :key="index">
          <v-card
            class="card-container"
          >
            <v-img height="250" :src="personaje.imagen"></v-img>
            <v-card-title>{{ personaje.nombre }}</v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-flex>
  </div>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
