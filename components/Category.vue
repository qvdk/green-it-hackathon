<template>
  <v-container>
    <div class="text-h5">Catégorie produits</div>
    <v-container style="min-width: 260px">
      <v-row style="text-align: center" dense>
        <v-col v-for="category in categories" :key="category.id" cols="6" sm="3" md="3" lg="3" xl="3">
          <a :href="category.route"><img :src="category.url" :alt="category.alt" /></a>
          <br/>
          {{ category.alt }}
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  data: () => {
    return{
      categories: [
       { url: 'contenant.webp', alt: 'Contenants', route: '/category' },
       { url: 'outil.webp', alt: 'Outils', route: '/category' },
       { url: 'plantation.webp', alt: 'Plantations', route: '/category' },
       { url: 'substrat_alternative.webp', alt: 'Substrat alternatif', route: '/category' }
      ]
    }
  }
}
</script>
