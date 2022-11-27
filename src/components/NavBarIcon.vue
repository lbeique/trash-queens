<script setup>
import { Icon, addIcon, addCollection } from '@iconify/vue'
</script>

<template>
        <Icon icon={{ iconName }} />
</template>

<script>
export default {
    name: "NavBarIcon",
    props: {
        iconName: {
            type: String,
            required: true
        }
    },
    data() {
        return {};
    },
};
</script>

<style scoped>
    Icon {
        background-color: "#F5F9E9";
        margin-right: 10px;
    }
</style>