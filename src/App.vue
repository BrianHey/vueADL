<template>
  <div id="app">
    <Navbar />
    <desafio_1 />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import desafio_1 from "@/components/Desafio1.vue";

export default {
  name: "Goku",
  components: {
    Navbar,
    desafio_1,
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
