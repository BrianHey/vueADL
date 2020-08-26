<template>
  <div id="app">
    <h1>00:00 min/seg</h1>
    <div class="botones">
      <button @click="iniciar">3 segs</button>
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
      tareas: [],
      tarea: "",
    };
  },
  methods: {
    iniciar() {
      alert();
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
