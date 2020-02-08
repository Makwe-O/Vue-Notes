<template>
  <div class="card-grid">
    <Card
      :qouteDetail="quote"
      v-for="quote in quoteList"
      v-bind:key="quote.id"
    />
  </div>
</template>
<script>
import Card from './Card';
export default {
  name: 'CardGrid',
  components: {
    Card
  },
  props: {
    quoteList: Array
  }
};
</script>

<style scoped>
.card-grid {
  display: flex;
  max-width: 960px;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
