<template>
  <v-app>
    <v-app-bar
      fixed
      app
    >
      <a href="/"><v-img src="solelia.webp" max-width="28" /></a>
      <v-spacer />
      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>Solelia - Incubateur EuraTechnologies, 165 Av. de Bretagne, 59000 Lille - France</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      fixed: false,
      title: 'Solelia'
    }
  }
}
</script>
