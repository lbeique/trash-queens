<script setup>
import NavBar from './components/NavBar.vue';
</script>

<template>
  <main>
    <RouterView />
  </main>
  <footer>
    <NavBar />
  </footer>
</template>

<style scoped>
@font-face {
  font-family: "Nunito-Regular";
  src: local("Nunito"),
    url('../src/assets/fonts/Nunito-Regular.ttf') format("truetype");
}

@font-face {
  font-family: "Nunito-Bold";
  src: local("Nunito"),
    url('../src/assets/fonts/Nunito-Bold.ttf') format("truetype");
}

@font-face {
  font-family: "FuzzyBubbles-Regular";
  src: local("FuzzyBubbles"),
    url('../src/assets/fonts/FuzzyBubbles-Bold.ttf') format("truetype");
}

@font-face {
  font-family: "FuzzyBubbles-Bold";
  src: local("FuzzyBubbles"),
    url('../src/assets/fonts/FuzzyBubbles-Bold.ttf') format("truetype");
}

main {
  height: 100vh;
}

footer {
  position: sticky;
  margin-top: 12rem;
  bottom: 0;
}
</style>
