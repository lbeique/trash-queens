<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
import UserEngagement from '../components/education/UserEngagement.vue';
import Scroll from '../components/shared/Scroll.vue';
import Carousel from '../components/education/Carousel.vue';
</script>

<template>
  <Header title="How to Recycle?" />
  <Carousel @forwardClick="nextCard" @backClick="backCard" />
  <UserEngagement>
    <Scroll scrollColor="#F5F9E9" fontColor="#F5F9E9"/>
  </UserEngagement>
</template>

<script>
export default {
    name: "EduHow",
    methods: {
      nextCard() {
        this.$refs.carousel.nextCard();
      },
      backCard() {
        this.$refs.carousel.backCard();
      }
    },
    computed: {

      
    },
    props: {


    },
    data() {
        return {
          

        };
    },
    components: { 
      Header,
      UserEngagement,
      Scroll,
      Carousel 
    }
};
</script>

<style scoped>
.header {
  padding: 2rem;
}

</style>