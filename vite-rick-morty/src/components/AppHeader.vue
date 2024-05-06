<script>
export default {};
</script>

<template>
  <header class="d-flex justify-content-center align-items-center">
    <h1>Ricky and Morty App</h1>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

header {
  padding: 20px;
  position: fixed;
  width: 100%;
  left: 0;
  top: 0;
  // transform: translate(-50%);

  h1 {
    background-color: lightcoral;
    border-radius: 20px;
    padding: 20px 15px;
    color: white;
    font-weight: bold;
  }
}
</style>
