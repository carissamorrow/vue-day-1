<template>
  <div id="hello-life">
    <h1>Welcome To My New Slap Game</h1>
    <img src="http://worldartsme.com/images/animated-face-slap-clipart-1.jpg">
    <button @click='attack(1)'>SLAP</button>
    <button @click='attack(5)'>Punch</button>
    <button @click='attack(10)'>Kick</button>
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
  img {
    height: 300px;
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