<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
</script>

<template>
  <Header title="Start Game">
    <template v-slot:Button>
      <Button text="Tutorial" variant="tutorial-alternate" @click="startTutorial" />
    </template>
  </Header>
  <RouterLink to="/gamePlay-Easy">
    <Button text="Easy Mode" variant="primary" />
  </RouterLink>
  <!-- <RouterLink to="/GamePlay-Hard">
    <Button text="Hard Mode" variant="primary" @click="startGame" />
  </RouterLink> -->

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
