<script setup>
import Button from '../components/shared/Button.vue';
import GoBack from '../components/shared/GoBack.vue';
import Tutorial from '../components/tutorial/Tutorial.vue';
</script>

<template>
    <div class="page">
        <GoBack />
        <Tutorial v-if="position == 1" :currentStep="position" text="Do your best!" :imageSource="imgUrl"
            backText="Return" forwardText="Next" :backClick="handleReturn" :forwardClick="handlePageTwo" />
        <Tutorial v-if="position == 2" :currentStep="position" text="Do your best!" :imageSource="imgUrl"
            backText="Previous" forwardText="Next" :backClick="handlePageOne" :forwardClick="handlePageThree" />
        <Tutorial v-if="position == 3" :currentStep="position" text="Do your best!" :imageSource="imgUrl"
            backText="Previous" forwardText="Start Game" :backClick="handlePageTwo" :forwardClick="handleGameStart" />
    </div>
</template>

<script>
export default {
    name: "Tutorial",
    methods: {
        handleReturn() {
            this.$router.push("/game");
        },
        handlePageOne() {
            this.position = 1;
        },
        handlePageTwo() {
            this.position = 2;
        },
        handlePageThree() {
            this.position = 3;
        },
        handleGameStart() {
            this.$router.push("/gameplay-easy");
        }
    },
    computed: {},
    props: {},
    data() {
        return {
            position: 1,
            imgUrl: new URL("https://images.unsplash.com/photo-1525695230005-efd074980869?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80").href
        }
    },
    components: {
        GoBack,
        Button,
        Tutorial
    }
};
</script>

<style scoped>
.page {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    gap: 2rem;
    width: 100%;
}
</style>