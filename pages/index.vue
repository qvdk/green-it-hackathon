<template>
  <v-container>
    <Video
      :video="category.video"
      :poster="category.videoPoster"
    >
    </Video>
    <Category />
    <Gallery />
    <Team />
  </v-container>
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
