<template>
    <header>
        <span>
            <h3>Filter by type</h3>
            <select v-model="filter.type" v-on:change="$emit('select', filter.type)">
                <option disabled value="">Select a type</option>
                <option>normal</option>
                <option>fire</option>
                <option>fighting</option>
                <option>water</option>
                <option>flying</option>
                <option>grass</option>
                <option>poison</option>
                <option>electric</option>
                <option>ground</option>
                <option>psychic</option>
                <option>rock</option>
                <option>ice</option>
                <option>bug</option>
                <option>dragon</option>
                <option>ghost</option>
                <option>dark</option>
                <option>steel</option>
                <option>fairy</option>
            </select>
        </span>
    </header>
</template>

<script>
export default {
  props: ['filter']
};
</script>