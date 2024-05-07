<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
      statusArr: ["All", "Alive", "Unknown", "Dead"],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="d-flex justify-content-between flex-column">
      <div>
        <select @change="$emit('filter')" v-model="store.selectedStatus">
          <option :value="status" v-for="status in statusArr">
            {{ status }}
          </option>
        </select>
        <p>Ci sono {{ store.charList.length }} elementi</p>
      </div>

    </div>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.container {
    select {
        padding: 10px;
        border: 4px solid lightcoral;
        border-radius: 5px;
        background-color: white;
        font-size: 20px;
        font-weight: bold;
    }

    p{
        font-size: 25px;
        font-weight: bold;
    }
}
</style>
