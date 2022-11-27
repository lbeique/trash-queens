<script setup>
import NavBar from './components/NavBar.vue';
import NavBarItem from './components/NavBarItem.vue';
import NavBarIcon from './components/NavBarIcon.vue';
</script>

<template>
  <footer>
        <!-- <NavBar /> -->
        <!-- <NavBarItem /> -->
        <NavBarIcon iconName="apples"/>
    </footer>
</template>

<style scoped>
@font-face {
  font-family: "Nunito";
  src: local("Nunito"),
   url('https://fonts.googleapis.com/css2?family=Nunito&display=swap') format("truetype");
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
