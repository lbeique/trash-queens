<script setup>
import Button from '../shared/Button.vue'
import Tracker from './Tracker.vue';
</script>

<template>
    <div class="card">
        <h1 class="card__title">Tutorial</h1>
        <div class="card__content">
            <img class="card__image" :src="imageSource" alt="image">
            <p class="card__text">{{ text }}</p>
        </div>
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
    height: 100%;
    min-height: 622px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    background-color: #273D4E;
    padding: 4rem 1rem 1rem 1rem;
    border-radius: 20px;
}

.card__title {
    color: #F5F9E9;
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