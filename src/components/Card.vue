<template>
  <div class="card__container">
    <div class="card__main">
      <p v-if="qouteDetail.text.length >= 25">{{ qouteDetail.text.slice(0,25) + '...' }}</p>
      <p v-else>{{ qouteDetail.text }}</p>
      <div class="card__bottom">
        <p>Date Added: {{ qouteDetail.date }}</p>
      </div>
    </div>
    <div class="card__options">
      <button @click="viewNote(qouteDetail)" class="card__options__icon">
        <figure>
          <img src="../assets/eye.svg" width="20px" />
        </figure>
      </button>
      <button @click="deleteNote(qouteDetail)" class="card__options__icon">
        <figure>
          <img src="../assets/bin.svg" width="20px" />
        </figure>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    qouteDetail: Object,
    viewNote: Function,
    deleteNote: Function
  }
};
</script>

<style scoped>
.card__container {
  border-radius: 2px;
  border: 1px solid #e3e3e3;
  margin: 10px;
  transition: all 0.5s;
  max-width: 240px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.card__main {
  padding: 24px;
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
.card__options {
  display: flex;
  background: #e3e3e3;
  justify-content: space-between;
}
.card__options__icon {
  cursor: pointer;
  border: none;
  background: #e3e3e3;
  transition: all 0.5s;
}
.card__options__icon:hover {
  background: #cccccc;
}
</style>
