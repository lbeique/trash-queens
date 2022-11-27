<script setup>
import GameButton from '../components/GameButton.vue'
</script>

<template>
  <main>
    <GameButton text="Start Game" @click="startGame" />
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
