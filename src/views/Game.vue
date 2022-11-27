<script setup>
import GameButton from '../components/shared/GameButton.vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <RouterLink to="/GamePlay-Easy">
    <GameButton text="Easy Mode" @click="startGame" />
  </RouterLink>
  <RouterLink to="/GamePlay-Hard">
    <GameButton text="Hard Mode" @click="startGame" />
  </RouterLink>

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
