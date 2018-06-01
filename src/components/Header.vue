<template>
  <header>
    <Sort :sort="sort"/>
    <FilterControl :filter="filter" :types="types"/>
  </header>
</template>

<script>
import Sort from './Sort';
import FilterControl from './FilterControl';
export default {
  components: { Sort, FilterControl },
  props: ['sort', 'filter', 'types']
};
</script>