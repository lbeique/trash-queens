<template>
    <div>
        <img draggable="false" class="trashMountain__svg" :style="{'transform': `translateY(${translateRem}rem)`}" src="../../assets/garbages/trash-mountain.svg" alt="trash-mountain" />
        <!-- <button @click=" translateRem = translateRem - 2">move up </button> -->
    </div>
</template>

<script>
export default{
    name: 'GameTrashMountain',
    components: {},
    methods: {
        moveMountainY(){
            console.log('move up')
            this.translateRem = this.translateRem - 2
        }
    },
    computed: {},
    props: {},
    data(){
        return {
            translateRem: 0
        }
    }
}

</script>

<style scoped>

.trashMountain__svg{
    /* width: 24.375rem; */
    width: 100%;
    height: 16.5rem;
    transition: all .2s;
    z-index: -20;
   
}

</style>