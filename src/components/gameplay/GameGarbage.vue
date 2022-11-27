<template>
    <div class="garbage__container">
        <img :src="garbageUrl" draggable="true">
        <span class="garbage__name">{{ selectedGarbage.garbageName }}</span>
    </div>
</template>

<script>
export default {
    name: "GameGarbage",
    methods: {
        getRandomGarbage() {
            this.selectedGarbage = this.garbages[Math.floor(Math.random() * this.garbages.length)]
            this.garbageUrl = new URL(`../../assets/garbages/trash-${this.selectedGarbage.garbageName}.svg`, import.meta.url).href
            this.setCurrentGarbage(this.selectedGarbage)
        }
    },
    computed: {

    },
    props: {
        setCurrentGarbage: Function
    },
    beforeMount() {
        this.getRandomGarbage()
    },
    data() {
        return {
            selectedGarbage: {},
            garbageUrl: '',
            garbages: [
                {
                    garbageName: 'apple',
                    garbageCategory: 'organics'
                },
                {
                    garbageName: 'apple-bitten',
                    garbageCategory: 'organics'
                },
                {
                    garbageName: 'avocado',
                    garbageCategory: 'organics'
                },
                {
                    garbageName: 'pizza',
                    garbageCategory: 'organicx'
                },
                {
                    garbageName: 'broken-glass',
                    garbageCategory: 'glass'
                },
                {
                    garbageName: 'broken-bottle',
                    garbageCategory: 'glass'
                },
                {
                    garbageName: 'glass',
                    garbageCategory: 'glass'
                },
                {
                    garbageName: 'can',
                    garbageCategory: 'metal'
                },
                {
                    garbageName: 'fork',
                    garbageCategory: 'metal'
                },
                {
                    garbageName: 'frying-pan',
                    garbageCategory: 'metal'
                },
                {
                    garbageName: 'cardbox',
                    garbageCategory: 'paper'
                },
                {
                    garbageName: 'airplane',
                    garbageCategory: 'paper'
                },
                {
                    garbageName: 'newspaper',
                    garbageCategory: 'paper'
                },
                {
                    garbageName: 'mouse',
                    garbageCategory: 'e-waste'
                },
                {
                    garbageName: 'hairdryer',
                    garbageCategory: 'e-waste'
                },
                {
                    garbageName: 'computer',
                    garbageCategory: 'e-waste'
                },
                {
                    garbageName: 'plastic-bag',
                    garbageCategory: 'plastic'
                },
                {
                    garbageName: 'plastic-bottle',
                    garbageCategory: 'plastic'
                },
                {
                    garbageName: 'plastic-cup',
                    garbageCategory: 'plastic'
                },
            ]
        };
    }
}
</script>

<style scoped>
.garbage__container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    /* width: 9.063rem; */
    height: 3.979rem;
}

img {
    width: 100%;
    height: 100%;
    margin-bottom: 1rem;
    z-index: 10;
    filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}

span {
    display: flex;
    align-items: center;
    border-radius: 0.625rem;
    background-color: #fff5e9;
    color: black;
    padding: 1rem;
    height: 1.223rem;
    font-family: "FuzzyBubbles-Regular", sans-serif;
    font-size: 1.063rem;
    font-weight: bold;
}
</style>