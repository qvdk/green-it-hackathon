<template>
  <div>
    <h2>Product Category</h2>
    <v-container style="min-width: 260px">
      <v-row style="text-align: center" dense>
        <v-col v-for="category in categories" :key="category.id" cols="6" xs="6" sm="3" md="3" lg="3" xl="3">
          <img :src="category.url" :alt="category.alt" />
          <br/>
          {{ category.alt }}
        </v-col>
      </v-row> 
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => {
    return{
      categories: [
       { url: 'contenant.webp', alt: 'Containers' },
       { url: 'outil.webp', alt: 'Tools' },
       { url: 'plantation.webp', alt: 'Plantations' },
       { url: 'substrat_alternative.webp', alt: 'Substract Alternative' }
      ]
    }
  }
}
</script>