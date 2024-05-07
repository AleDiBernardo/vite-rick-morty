<script>
import {store} from "./store";
import axios from "axios"
import AppMain from './components/AppMain.vue';
import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';

export default{
  components: {
    AppMain,
    AppHeader,
    AppSearch
  },
  data(){
    return{
      store
    }
  },
  created(){
    this.getChars();
  },
  methods: {
    getChars(){
      const params = {
        num: 20,
        offset: 0,
      }

      if (this.store.selectedStatus !== "All") {
        params.status = this.store.selectedStatus;
      }

      axios
        .get("https://rickandmortyapi.com/api/character", {
          params
        })
        .then((resp) => {
          this.store.charList = resp.data.results;
          console.log(this.store.charList);
        });
      
    }
  }
}
</script>

<template>
  <AppHeader/>
  <AppSearch @filter="getChars" />
  <AppMain/>
</template>

<style lang="scss">


</style>