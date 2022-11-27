<script setup>
import GameButton from '../components/shared/GameButton.vue'

</script>

<template>
  <div class="center">
    <GameButton text="Sandbox" @click="startGame" />
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
  justify-content: center;
  align-items: center;
}
</style>