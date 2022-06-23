<template>
  <v-container>
    <v-card outlined color="transparent">
      <div class="text-h5">Des solutions durables comme responsable ...</div>
      <v-img
        src="advice1.webp"
      >
      </v-img>
      <v-card-text>
        Mon Petit Potager a fait le choix de s'investir durablement pour l'environnement.
      </v-card-text>
      <v-card-actions>
        <v-btn to="/advices" nuxt color="indigo">
          En savoir plus
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    name: 'Galery',
    data () {
      return {
        items: [
          {
            src: 'advice1.webp',
          },
          {
            src: 'advice2.webp',
          },
          {
            src: 'advice3.webp',
          },
          {
            src: 'advice4.webp',
          },
        ],
      }
    },
  }
</script>
