<template>
  <v-container class="text-center">
    <div class="text-h6">Solelia sublime votre jardin</div>
    <video controls :poster="poster" preload="none" style="max-width: 700px; width: 100%;">
      <source :src="video" />
      Votre navigateur ne supporte pas les vidéos embarquées.
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
