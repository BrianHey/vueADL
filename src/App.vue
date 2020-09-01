<template>
<div>
  <Character :src="src" :mssg="mssg"/>
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
      src: "https://static.vix.com/es/sites/default/files/styles/1x1/public/imj/p/paisajes-espectaculares-del-mundo-1.jpg",
      mssg: "El hermoso sur de Chile"
    }
  },
};
</script>

<style>
</style>