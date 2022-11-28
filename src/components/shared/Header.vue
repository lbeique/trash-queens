<script setup>
import GoBackVue from './GoBack.vue';
</script>

<template>
  <header>
    <GoBackVue :isGame="false" />
    <div header__container>
        <h1>{{ title }}</h1>
        <slot name="Button"></slot>
    </div>
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
  flex-direction: column;
  align-items: flex-start;
}

.header__container {
    display: flex;
}
</style>