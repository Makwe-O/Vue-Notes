<template>
  <form @submit.prevent="createNote(newNote)">
    <h2>Enter Your Note in the form below</h2>
    <textarea name="quote" cols="50" rows="10" v-model="newNote"></textarea>
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      newNote: ""
    };
  },
  props: {
    createNote: Function
  }
};
</script>

<style  scoped>
form {
  max-width: 600px;
  margin: 0 auto;
}
textarea {
  width: 100%;
}
button {
  padding: 10px 20px;
  border: 0px;
  margin-top: 20px;
  border-radius: 5px;
  background: #f3d55b;
  color: #fff;
  transition: all 0.5s;
}
button:hover {
  background: #cab14b;
}
</style>