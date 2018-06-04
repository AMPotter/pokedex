<template>
  <span>
    Sort By:
    <select v-model="sort.prop">
      <option value="pokemon">name</option>
      <option value="type_1">type</option>
      <option value="attack">attack</option>
      <option value="defense">defence</option>
    </select>
  </span>
</template>

<script>
export default {
  props: ['sort']
};
</script>