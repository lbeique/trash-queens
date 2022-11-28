<script setup>
import Button from '../components/shared/Button.vue'
</script>

<template>
    <div class="card">
        <div class="card__content">
            <h1 class="card__content__title">{{ title }}</h1>
            <img class="card__content__image" :src="imageSource" alt="image">
            <p class="card__content__text">{{ text }}</p>
        </div>
        <Button :text="backText" variant="tutorial" @click="backClick" />
        <Button :text="forwardText" variant="tutorial" @click="forwardClick" />
        <div class="card__tracker">
            <div class="card__tracker__dot" :class="isActive"></div>
            <div class="card__tracker__dot" :class="isActive"></div>
            <div class="card__tracker__dot" :class="isActive"></div>
        </div>
    </div>
</template> 

<script>
export default {
    name: "Tutorial",
    methods: {},
    computed: {},
    props: {
        title: {
            type: String,
            required: true
        },
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
        isActive: {
            type: String,
            required: true
        }
    },
    data() {
        return {};
    },
    components: {
        Button
    }
};
</script>

<style scoped>
.card {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    padding: 20px;
    position: relative;
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
    font-size: 1.5rem;
    font-family: "FuzzyBubbles-Bold", sans-serif;
}

.card__content__image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.card__content__text {
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