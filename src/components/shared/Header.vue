<script setup>
import GoBack from './GoBack.vue';
</script>

<template>
    <div class="header">
        <GoBack :isGame="false" />
        <div class="header__container">
            <div header__title>
                <h1>{{ title }}</h1>
            </div>
            
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
    width: 100%;
    gap: 1rem;
    padding: 2rem 2rem 0 2rem;
}

h1 {
    font-size: 2rem;
    font-family: "FuzzyBubbles-Regular", sans-serif;
}

.header__container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width:100%;
}
</style>