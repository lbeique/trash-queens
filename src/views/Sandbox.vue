<script setup>
import GameButton from '../components/GameButton.vue'
import GameRecycleBins from '../components/GameRecycleBins.vue';
import Hint from '../components/Hint.vue'
import GameGarbage from '../components/GameGarbage.vue';
import GoBack from '../components/GoBack.vue'
// import ExitGamePrompt from '../components/ExitGamePrompt.vue'
import ScoreVue from '../components/Score.vue';
import FinalScoreVue from '../components/FinalScore.vue';
import BackgroundGameVue from '../components/BackgroundGame.vue';
import Timer from '../components/Timer.vue';
</script>

<template>
  <main>
    <GoBack :isGame= true />
    <GameButton text="Start Game" @click="startGame" />
    <div class="recycleBins__grid">
      <GameRecycleBins v-for="bin in recycleBins" :binType="bin" :key="bin" :currentGarbage="currentGarbage" @next-garbage="nextGarbage"/>
    </div>
    <GameGarbage :setCurrentGarbage="setCurrentGarbage" ref="gameGarbage"/>
    <!-- <Hint garbage-name="apple"  garbage-category="organics" /> -->
    <Hint garbage-name="apple"  garbage-category="organics" />
    <ScoreVue :currentScore="0"></ScoreVue>
    <FinalScoreVue :finalScore="0"></FinalScoreVue>
    <Timer></Timer>
    <BackgroundGameVue></BackgroundGameVue>

  </main>
</template>

<script>
export default {
  name: "Sandbox",
  methods: {
    startGame() {
      console.log("Starting game...");
    },
    setCurrentGarbage(garbage){
      this.currentGarbage = garbage
    },
    nextGarbage(){
      this.$refs.gameGarbage.getRandomGarbage()
    }
  },
  computed: {},
  props: {},
  data() {
    return { 
        currentGarbage: {},
        recycleBins: [
          'organics',
          'glass',
          'metal',
          'paper',
          'e-waste',
          'plastic'
        ]
    };
  }
};
</script>

<style scoped>
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 6rem;
    padding:5px;
    background-color: white;
  }

  .recycleBins__grid{
    display: grid;
    grid-template: repeat(2, 1fr)/repeat(3, 1fr);
    grid-gap: 1.25rem;
    place-items: center;
  }

</style>
