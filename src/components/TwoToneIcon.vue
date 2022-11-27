<script setup>
import { Icon } from '@iconify/vue'

</script>

<template>
        <Icon :icon='iconName' :color="iconColor" :height="iconHeight" :width="iconWidth"/>
</template>

<script>
export default {
    name: "NavBarIcon",
    props: {
        iconName: {
            type: String,
            required: true
        },
        iconColor: {
            type: String,
            required: true
        },
        iconHeight: {
            type: Number,
            required: true
        },
        iconWidth: {
            type: Number,
            required: true
        }
    },
    components: {
        Icon
    },
    computed: {},
    data() {
        return {};
    },
};
</script>

<style scoped>
</style>