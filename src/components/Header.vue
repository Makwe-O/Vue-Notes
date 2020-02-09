<template>
  <nav>
    <figure>
      <img src="../assets/logo.svg" alt="logo" width="50px" />
    </figure>
    <a href="https://github.com/Makwe-O/Vue-Notes" target="_blank">Link to Github</a>
  </nav>
</template>

<script>
export default {
  name: "Header"
};
</script>
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>