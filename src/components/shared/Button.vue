<template>
    <button class="game-button" :class="variant">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: "Button",
    methods: {},
    computed: {},
    props: {
        text: {
            type: String,
            required: true
        },
        variant: {
            type: String,
            default: "primary",
            required: true
        }
    },
    data() {
        return {};
    },
};
</script>

<style scoped>
.game-button {
    border: none;
    color: #F5F9E9;
    border-radius: 8px;
    cursor: pointer;
    display: inline-block;
    font-size: 1.5rem;
    font-weight: 400;
    margin: 0;
    padding: 1rem 3rem;
    text-align: center;
    transition: all 0.2s;
}

.primary {
    background-color: #273D4E;
}

.primary:hover {
    transform: translateY(-0.2rem);
    filter: drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.25));
    background-color: #5AB4AB;
}

.primary:active {
    transform: translateY(0.1rem);
    background-color: #8C8C8C;
    filter: none;
}

.alternate {
    background-color: #5AB4AB;
}

.alternate:hover {
    transform: translateY(-0.2rem);
    filter: drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.25));
    background-color: #273D4E;
}

.alternate:active {
    transform: translateY(0.1rem);
    background-color: #8C8C8C;
    filter: none;
}

.tutorial {
    background-color: #F7C932;
    color: #273D4E;
}

.tutorial:hover {
    transform: translateY(-0.2rem);
    filter: drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.25));
    background-color: #F5F9E9;
}

.tutorial:active {
    transform: translateY(0.1rem);
    background-color: #8C8C8C;
    filter: none;
}

</style>