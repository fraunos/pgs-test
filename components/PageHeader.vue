<template>
  <header class="">
    <div class="container">
      <div class="logo">
        LOGO
      </div>
      <nav>
        <div>
          <nuxt-link v-for="(route, index) in routes" :key="index" :to="route.url">{{route.name}}</nuxt-link>
        </div>
      </nav>
    </div>
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

<style scoped>
header{
  width: 100%;
  height: 100%;
  font-size: 1.6vh;
  text-transform: uppercase;
  letter-spacing: -.05em;
  font-weight: bold;
  box-sizing: border-box;
  border-bottom: solid .2em #0001;
  display: flex;
  justify-content: center;
  margin-bottom: 3em;
  background: white;
}
nav div{
  height: 100%;
  padding-bottom: .5em;
  box-sizing: content-box;
}
nav a {
  margin-right: 4.2em;
  padding-bottom: .5em;
  text-decoration: none;
}
nav a:last-child{
  margin-right: 0;
}
a, a:active{
  color: #0009;
}
.nuxt-link-exact-active{
  color: #fa8a23ff;
  border-bottom: solid .2em #fa8a23ff;
}
.logo{
  font-size: 4.8em;
  height: 2em;
}
</style>
