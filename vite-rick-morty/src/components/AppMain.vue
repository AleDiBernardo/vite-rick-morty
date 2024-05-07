<script>
import {store} from "../store";
import AppCard from "./AppCard.vue";
export default {
  data() {
    return {
      store
    };
  },

  components: {
    AppCard,
  },
};
</script>

<template>
  <div class="container">
    <div class="row row-cols-lg-4 row-cols-md-3 row-cols-2 gap-4 justify-content-center">
      <div class="col" v-for="curChar in store.charList">
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

.container{
  padding-top: $pt-40;
  padding-bottom: $pb-60;
}

</style>
