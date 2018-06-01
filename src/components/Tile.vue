<template>
    <div>
        <li v-if="pokemon.type_1 === filter.type || pokemon.type_2 === filter.type || !filter.type">
            <img :src="pokemon.url_image">
            <h3>No. {{pokemon.id}}: {{pokemon.pokemon}}</h3>
            <ul>
                <li>HP: {{pokemon.hp}}</li>
                <li>Type: {{pokemon.type_1}}</li>
                <li v-if="pokemon.type_2 !== 'NA'">Second Type: {{pokemon.type_2}}</li>
                <li>Attack: {{pokemon.attack}}</li>
                <li>Defense: {{pokemon.defense}}</li>
                <li>Special Attack: {{pokemon.special_attack}}</li>
                <li>Special Defense: {{pokemon.special_defense}}</li>
                <li>Speed: {{pokemon.speed}}</li>
            </ul>
        </li>
    </div>
</template>

<script>
export default {
  props: ['pokemon', 'filter']
};
</script>
