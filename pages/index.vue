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
  components: {},
  data() {
    return {
      lorem: {
        head: 'Lorem ipsum',
        body: 'Etiam ullamcorper. Suspendisse a pellentesque dui, non felis maecenas.'
      }
    }
  }
}
</script>

<style scoped>
.cards {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.card {
  width: 30%;
  margin: 1%;
  box-shadow: 0px 1px 4px #0003;
}

.card .img {
  background-image: url('http://via.placeholder.com/150x150');
  width: 100%;
  height: 200px;
}

.card h1 {
  margin-bottom: .5em;
}

.desc {
  background: white;
  padding: 2em 1em;
}
</style>
