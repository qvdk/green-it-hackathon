<template>
  <v-container>
    <div class="text-h5">Magic Team</div>
    <v-container>
      <v-row style="text-align: center" no-gutters>
        <v-col v-for="member in members" :key="member.id">
          <img :src="member.url" :alt="member.alt" loading="lazy" />
          <br/>
          {{ member.alt }} - {{ member.desc }}
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  data: () => {
    return{
      members: [
       { url: 'sheldon_cooper.webp', alt: 'Sheldon Cooper', desc: 'Not happy' },
       { url: 'hermione.webp', alt: 'Hermione', desc: 'Magician' },
       { url: 'steve_jobs.webp', alt: 'Steve Jobs', desc: 'Love my IPhone' },
       { url: 'pascale.webp', alt: 'Pascale Le Gigan', desc: 'Add CSG in footer' }
      ]
    }
  }
}
</script>
