<template>
  <div class="card">
    <p>Note: {{ qouteDetail.text }}</p>
    <div class="card__bottom">
      <p>Date Added: {{ qouteDetail.date }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    qouteDetail: Object
  }
};
</script>

<style scoped>
.card {
  border-radius: 2px;
  padding: 24px;
  border: 1px solid #e3e3e3;
  margin: 10px;

  transition: all 0.5s;
  max-width: 240px;
}
.card__bottom {
  border-top: 1px solid #e3e3e3;
}
p {
  text-align: left;
}
.card:hover {
  box-shadow: 1px 1px 5px #e6e6e6;
}
</style>
