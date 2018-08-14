<template>
<div class="main">
  <page-header></page-header>
  <nuxt/>
  <page-footer></page-footer>
</div>
</template>

<script>
import PageHeader from '~/components/PageHeader.vue'
import PageFooter from '~/components/PageFooter.vue'

export default {
  components: {
    PageHeader,
    PageFooter
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto');

html,
body {
  width: 100%;
  min-height: 100vh;
  background: #f8f8f8;
}

body>div {
  height: 100%;
}

.main {
  min-height: 100vh;
}

div {
  width: 100%;
}

.main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

html {
  color: #0009;
  font-family: Roboto, Arial, sans-serif;
  font-size: 2vh;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  width: 65vw;
}

section {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100%;
  flex: 1 1 auto;
}

a {
  outline: none;
}

@media screen and (max-aspect-ratio: 1/1) {
  .skicam,
  .card {
    width: 100% !important;
    height: auto;
  }
  .container {
    width: 90vw;
  }
}
</style>
