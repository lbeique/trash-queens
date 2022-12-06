<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
import UserEngagement from '../components/education/UserEngagement.vue';
import Scroll from '../components/shared/Scroll.vue';
</script>

<template>
  <Header title="How to Recycle?" />
  <UserEngagement>
    <Scroll scrollColor="#F5F9E9" fontColor="#F5F9E9"/>
  </UserEngagement>
</template>

<script>
export default {
    name: "EduHow",
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
.header {
  padding: 2rem;
}

</style>