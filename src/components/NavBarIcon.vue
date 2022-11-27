// vue component that takes an svg path and renders it as an icon

<template>
    <div>
        <svg
        :width="size"
        :height="size"
        :viewBox="viewBox"
        :fill="fill"
        :stroke="stroke"
        :stroke-width="strokeWidth"
        :stroke-linecap="strokeLinecap"
        :stroke-linejoin="strokeLinejoin"
        :class="className"
        >
        <path :d="path" />
        </svg>
    </div>
</template>

<script>
export default {
    name: "NavBarIcon",
    props: {
        path: {
            type: String,
            required: true
        },
        size: {
            type: Number,
            default: 24
        },
        viewBox: {
            type: String,
            default: "0 0 24 24"
        },
        fill: {
            type: String,
            default: "none"
        },
        stroke: {
            type: String,
            default: "currentColor"
        },
        strokeWidth: {
            type: Number,
            default: 2
        },
        strokeLinecap: {
            type: String,
            default: "round"
        },
        strokeLinejoin: {
            type: String,
            default: "round"
        },
        className: {
            type: String,
            default: ""
        }
    }
};
</script>

<style scoped>
</style>