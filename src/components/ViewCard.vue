<template>
  <div>
    <h2>Selected Note</h2>
    <p>{{selectedNote.text}}</p>
  </div>
</template>

<script>
export default {
  name: "ViewCard",
  props: {
    selectedNote: Object
  }
};
</script>

<style scoped>
p {
  text-align: left;
  font-size: 20px;
}
div {
  margin-top: 30px;
  margin-bottom: 120px;
}
</style>