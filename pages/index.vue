<template>
    <v-row dense>
      <Video
        :video="category.video"
        :poster="category.videoPoster"
      >
      </Video>
      <Category />
      <Gallery />
      <Team />
    </v-row>
</template>

<script>
export default {
  data () {
    return {
      category: {
        name: 'Carré potager',
        videoPoster: 'video_preview.webp',
        video: 'flower.webm'
      }
    }
  }
}
</script>
