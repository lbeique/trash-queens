<script setup>
import FinalScoreVue from '../components/gameplay/FinalScore.vue';
import Button from '../components/shared/Button.vue'
</script>

<template>
        <div class="container">
            <FinalScoreVue :finalScore="this.$route.params.id" />
            <Button text="Share" variant="game" class="btn"></Button>
            <Button text="Play Again" variant="alternate" @click="playAgain" class="btn"></Button>
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
            this.$router.push("/gameplay-easy");
        }
    },
};
</script>

<style scoped>
.container {
    height: 85vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.btn{
  margin:10px 0;
}
</style>