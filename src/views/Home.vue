<script setup>
import Card from '../components/home/Card.vue';
import Button from '../components/shared/Button.vue'
import Scroll from '../components/shared/Scroll.vue';

</script>

<template>
  <div class="center">
    <Button text="Sandbox" variant="tutorial-alternate" @click="startGame"/>
    <Card :text="gameText" :title="gameTitle" :image="gameImage" :buttonText="gameButtonText" :buttonFunction="game" />
    <Scroll />
  </div>
</template>

<script>
export default {
    name: "Sandbox",
    methods: {
        game() {
            this.$router.push("/sandbox");
        },
        about() {
            this.$router.push("/about");
        },
        resources() {
            this.$router.push("/resources");
        },
    },
    computed: {},
    props: {},
    data() {
        return {
          gameText: "Help the Trashy Queens sort through the wastes of the endless Trash Mountain!",
          gameTitle: "Explore the Game",
          gameImage: new URL(`../assets/recycling-bin/paper-bin.svg`, import.meta.url).href,
          gameButtonText: "The Game"
        };
    },
    components: {
    Button,
    Scroll,
    Card
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