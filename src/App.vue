<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Strat :title="strat.title" :text="strat.text"/>
    <div class="field is-grouped is-grouped-centered">
      <p class="control">
        <b-button class="is-primary is-medium" @click="attackStrat">Choose Attack Strat</b-button>
      </p>
      <p class="control">
        <b-button class="is-primary is-medium" @click="defenseStrat">Choose Defense Strat</b-button>
      </p>
    </div>
  </div>
</template>

<script>
import Strat from './components/Strat.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Strat
  },
  data() {
    return {
      strat: {
        title: "Rainbow Six Siege Stratroulette",
        text: "Click one of the buttons below to pick  random strat."
      }
    }
  },
  methods: {
    attackStrat() {
      axios.get('api/attack_strats/random')
      .then((res) => {
        this.strat.title = res.data.title,
        this.strat.text = res.data.text
      })
      .catch(function (err) {
        console.log(err.message)
      })
    },
    defenseStrat() {
      axios.get('api/defense_strats/random')
      .then((res) => {
        this.strat.title = res.data.title,
        this.strat.text = res.data.text
      })
      .catch(function (err) {
        console.log(err.message)
      })
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
