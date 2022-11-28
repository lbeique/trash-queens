<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
import GameButtonMode from '../components/gameIntro/GameButtonMode.vue';
</script>

<template>
  <Header title="Start Game">
    <template v-slot:Button>
      <Button text="Tutorial" variant="tutorial-alternate" @click="startTutorial" />
    </template>
  </Header>

  <RouterLink style="text-decoration: none;" to="/GamePlay-Easy">
    <GameButtonMode :gameMode="'easy'" @click="startGame"/>
  </RouterLink>
  <RouterLink style="text-decoration: none;" to="/GamePlay-Hard">
    <GameButtonMode :gameMode="'hard'" @click="startGame"/>
  </RouterLink>
  


</template>

<script>
export default {
    name: "GameIntro",
    methods: {
        startTutorial() {
            this.$router.push("/tutorial");
        }
    },
    computed: {},
    props: {},
    data() {
        return {};
    },
    components: { 
      Header, 
      Button 
    }
};
</script>

<style scoped>

</style>
