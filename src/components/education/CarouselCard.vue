<script setup>
import Button from '../shared/Button.vue'
import Tracker from '../tutorial/Tracker.vue';
</script>

<template>
    <div class="card" :class="color">
        <h1 class="card__title">{{ title }}</h1>
        <div class="card__image_row">
            <img class="card__image" :src="trashSource" alt="trash">
        </div>
        <p class="card__content">{{ text }}</p>
        <div class="card__arrows">
            <Arrow direction="left" @click="backClick" />
            <Arrow direction="right" @click="forwardClick" />
        </div>
        <div class="card__bottom">
            <p class="card__text">{{ bin }}</p>
            <img class="card__bin" :src="binSource" alt="bin">
        </div>
        <div class="card__tracker">
            <Tracker :trackerPosition="currentStep" :totalPositions=6 />
        </div>
    </div>
</template> 

<script>
export default {
    name: "CarouselCard",
    methods: {},
    computed: {},
    props: {
        text: {
            type: String,
            required: true
        },
        trashSource: {
            type: String,
            required: true
        },
        binSource: {
            type: String,
            required: true
        },
        content: {
            type: String,
            required: true
        },
        bin: {
            type: String,
            required: true
        },
        backClick: {
            type: Function,
            required: true
        },
        forwardClick: {
            type: Function,
            required: true
        },
        currentStep: {
            type: Number,
            required: true
        },
        color: {
            type: String,
            required: true
        },
    },
    data() {
        return {};
    },
    components: {
        Arrow,
        Tracker
    }
};
</script>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    border-radius: 20px;
    font-family: "Nunito-Regular", sans-serif;
}

.red {
    background-color: #84A7F1;
}

.blue {
    background-color: #F7C932;
}

.yellow {
    background-color: #E05F4E;
}

.card__title {
    font-size: 1.5rem;
    font-family: "FuzzyBubbles-Bold", sans-serif;
}

.card__content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    max-width: 230px;
}

.card__image {
    max-height: 130px;
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 4px;
}

.card__text {
    color: #F5F9E9;
    font-size: 1rem;
    font-family: "Nunito-Regular", sans-serif;
}

.card__buttons {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.card__tracker {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>