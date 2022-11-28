<script setup>
import Button from '../components/shared/Button.vue'
</script>

<template>
 
    <Button text="Start Game" variant="alternate" @click="startGame" />
  
</template>

<script>
export default {
  name: "Sandbox",
  methods: {
    startGame() {
      console.log("Starting game...");
    }
  },
  computed: {},
  props: {},
  data() {
    return {};
  }
};
</script>

<style scoped>
  main {
    display: flex;
    justify-content: center;
  }
</style>