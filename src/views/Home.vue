<script setup>
import Button from '../components/shared/Button.vue'

</script>

<template>
  <div class="center">
    <Button text="Sandbox" variant="primary" @click="startGame" />
    <Button text="Sandbox" variant="alternate" @click="startGame" />
    <Button text="Sandbox" variant="game" @click="startGame" />
    <Button text="Sandbox" variant="tutorial" @click="startGame" />
    <Button text="Sandbox" variant="tutorial-alternate" @click="startGame" />
  </div>
</template>

<script>
export default {
  name: "Sandbox",
  methods: {
    startGame() {
      this.$router.push('/sandbox');
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
.center {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
</style>