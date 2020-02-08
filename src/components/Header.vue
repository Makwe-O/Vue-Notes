<template>
  <nav>
    <figure>
      <img src="../assets/logo.svg" alt="logo" width="50px" />
    </figure>
    <a>Link to Github</a>
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