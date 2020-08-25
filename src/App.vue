<template>
<div id="app">
  <!--  <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />-->
  <Navbar />
  <input v-model="tarea" />
  <button @click="agregarTarea">Agregar</button>
  <ul>
    <li v-for="(tarea, index) in tareas" :key="index">{{tarea}}</li>
  </ul>
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
    agregarTarea() {
      this.tareas.push(this.tarea);
      this.tarea = "";
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
