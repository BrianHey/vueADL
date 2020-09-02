<template>
<div>
  <h1>papa</h1>
  <input type="text" v-model="name">
</div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      name: ''
    }
  },
  beforeCreate() {
    console.log("Hola soy 1");
  },
  created() {
    console.log("Hola soy 2");
  },
  beforeMount() {
    console.log("Hola soy 3");
  },
  mounted() {
    console.log("Hola soy 4");
  },
  beforeUpdate() {
      console.log("Hola soy beforeUpdate");
      console.log(this.name)
  },
  updated() {
    console.log("Hola soy updated");
      console.log(this.name)
    
  },
};
</script>
