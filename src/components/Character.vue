<template>
  <div>
      <img :src="src" alt="">
      <h3>{{mssg}}</h3>
    
  </div>
</template>

<script>

export default {
    name: 'Character',
    props:{
      src: String,
      mssg: String
    }
}
</script>

<style>

</style>