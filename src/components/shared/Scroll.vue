<script setup>
import Iconify from './Iconify.vue'
</script>

<template>
    <div class="scroll" @click="scrollToTop">
        <p class="scroll__text">{{ text }}</p>
        <Iconify iconName="icon-park-twotone:up-one" iconColor="#273D4E" iconHeight="32" />
    </div>
</template>

<script>
export default {
    name: "Scroll",
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: "smooth"
            });
        }
    },
    computed: {},
    props: {},
    data() {
        return {
            text: "Scroll to Top"
        };
    }
};
</script>

<style scoped>
.scroll {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5rem;
    padding: 1rem;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
}

.scroll__text {
    font-family: "Nunito-Regular", sans-serif;
    font-size: 1rem;
    color: #273D4E;
}
</style>