<template>
  <div class="desafio-1">
    <p v-if="errorTarea" class="error">Por favor ingresa una tarea</p>
    <input v-model="tarea" />
    <button @click="agregarTarea">Agregar</button>
    <ul>
      <li v-for="(tarea, index) in tareas" :key="index">{{ tarea }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Desafio1",
  data() {
    return {
      tareas: [],
      tarea: "",
      errorTarea: false
    };
  },
  methods: {
    agregarTarea() {
      const task = this.tarea.trim();
      if (task === "") {
        this.errorTarea = true
        return 
      } else {
        this.errorTarea = false;
        this.tareas.push(task);
        this.tarea = "";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.desafio-1 {
  .error {
    color: red;
  }
}
</style>
