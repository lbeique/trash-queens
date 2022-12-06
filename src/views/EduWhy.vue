<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
import UserEngagement from '../components/education/UserEngagement.vue';
import Scroll from '../components/shared/Scroll.vue';
</script>

<template>
  <Header title="Why Recycle?" />
  <UserEngagement>
    <Scroll scrollColor="#F5F9E9" fontColor="#F5F9E9"/>
  </UserEngagement>
</template>

<script>
export default {
    name: "EduWhy",
    methods: {

    },
    computed: {},
    props: {},
    data() {
        return {};
    },
    components: {
    Header,
    Button,
    UserEngagement
}
};
</script>

<style scoped>

.header {
  padding: 2rem;
}

</style>