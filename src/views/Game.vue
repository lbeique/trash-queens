<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <RouterLink to="/GamePlay-Easy">
    <Button text="Easy Mode" variant="primary" @click="startGame" />
  </RouterLink>
  <RouterLink to="/GamePlay-Hard">
    <Button text="Hard Mode" variant="primary" @click="startGame" />
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
