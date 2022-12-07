// vue carousel component that imports the CarouselCard
<script setup>
    import CarouselCard from './CarouselCard.vue';
</script>

<template>
    <div class="carousel">
        <CarouselCard
            v-for="(card, index) in cards"
            :key="index"
            :text="card.text"
            :color="card.color"
            :trashSource="card.trashSource"
            :binSource="card.binSource"
            :content="card.content"
            :bin="card.bin"
            :backClick="backClick"
            :forwardClick="forwardClick"
        />
    </div>
</template>

<script>
    export default {
        name: "Carousel",
        methods: {
            backClick() {
                this.$emit('backClick');
            },
            forwardClick() {
                this.$emit('forwardClick');
            }
        },
        computed: {},
        props: {},
        data() {
            return {
                cards: [
                    {
                        title: "Organics",
                        text: "Organics are food waste products or any material that is biodegradable. This is the purest form of recycling, because nature does 100% of the work for us!",
                        trashSource: [require('@/assets/garbages/trash-apple-bitten.svg'), require('@/assets/garbages/trash-pizza.svg'), require('@/assets/garbages/trash-avocado.svg')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "blue",
                        bin: "Trash"
                    },
                    {
                        title: "Glass",
                        text: "Glass is infinitely recyclable! We can take bottles, and other common household items, and purpose them without any loss in quality.",
                        trashSource: [require('@/assets/images/trash.png'), require('@/assets/images/trash.png'), require('@/assets/images/trash.png')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "yellow",
                        bin: "Trash"
                    },
                    {
                        title: "Metal",
                        text: "Metal rocks! No pun intended, but recycling aluminum containers can be used to create new road signs and window frames, that’s super cool!",
                        trashSource: [require('@/assets/images/trash.png'), require('@/assets/images/trash.png'), require('@/assets/images/trash.png')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "red",
                        bin: "Trash"
                    },
                    {
                        title: "Paper",
                        text: "Paper packaging can be recycled into a whole bunch of new things, including new boxes, paper towels, tissues, plant pot, Kraft paper and even drywall liner!",
                        trashSource: [require('@/assets/images/trash.png'), require('@/assets/images/trash.png'), require('@/assets/images/trash.png')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "blue",
                        bin: "Trash"
                    },
                    {
                        title: "E-Waste",
                        text: "Did you know our everyday electronics contain plastics, glass, gold, silver, copper and aluminum? E-wastes are a treasure trove of recyclable material!",
                        trashSource: [require('@/assets/images/trash.png'), require('@/assets/images/trash.png'), require('@/assets/images/trash.png')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "yellow",
                        bin: "Trash"
                    },
                    {
                        title: "Plastic",
                        text: "It’s not only plastic containers, but most flexible plastics can be recycled too! Plastic can be recycled into ropes, packaging, chairs, brush bristles and even car bumpers!",
                        trashSource: [require('@/assets/images/trash.png'), require('@/assets/images/trash.png'), require('@/assets/images/trash.png')],
                        binSource: require('@/assets/images/bin.png'),
                        color: "red",
                        bin: "Trash"
                    }
                ]
            };
        },
        components: {
            CarouselCard
        }
    };
</script>

<style scoped>
    .carousel {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100%;
    }
</style>