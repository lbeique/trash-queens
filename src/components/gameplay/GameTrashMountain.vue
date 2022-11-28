<template>
    <div>
        <img draggable="false" class="trashMountain__svg" :style="{ 'transform': `translateY(${translateRem}rem)` }"
            src="../../assets/garbages/trash-mountain.svg" alt="trash-mountain" />
        <!-- <button @click="moveMountainY()">move up </button> -->
    </div>
</template>

<script>
export default {
    name: 'GameTrashMountain',
    components: {},
    methods: {
        moveMountainY() {
            console.log('move up')
            if (this.counter < 9) {
                this.counter++
                this.translateRem = this.translateRem - 1.4
                this.$emit("wrongItems", this.counter)
                this.setWrongNums(this.counter)
            } else {

            }
        }
    },
    computed: {},
    props: {
        setWrongNums: Function
    },
    data() {
        return {
            translateRem: 0,
            counter: 0
        }
    }
}

</script>

<style scoped>
.trashMountain__svg {
    /* width: 24.375rem; */
    width: 100%;
    height: 16.5rem;
    transition: all .2s;
    /* z-index: -10; */

}
</style>