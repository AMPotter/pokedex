<template>
  <div id="app">
    <Header />
    <Results :pokemonTiles="pokemonList"/>
  </div>
</template>

<script>
import pokemon from './data/pokemon.js';
import Header from './components/Header.vue';
import Results from './components/Results.vue';

export default {
  data() {
    return {
      pokemonList: pokemon,
      selected: null
    };
  },
  components: {
    Header,
    Results
  },
  methods: {
    updateSelected(pokemon) {
      this.selected = pokemon;
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
