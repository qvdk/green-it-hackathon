<template>
  <v-row dense>
    <Video
      :video="category.video"
      :poster="category.videoPoster"
    >
    </Video>
    <v-col
      v-for="product in products"
      :key="product.name"
      cols="12"
      sm="12" md="6" lg="4"
    >
      <Product :product="product" />
    </v-col>
  </v-row>
</template>

<script>
import Product from '../components/Product.vue';
export default {
    name: "CategoryPage",
    components: { Product },
    data () {
      return {
        category: {
          name: 'Carré potager',
          videoPoster: 'video_preview.webp',
          video: 'flower.webm'
        },
        products: [
          {
            name: "Carré potager MON PETIT POTAGER L.75 x l.35 x H.36cm",
            image: "product1.webp",
            description: "La JARDINIERE DESIGN est un potager au naturel idéal...",
            rate: 3.2,
            rateCount: 10,
            price: 59.0
          },
          {
            name: "Terreau universel GEOLIA, 50l",
            image: "product2.webp",
            description: "Pour toutes plantes, favorise la reprise et la croissance des végétaux.",
            rate: 4.5,
            rateCount: 189,
            price: 4.90
          }
        ]
      }
    }
}
</script>
