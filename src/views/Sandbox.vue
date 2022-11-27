<script setup>
import GameButton from '../components/GameButton.vue'
import Hint from '../components/Hint.vue'
import GoBack from '../components/GoBack.vue'
// import ExitGamePrompt from '../components/ExitGamePrompt.vue'

</script>

<template>
  <main>
    <GoBack :isGame= true />
    <GameButton text="Start Game" @click="startGame" />
    <Hint garbage-name="apple"  garbage-category="organics" />
<!--    <ExitGamePrompt/>-->

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
    flex-direction: column;
    justify-content: center;
    gap: 6rem;

    padding:5px
  }
</style>
