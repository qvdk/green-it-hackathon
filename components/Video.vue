<template>
  <v-container class="text-center">
    <video controls :poster="poster" preload="none" width="100%" style="max-width: 700px">
      <source :src="video" />
      Votre navigateur ne supporte pas les vidéos embarqués.
    </video>
  </v-container>
</template>

<script>
export default {
  name: 'Video',
  props: {
    video: {
      type: String,
      require: true
    },
    poster: {
      type: String,
      require: true
    }
  }
}
</script>
