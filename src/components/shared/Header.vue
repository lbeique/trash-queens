// vue component that is the header. it has a the goback button and a title

<script setup>
import GoBackVue from './GoBack.vue';
</script>

<template>
  <header>
    <GoBackVue :isGame="false" />
    <h1>{{ title }}</h1>
  </header>
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
    GoBackVue 
}
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>