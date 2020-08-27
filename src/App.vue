<template>
<div id="app">
  <h1>{{contadorMin < 10 ? '0'+contadorMin : contadorMin }}:{{contadorSeg < 10 ? '0'+contadorSeg : contadorSeg }} min/seg</h1>
  <div class="botones">
    <button @click="iniciar(3)">3 segs</button>
    <button @click="iniciar(60)">1 min</button>
    <button @click="iniciar">2 min</button>
  </div>
</div>
</template>

<script>
export default {
  name: "Goku",

  data() {
    return {
      contadorMin: 0,
      contadorSeg: 0,
      myIntervalo: null,
    };
  },

  methods: {
    iniciar(time) {
      this.contadorSeg = time;
      clearInterval(this.myIntervalo);
      this.myIntervalo = setInterval(() => {
        this.contadorSeg > 0 ? this.contadorSeg-- : false;
        console.log("Soy el intervalo >:-)");
      }, 1000);
      setTimeout(() => {
        clearInterval(this.myIntervalo);
      }, (time + 1) * 1000);
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
