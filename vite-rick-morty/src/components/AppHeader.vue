<script>
export default {
  data() {
    return {
      title: "Ricky and Morty App",
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <h1>{{ title }}</h1>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

header {
  position: fixed;
  z-index: 99;
  left: 0px;
  top: 0px;
  width: 100%;
  background-color: $header-color;
  height: $header-height;

  .container {
    @include flex(row, center, center);
    height: 100%;
  }
}
</style>
