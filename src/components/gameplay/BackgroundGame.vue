
<template>
    <div>
        <!-- <svg class="backgroundContainer">
        </svg> -->
        <!-- <img src="`../assets/backgrounds/{{backgrounds[0]}}`" alt="cartoon trees"> -->
        <img :src="backgroundUrl" alt="cartoon trees">

    </div>
</template>

<script>
export default {
    props: [
        "numWrong"
    ],
    data() {
        return {
            // show: true,
            backgrounds: [
                "Game-Skyscape.svg",
                "Game-Skyscape_orange.svg",
                "Game-Skyscape_dark.svg"
            ],
            backgroundUrl: ""
        }
    },
    methods: {
        changeBack() {
            if (this.numWrong < 6) {
                this.backgroundUrl = new URL(`../../assets/backgrounds/${this.backgrounds[0]}`, import.meta.url).href
            } else if (6 < this.numWrong < 12) {
                this.backgroundUrl = new URL(`../../assets/backgrounds/${this.backgrounds[1]}`, import.meta.url).href
            } else {
                this.backgroundUrl = new URL(`../../assets/backgrounds/${this.backgrounds[3]}`, import.meta.url).href
            }
        }
    },
    beforeMount() {
        this.changeBack()
    }

};
</script>

<style scoped>
img {
    width: 100vw;
}

/* .backgroundContainer {
    background-image: url("../assets/backgrounds/Game-Skyscape.svg");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    width: 100vw;
    height: 50vh;
} */
</style>