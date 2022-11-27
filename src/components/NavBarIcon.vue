<script setup>
import { Icon } from '@iconify/vue'

</script>

<template>
    <div>
        <Icon class='icon' icon='icon-park-twotone:home' :color="colorObject" />
    </div>
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
    components: {
        Icon
    },
    computed: {
        colorObject() {
            return {
                color: '#F5F9E9'
            }
        }
    },
    data() {
        return {
            colorObject: {
                activeColor: 'F7C932',
                inactiveColor: '#F5F9E9'
            }
        };
    },
};
</script>

<style scoped>
    Icon {
        background-color: "#F5F9E9";
        margin-right: 10px;
    }
</style>