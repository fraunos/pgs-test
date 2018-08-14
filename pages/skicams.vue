<template>
<section class="container">
  <div>
    skicams
  </div>
</section>
</template>

<script>
export default {
  components: {},
  methods: {
    async fetchSomething() {
      const ip = await this.$axios.$get('http://icanhazip.com')
      this.ip = ip
    }
  }
}
</script>

<style>

</style>
