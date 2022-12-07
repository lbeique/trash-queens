<template>
    <div class="tracker">
        <template v-for="(s, i) in totalPositions" :key="i">
            <div class="tracker__dot" :class="{'tracker__dot--active': trackerPosition == s}" />
        </template>
    </div>
</template>

<script>
export default {
    name: "Tracker",
    methods: {

    },
    computed: {},
    props: {
        trackerPosition: {
            type: Number,
            required: true
        },
        totalPositions: {
            type: Number,
            required: true
        }
    },
    data() {
        return {};
    }
};
</script>

<style scoped>
.tracker {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 0.25rem;
}

.tracker__dot {
    width: 0.5rem;
    height: 0.5rem;
    border-radius: 50%;
    background-color: #F5F9E9;
}

.tracker__dot--active {
    background-color: #F7C932;
}
</style>
