<template>
  <section class="container">
    <div class="cards">
      <div v-for="n in 3" :key="n" class="card">
        <div class="img">
        </div>
        <div class="desc">
          <h1>{{lorem.head}}</h1>
          <p>{{lorem.body}}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  components: {
  },
  data () {
    return {
      lorem: {
        head: 'Lorem ipsum',
        body: 'Etiam ullamcorper. Suspendisse a pellentesque dui, non felis maecenas.'
      }
    }
  }
}
</script>

<style>
</style>
