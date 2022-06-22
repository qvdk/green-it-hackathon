<template>
  <v-container>
    <h2>Product Category</h2>
    <v-container style="min-width: 260px">
      <v-row style="text-align: center" dense>
        <v-col v-for="category in categories" :key="category.id" cols="6" xs="6" sm="3" md="3" lg="3" xl="3">
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
       { url: 'contenant.webp', alt: 'Containers', route: '/category' },
       { url: 'outil.webp', alt: 'Tools', route: '/category' },
       { url: 'plantation.webp', alt: 'Plantations', route: '/category' },
       { url: 'substrat_alternative.webp', alt: 'Substract Alternative', route: '/category' }
      ]
    }
  }
}
</script>
