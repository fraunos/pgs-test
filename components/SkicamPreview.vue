<template>
<div class="skicam">
  {{skicam.name}}
  <img :src="currentImage" alt="">
</div>
</template>
<script>
export default {
  props: ['skicam'],
  created() {
    this.skicam.cams = Object.keys(this.skicam.cams).map(key => this.skicam.cams[key])
    let self = this
    setInterval(function () {
      self.counter++
    }, 5000)
  },
  data() {
    return {
      counter: 0
    }
  },
  computed: {
    currentImage() {
      return this.skicam.cams[this.counter % this.skicam.cams.length].url
    }
  }
}
</script>

<style>
img {
  height: 200px;
  width: 200px;
}
</style>
