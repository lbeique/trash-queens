<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBarIcon from './NavBarIcon.vue';

</script>

<template>
    <div class="navbar">
        <NavBarIcon iconName={{ navIcon }} />
        <RouterLink to={{ navTo }} class="navbar-link">
            {{ navName }}
        </RouterLink>
    </div>
    
    <RouterView />
</template>

<script>
export default {
    name: "NavBar",
    props: {
        navName: {
            type: String,
            required: true
        },
        navTo: {
            type: String,
            required: true
        },
        navIcon: {
            type: String,
            required: true
        }
    },
    components: {
        NavBarIcon
    },
    data() {
        return {};
    },
};
</script>

<style scoped>
    .navbar {
        display: flex;
        justify-content: center;
        flex-direction: column;
    }
    .navbar-link {
        color: #F5F9E9;
        font-size: 0.75rem;
        font-family: "Nunito", sans-serif;
    }
</style>