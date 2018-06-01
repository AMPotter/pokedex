<template>
  <span>
    Type:
    <select v-model="filter.type">
      <option value="all">All Types</option>
      <option v-for="type in types" :key="type">
        {{type}}
      </option>
    </select>

    Attack:
    <input v-model="filter.attack" type="number">

    Defense:
    <input v-model="filter.defense" type="number">
  </span>
</template>

<script>
export default {
  props: ['filter', 'types']
};
</script>