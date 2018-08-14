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
    PageHeader, PageFooter
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto');

html, body {
  width: 100vw;
  min-height: 100vh;
  background: #f8f8f8;
}
#__nuxt, #__layout, .main{
  height: 100%;
}
div{
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
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
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
}
</style>
