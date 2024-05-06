<script>
export default {
  props: {
    cardImg: String,
    cardName: String,
    cardStatus: String,
    cardSpecies: String,
  },
};
</script>

<template>
  <div
    class="myCard d-flex flex-column gap-2 align-center justify-content-center p-2"
  >
    <img :src="cardImg" alt="" class="rounded-circle"/>
    <h4 class="fw-bold fs-3">{{ cardName }}</h4>
    <span class="fs-4">{{ cardStatus }}</span>
    <span>{{ cardSpecies }}</span>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.myCard{
    background-color: lightblue;
    border-radius: 20px;
    color: white;

}

img{
    border: 4px solid white;
}
</style>
