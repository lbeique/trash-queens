<script setup>
import GameButton from '../components/GameButton.vue'

</script>

<template>
 
    <GameButton text="Sandbox" @click="startGame" />
 
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
  main {
    display: flex;
    justify-content: center;
  }
</style>