<template>
  <v-card
    class="d-flex flex-row"
  >

    <v-img max-width="30%" max-height="200" :src="product.image" loading="lazy"></v-img>

    <v-card>

        <v-card-title class="text-subtitle-1">{{ product.name }}</v-card-title>

        <v-card-text>
          <v-row
            align="center"
            class="mx-0"
          >
            <v-rating
              :value="product.rate"
              color="amber"
              dense
              half-increments
              readonly
              size="14"
            ></v-rating>

            <div class="grey--text ms-4 text-xs">
              {{ product.rateCount }}
            </div>
          </v-row>

          <div class="my-4 mb-0 text-h6 green--text">
            <span>{{ product.price | currencyEuro }}</span>
          </div>

          <div class="text-xs">{{ product.description }}</div>
        </v-card-text>

        <v-card-actions>
          <v-spacer />
          <v-btn
            color="indigo"
            @click="addToCart(product)"
          >
            Acheter
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-card>
</template>

<script>
export default {
  name: 'Product',
  props: {
    product: {
      type: Object,
      require: true
    }
  },
  filters: {
    currencyEuro (value) {
      return new Intl.NumberFormat("en-US", { style: "currency", currency: "EUR" }).format(value);
    }
  },
  methods: {
    addToCart(product) {
      alert(product.name + ' ajouté au panier')
    }
  }
}
</script>

<style scoped>
.v-card__subtitle, .v-card__text, .v-card__title {
    padding: 2px;
    padding-left: 8px;
}
</style>
