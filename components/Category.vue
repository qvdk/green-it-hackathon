<template>
  <div>
      <img v-for="image in images" :src="image.url" :alt="image.alt" />
  </div>
</template>

<script>
export default {
  data: () => {
    return{
      images: [
       { url: 'contenant.webp', alt: 'Containers' },
       { url: 'outil.webp', alt: 'Tools' },
       { url: 'plantation.webp', alt: 'Plantations' },
       { url: 'substrat_alternative.webp', alt: 'Substract Alternative' }
      ]
    }
  }
}
</script>