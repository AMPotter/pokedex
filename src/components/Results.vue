<template>
    <div>
        <h2>{{pokemonTiles.length}} Pokemon for you to look at.</h2>
        <ul>
            <Tile
                v-for="pokemon in pokemonTiles"
                v-bind:key="pokemon.id"
                :pokemon="pokemon"
                :filter="filter"
            />
        </ul>
    </div>
</template>

<script>
import Tile from './Tile.vue';

export default {
  props: ['pokemonTiles', 'filter'],
  components: {
    Tile
  }
};
</script>
