<script setup>
import Button from '../shared/Button.vue'
import Tracker from './Tracker.vue';
</script>

<template>
    <div class="card">
        <h1 class="card__content__title">Tutorial</h1>
        <img class="card__content__image" :src="imageSource" alt="image">
        <p class="card__content__text">{{ text }}</p>
        <div class="card__buttons">
            <Button :text="backText" variant="tutorial" @click="backClick" />
            <Button :text="forwardText" variant="tutorial" @click="forwardClick" />
        </div>
        <div class="card__tracker">
            <Tracker :trackerPosition="currentStep" />
        </div>
    </div>
</template> 

<script>
export default {
    name: "Tutorial",
    methods: {},
    computed: {},
    props: {
        text: {
            type: String,
            required: true
        },
        imageSource: {
            type: String,
            required: true
        },
        backText: {
            type: String,
            required: true
        },
        forwardText: {
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
    },
    data() {
        return {};
    },
    components: {
        Button,
        Tracker
    }
};
</script>

<style scoped>
.card {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #273D4E;
    padding: 1rem;
    border-radius: 20px;
}

.card__content {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.card__content__title {
    color: #F5F9E9;
    font-size: 1.5rem;
    font-family: "FuzzyBubbles-Bold", sans-serif;
}

.card__content__image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.card__content__text {
    color: #F5F9E9;
    font-size: 1rem;
    font-family: "Nunito-Regular", sans-serif;
}

.card__tracker {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 20px;
}

.card__tracker__dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: #000;
    margin: 0 5px;
}
</style>