<template>
<section class="container">
  <div class="wrap">
    <form class="" action="" method="post" @submit.prevent>
      <input type="text" name="" value="" placeholder="Name" required>
      <input type="email" name="" value="" placeholder="Email" required>
      <textarea class="message" name="name" rows="5" placeholder="Message"></textarea>
      <input class="button" type="submit" name="" value="Send">
    </form>
  </div>
</section>
</template>

<script>
export default {
  components: {},
}
</script>

<style scoped>
  .wrap{
    background: white;
    border-radius: .2em;
    width: 50vmin;
    height: 50vmin;
    display: flex;
    justify-content: center;
    box-shadow: 0px 1px 4px #0003;
    align-items: center;
  }
  form{
    display: flex;
    width: 60%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .button {
    background: #2196f3;
    width: auto;
    color: white;
    text-transform: uppercase;
    border: none;
    border-radius: .2em;
    padding: .5em 2em;
    box-shadow: 0px 1px 4px #0003;
    cursor: pointer;
    margin: 0;
    align-self: flex-end;
  }
  input, textarea{
    font-family: Roboto;
    border: none;
    border-bottom: solid .1em #0005;
    padding: .3em 0;
    margin: 1em;
    width: 100%;
    font-size: inherit;
  }
  textarea{
    resize: none;
  }
  input.message{
    height: 5em;
  }
</style>
