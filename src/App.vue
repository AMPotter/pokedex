<template>
  <div id="app">
    <Header :sort="sort" :filter="filter" :types="types"/>
    <main>
      <Results :list="list"/>
    </main>
  </div>
</template>

<script>
import Header from './components/Header';
import Results from './components/Results';
import pokemon from './pokemon';

export default {
  components: {
    Header,
    Results
  },

  data() {
    return {
      pokemon,
      sort: {
        prop: 'pokemon'
      },
      filter: {
        type: 'all',
        attack: 0,
        defense: 0
      }
    };
  },

  computed: {
    list() {
      return this.filtered.slice().sort((a, b) => {
        const propA = a[this.sort.prop];
        const propB = b[this.sort.prop];
        if(propA === propB) return 0;
        if(propA > propB) return 1;
        return -1;
      });
    },
    filtered() {
      const { type, attack, defense } = this.filter;
      return this.pokemon.slice().filter(p => {
        return (type === 'all' || p.type_1 === type || p.type_2 === type)
          && (attack < 1 || p.attack > attack)
          && (defense < 1 || p.defense > defense);
      });
    },
    types() {
      const type1 = this.pokemon.map(p => p.type_1);
      const type2 = this.pokemon.map(p => p.type_2);
      const set = new Set(type1.concat(type2));
      return [...set.values()];
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>