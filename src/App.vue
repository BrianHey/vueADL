<template>
<div>
  <input v-model="pikachu" type="text"> 
  <button @click="buscar">Pokémon</button>
  <div>
    <img :src="imagen" alt="">
    <h6>{{nombre}}</h6>
    <p>{{movimientos}}</p>
  </div>
</div>
</template>

<script>
export default {
  name: "app",
};
</script>
