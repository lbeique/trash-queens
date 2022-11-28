<script setup>
import BackgroundGameVue from '../components/gameplay/BackgroundGame.vue';
import ScoreVue from '../components/gameplay/Score.vue';
import TimerVue from '../components/gameplay/Timer.vue';
import GameRecycleBinsVue from '../components/gameplay/GameRecycleBins.vue';
import GameGarbageVue from '../components/gameplay/GameGarbage.vue';
import HintVue from '../components/gameplay/Hint.vue';
import GameTrashMountain from "../components/gameplay/GameTrashMountain.vue"
</script>

<template>
    <div class="gameContainer">
        <ScoreVue :currentScore="score" class="topScore" />
        <BackgroundGameVue ref="backgroundGame" />
        <GameTrashMountain class="trashMountain" ref="gameTrashMountain" :setWrongNums="setWrongNums"
            :finalScore="score" />
        <TimerVue class="timer" :finalScore="score" />
        <div class="grassArea">
            <div class="recycleBins__grid">
                <GameRecycleBinsVue v-for="bin in recycleBins" :binType="bin" :key="bin"
                    :currentGarbage="currentGarbage" @next-garbage="nextGarbage" @wrong-drop="wrongDrop" />
            </div>
            <GameGarbageVue :setCurrentGarbage="setCurrentGarbage" ref="gameGarbage" class="garbage" />
            <HintVue :garbage-name="currentGarbage.garbageName" :garbage-category="currentGarbage.garbageCategory"
                class="hint" />
        </div>
    </div>

</template>

<script>
export default {
    name: "gameplay-Easy",
    methods: {
        setCurrentGarbage(garbage) {
            this.currentGarbage = garbage
        },
        nextGarbage() {
            this.$refs.gameGarbage.getRandomGarbage()
            this.rounds++
            // console.log("add round", this.rounds)
        },
        wrongDrop() {
            this.$refs.gameTrashMountain.moveMountainY()
            console.log("ahhh", this.numWrong)
            this.$refs.backgroundGame.changeBack(this.numWrong)
        },
        setWrongNums(counter) {
            this.numWrong = counter
            // console.log("this is in the gameplay", this.numWrong)
        }
    },
    computed: {
        score() {
            return this.rounds - this.numWrong
        }
    },
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
            ],
            numWrong: 0,
            rounds: 0
        };
    }
}

</script>

<style scoped>
.topScore {
    position: fixed;
    z-index: 1;
}

.trashMountain {
    position: absolute;
    top: 40%;
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
    /* z-index: -5; */
    /* overflow-y: hidden; */
}

.grassArea {
    background-color: #82CE9B;
    width: 100%;
    height: 100%;

    /* z-index: 1; */

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
    z-index: 3;
    bottom: 25%;
    left: 10%;
}
</style>

