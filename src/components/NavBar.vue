<script setup>
import NavBarItem from './NavBarItem.vue';
</script>

<template>
    <nav class="navbar">
        <NavBarItem navIcon='icon-park-twotone:home' navName='home' navTo='/' />
        <NavBarItem navIcon='icon-park-twotone:game-ps' navName='game' navTo='/game' />
        <NavBarItem navIcon='icon-park-twotone:book-open' navName='resources' navTo='/resources' />
    </nav>
</template>

<script>
export default {
    name: "NavBar",
    components: { 
        NavBarItem
    }
};
</script>

<style scoped>
.navbar {
    background-color: #5AB4AB;
    display: flex;
    justify-content: space-evenly;
    padding: 1rem 0;
}
</style>