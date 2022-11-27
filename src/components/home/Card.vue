<script setup>
    import Button from '../shared/Button.vue'
</script>

<template>
    <div class="card">
        <div class="card__image">
            <img :src="image" alt="Trash Queens are beautiful" />
        </div>
        <div class="card__content">
            <h2 class="card__title">{{ title }}</h2>
            <p class="card__text">{{ text }}</p>
            <Button :text="buttonText" variant="primary" @click="buttonFunction" />
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
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
        buttonText: {
            type: String,
            required: true
        },
        image: {
            type: String,
            required: true
        },
        buttonFunction: {
            type: Function,
            required: true
        }
    },
    data() {
        return {};
    }
};
</script>

<style scoped>
    .card {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 100%;
        background-color: var(--color-white);
        border-radius: 1rem;
        box-shadow: 0 0 1rem rgba(0, 0, 0, 0.2);
        overflow: hidden;
    }

    .card__image {
        width: 100%;
        height: 50%;
        overflow: hidden;
    }

    .card__content {
        width: 100%;
        height: 50%;
        padding: 1rem;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }

    .card__title {
        font-size: 1.5rem;
        font-weight: 700;
        text-align: center;
    }

    .card__text {
        font-size: 1rem;
        font-weight: 400;
        text-align: center;
    }
</style>