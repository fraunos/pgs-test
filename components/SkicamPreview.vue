<template>
<div class="skicam">
  <div class="date">{{currentDate}}</div>
  <h1>
    {{skicam.name}}
  </h1>
  <!-- <div class="img" :style="`background-image: url(${currentImage});`"></div> -->
  <img :src="currentImage" alt="" @mouseenter="hover=true" @mouseleave="hover=false">
</div>
</template>

<script>
import moment from 'moment'

export default {
  props: ['skicam'],
  created() {
    this.skicam.cams = Object.keys(this.skicam.cams).map(key => this.skicam.cams[key])
    let self = this
    setInterval(function () {
      if (self.hover) {
        self.counter++
      }
    }, 1000)
  },
  data() {
    return {
      counter: 0,
      hover: false
    }
  },
  computed: {
    currentImage() {
      return this.skicam.cams[this.counter % this.skicam.cams.length].url
    },
    currentDate() {
      return moment().format('DD-MM-YYYY');
    }
  }
}
</script>

<style>
.skicam {
  background: white;
  width: 48%;
  margin: 1%;
  height: auto;
  text-align: right;
  box-shadow: 0px 1px 4px #0003;
  border-radius: .2em;
}

.skicam .date {
  padding: .5em .5em 0 .5em;
  color: #0005;
  font-size: 90%;
}

.skicam img {
  width: 100%;
  height: auto;
}

.skicam h1 {
  text-align: center;
  margin-bottom: .5em;
}

.desc {
  background: white;
  padding: 2em 1em;
}
</style>
