<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Strat title="Pro Strat" text="Yo this strat is so pro" />
  </div>
</template>

<script>
import Strat from './components/Strat.vue'

export default {
  name: 'App',
  components: {
    Strat
  },
  data() {
    return {
      strat: {
        title: String,
        text: String
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
