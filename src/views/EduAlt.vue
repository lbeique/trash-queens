<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
</script>

<template>
  <Header title="Reduse, Reuse, and Recycle" />

</template>

<script>
export default {
    name: "EduAlt",
    methods: {

    },
    computed: {},
    props: {},
    data() {
        return {};
    },
    components: { 
      Header, 
      Button 
    }
};
</script>

<style scoped>

</style>