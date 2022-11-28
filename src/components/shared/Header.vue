<script setup>
import GoBack from './GoBack.vue';
</script>

<template>
    <div class="header">
        <GoBack :isGame="false" />
        <div header__container>
            <h1>{{ title }}</h1>
            <slot name="Button"></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: "Header",
    props: {
        title: {
            type: String,
            required: true
        }
    },
    components: {
        GoBack
    }
};
</script>

<style scoped>
.header {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

h1 {
    font-size: 2rem;
    font-family: "FuzzyBubbles-Regular", sans-serif;
}

.header__container {
    display: flex;
}
</style>