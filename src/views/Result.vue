<script setup>
import FinalScoreVue from '../components/gameplay/FinalScore.vue';
import Button from '../components/shared/Button.vue'
</script>

<template>
    <div>
        <div class="container">
            <FinalScoreVue :finalScore="this.$route.params.id" />
            <br />
            <Button text="Share" variant="game"></Button>
            <br />
            <Button text="Play Again" variant="alternate" @click="playAgain"></Button>
        </div>
    </div>

</template>

<script>
export default {
    name: "result",
    props: [
        "finalScore"
    ],
    methods: {
        playAgain() {
            this.$router.push("/game");
        }
    },
};
</script>

<style scoped>
.container {
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
</style>