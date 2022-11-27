
<template>
    <div>
        <!-- <svg class="backgroundContainer">
        </svg> -->
        <!-- <img src="`../assets/backgrounds/{{backgrounds[0]}}`" alt="cartoon trees"> -->
        <img src="../assets/backgrounds/Game-Skyscape.svg" alt="cartoon trees">

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
            ]
        }   
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