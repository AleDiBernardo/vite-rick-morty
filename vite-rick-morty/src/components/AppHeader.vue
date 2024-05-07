<script>
import AppSearch from "./AppSearch.vue";

export default {
  components: {
    AppSearch,
  },
};
</script>

<template>
  <header class="d-flex flex-column justify-content-center align-items-center">
    <div>
      <h1>Ricky and Morty App</h1>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

header {
  padding: 20px;
  // position: fixed;
  // width: 100%;
  // left: 0;
  // top: 0;
  // transform: translate(-50%);

  div {
    background-color: lightcoral;
    border-radius: 20px;
    padding: 10px;
    color: white;

    h1 {
      font-weight: bold;
      margin: 0;
    }
  }
}
</style>
