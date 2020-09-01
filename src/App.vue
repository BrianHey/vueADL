<template>
<div>
  <Character v-for="(personaje, i) in personajes" :key="i" :src="personaje.picture" :mssg="personaje.nombre"/>
</div>

</template>

<script>
import Character from "./components/Character";
export default {
  components: {
    Character,
  },
  data() {
    return {
      personajes: [],
    }
  },
  mounted(){
    fetch("https://rickandmortyapi.com/api/character")
    .then((response)=> response.json())
    .then((json)=>{
      let data = json.results;

      data.slice(0,5).forEach(el => {
        let nombre = el.name;
        let picture = el.image;

      
      this.personajes.push({nombre, picture});
        
      });
    })
    .catch((err)=>{console.log(`todo esta perdido rick ${err}`)})
  }
};
</script>

<style>
</style>