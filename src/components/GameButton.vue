<template>
    <button class="game-button" >
        {{ text }}
    </button>
</template>

<script>
export default {
    name: "GameButton",
    methods: {},
    computed: {},
    props: {
        text: {
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
.game-button {
    background-color: #273D4E;
    border: none;
    border-radius: 8px;
    color: #F5F9E9;
    cursor: pointer;
    display: inline-block;
    font-size: 1.5rem;
    font-weight: 400;
    margin: 0;
    padding: 1rem 3rem;
    text-align: center;
    filter: drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.25));
}

.game-button:hover {
    background-color: #5AB4AB;
}

.game-button:active {
    background-color: #8C8C8C;
}

.game-button:disabled {
    background-color: #8C8C8C;
    cursor: not-allowed;
}
</style>