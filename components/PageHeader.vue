<template>
  <header class="">
    <div class="logo">
      LOGO
    </div>
    <nav>
      <nuxt-link v-for="(route, index) in routes" :key="index" :to="route.url">{{route.name}}</nuxt-link>
    </nav>
  </header>
</template>
<script>
export default {
  data () {
    return {
      routes: [
        {
          name: 'About us',
          url: '/'
        },
        {
          name: 'Skicams',
          url: '/skicams'
        },
        {
          name: 'Contact',
          url: '/contact'
        }
      ]
    }
  }
}
</script>

<style>
</style>
