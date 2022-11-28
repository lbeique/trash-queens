<script setup>
import Button from '../components/shared/Button.vue'
</script>

<template>
  <main>
    <Button text="Start Game" variant="primary" @click="startGame" />
  </main>
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
