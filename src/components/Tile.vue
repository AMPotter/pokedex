<template>
  <li class="pokemon">
    <article :style="{ background: pokemon.color_1 }">
      <img :src="pokemon.url_image">
      <div>
        <h3>{{pokemon.pokemon}}</h3>
        <p>A:{{ pokemon.attack}} D:{{ pokemon.defense}}</p>
      </div>
    </article>
  </li>
</template>

<script>
export default {
  props: ['pokemon']
};
</script>

<style>
.pokemon {
  display: inline-block;
  height: 150px;
  width: 150px;
  min-height: 150px;
  min-width: 150px;
  padding: 5px;
  text-align: center;
  cursor: pointer;
}
.pokemon article {
  width: 100%;
  height: 100%;
  padding: 5px;
  overflow: hidden;
}
.pokemon h3 {
  font-size: 12pt;
  margin: 0;
}
.pokemon:hover {
  background: #aaa;
}
.pokemon img {
  width: 60px;
  margin-right: 5px;
}
</style>