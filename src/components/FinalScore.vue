
<template>
    <div>
        <div class="finalScoreContainer">
            <img src="../assets/trees.png" alt="cartoon trees">
            <span>Your Score: {{finalPercentage}}%</span>
            <span>{{finalScore}}/25</span>
        </div>
    </div>
</template>

<script>
export default {
    props: [
        "finalScore"
    ],
    computed: {
        finalPercentage() {
            return this.finalScore/25 * 100
        }
    }
};
</script>

<style scoped>
.finalScoreContainer {
    width: 60vw;
    display: flex;
    flex-direction: column;
    align-items: center;
}

span {
    font-size: 2rem;
    font-weight: 800;
}
</style>