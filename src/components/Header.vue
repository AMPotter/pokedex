<template>
    <main>
        <h1>Pokedex</h1>
        <section class="controls">
            <SearchFilter :filter="filter" />
        </section>
    </main>
</template>

<script>
import SearchFilter from './SearchFilter.vue';
import Sort from './Sort.vue';

export default {
  components: {
    SearchFilter,
    Sort
  },
  props: ['filter']
};
</script>
