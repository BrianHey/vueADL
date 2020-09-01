<template>
<div>
  <img :src="src" alt />
  <h3 @click="avisaleApapa">{{name}}</h3>
</div>
</template>

<script>
export default {
  name: "Character",
  props: {
    src: String,
    name: String,
  },
  methods: {
    avisaleApapa() {
      this.$emit("toctoc", 2);
    },
  },
};
</script>

<style>
</style>
