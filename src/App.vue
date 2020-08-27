<template>
  <div id="app">
    <h1>{{contadorMin < 10 ? '0'+contadorMin : contadorMin }}:{{contadorSeg < 10 ? '0'+contadorSeg : contadorSeg }} min/seg</h1>
    <div class="botones">
      <button @click="iniciar(3)">3 segs</button>
      <button @click="iniciar">1 min</button>
      <button @click="iniciar">2 min</button>
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue";

export default {
  name: "Goku",
  components: {
    Navbar,
  },
  data() {
    return {
      contadorMin: 0,
      contadorSeg: 0

    }
      
  },
  // function myFunction() {
  // setInterval(function(){ alert("Hello"); }, 3000);
  methods: {
    iniciar(time) {
      this.contadorSeg = time
      setInterval(()=>{this.contadorSeg > 0 ? this.contadorSeg-- : false},1000)
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  ul {
    li {
      color: blue;
    }
  }
}
</style>
