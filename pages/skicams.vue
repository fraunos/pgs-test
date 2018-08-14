<template>
<section class="container">
  <div v-if="skicamsFiltered">
    <skicam-preview v-for="(skicam, index) in skicamsFiltered" :key="index" :skicam="skicam"></skicam-preview>
  </div>
</section>
</template>

<script>
import SkicamPreview from '~/components/SkicamPreview.vue'

export default {
  components: {
    SkicamPreview
  },
  mounted() {
    this.fetchSkicams()
  },
  data() {
    return {
      skicams: null,
      filter: ['Andalo', 'Monte Bondone']
    }
  },
  computed: {
    skicamsFiltered() {
      // return this.skicams.filter((item) => this.filter.indexOf(item.name) > -1 ? true : false)
      return this.skicams.slice(0, 10)
    }
  },
  methods: {
    async fetchSkicams() {
      const skicams = await this.$axios.$get('https://makevoid-skicams.p.mashape.com/cams.json', {
        headers: {
          'X-Mashape-Key': 'kxSXmUymofmshFHhhKxWOSJpqJsJp1I3zNnjsnqKwhITAiC1zw'
        }
      })
      this.skicams = Object.keys(skicams).map(key => skicams[key])
    }
  }
}
</script>

<style>

</style>
