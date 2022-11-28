<script setup>
import FinalScoreVue from '../components/gameplay/FinalScore.vue';
import Button from '../components/shared/Button.vue'
</script>

<template>
    <div>
        <div class="container">
            <FinalScoreVue :finalScore="1" />
            <br />
            <Button text="Share" variant="game"></Button>
            <br />
            <Button text="Play Again" variant="alternate"></Button>
        </div>
    </div>

</template>

<script>
</script>

<style scoped>
.container {
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
</style>