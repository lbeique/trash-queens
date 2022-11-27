<script setup>
import BackgroundGameVue from '../components/gameplay/BackgroundGame.vue';
import ScoreVue from '../components/gameplay/Score.vue';
import TimerVue from '../components/gameplay/Timer.vue';
import GameRecycleBinsVue from '../components/gameplay/GameRecycleBins.vue';
import GameGarbageVue from '../components/gameplay/GameGarbage.vue';
import HintVue from '../components/gameplay/Hint.vue';
</script>

<template>
    <div class="gameContainer">
        <ScoreVue :currentScore="0" class="topScore" />
        <BackgroundGameVue :numWrong="3" />
        <TimerVue class="timer" />
        <div class="recycleBins__grid">
            <GameRecycleBinsVue v-for="bin in recycleBins" :binType="bin" :key="bin" :currentGarbage="currentGarbage"
                @next-garbage="nextGarbage" />
        </div>
        <GameGarbageVue :setCurrentGarbage="setCurrentGarbage" ref="gameGarbage" class="garbage" />
        <HintVue :garbage-name="currentGarbage.garbageName" :garbage-category="currentGarbage.garbageCategory"
            class="hint" />
    </div>

</template>

<script>
export default {
    name: "Gameplay",
    methods: {
        setCurrentGarbage(garbage) {
            this.currentGarbage = garbage
        },
        nextGarbage() {
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
}

</script>

<style scoped>
.topScore {
    position: fixed;
    z-index: 1;
}

.timer {
    position: absolute;
    top: 15%;
    left: 35vw;
}

.gameContainer {
    background-color: #82CE9B;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    /* overflow-y: hidden; */
}

.recycleBins__grid {
    display: grid;
    grid-template: repeat(2, 1fr)/repeat(3, 1fr);
    grid-gap: 1.25rem;
    place-items: center;
    margin: 5% 0;
}

.garbage {
    margin: 10%
}

.hint {
    position: absolute;
    z-index: 1;
    bottom: 15%;
    left: 10%;
}
</style>

