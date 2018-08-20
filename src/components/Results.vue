<template>
  <ul class="results">
    <Tile
      v-for="pokemon in list"
      :key="pokemon.pokemon"
      :pokemon="pokemon"
    />
  </ul>
</template>

<script>
import Tile from './Tile';

export default {
  props: ['list'],
  components: { Tile }
};
</script>

<style>
.results {
  list-style: none;
}