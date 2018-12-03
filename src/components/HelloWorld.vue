<template>
  <div id="hello-life">
    <h1>Welcome To My New Slap Game</h1>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQrxHEkB15etL8g9BgeR98I2tH4Auw8lMtfZ0XaxwgOM44U87s0jA">
    <div class="button">
      <button @click='attack(1)'>SLAP</button>
      <button @click='attack(5)'>Punch</button>
      <button @click='attack(10)'>Kick/button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
      }
    },
    computed: {
      target() {
        return this.$store.state.targets[0]
      },
    },
    methods: {
      attack(val) {
        this.$store.dispatch('attack', val)
      },
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #hello-life {
    background-color: lightblue;
  }

  button {
    size: 40px;
  }

  img {
    height: 300px;
    position: relative
  }

  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>