<script>
import axios from 'axios'
export default{
  data(){
    return{
      characterArray: [],
    }
  },
  created(){
    axios.get('https://rickandmortyapi.com/api/character').then((resp)=>{
      this.characterArray = resp;
      console.log(this.characterArray.data.results[0].name);
      console.log(this.characterArray.data.results[0].status);
      console.log(this.characterArray.data.results[0].species);


    });
  }
}
</script>

<template>
    <h1>ciao</h1>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;


</style>
