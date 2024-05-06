<script>
import axios from "axios";
import AppCard from "./AppCard.vue";
export default {
  data() {
    return {
      characterArray: [],
    };
  },
  created() {
    axios.get("https://rickandmortyapi.com/api/character").then((resp) => {
      this.characterArray = resp.data.results;
      console.log(this.characterArray);
    });
  },
  components: {
    AppCard,
  },
};
</script>

<template>
  <div class="container">
    <h1>Ricky and Morty App</h1>
    <div class="row row-cols-lg-4 row-cols-md-3 row-cols-2 gap-4 justify-content-center">
      <div class="col" v-for="curChar in characterArray">
        <AppCard
          :cardImg="curChar.image"
          :cardName="curChar.name"
          :cardStatus="curChar.status"
          :cardSpecies="curChar.species"
        />
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

h1 {
  margin: 30px 0px;
}
</style>
