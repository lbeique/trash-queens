<template>
  <div class="recycleBinContainer">
    <template v-if="binType == 'organic'">
      <img src="../assets/recycling-bins/organic-bin.svg" alt="organic-bin" />
    </template>
    <template v-else-if="binType == 'glass'">
      <img src="../assets/recycling-bins/glass-bin.svg" alt="glass-bin" />
    </template>
    <template v-else-if="binType == 'metal'">
      <img src="../assets/recycling-bins/metal-bin.svg" alt="metal-bin" />
    </template>
    <template v-else-if="binType == 'paper'">
      <img src="../assets/recycling-bins/paper-bin.svg" alt="paper-bin" />
    </template>
    <template v-else-if="binType == 'eWaste'">
      <img src="../assets/recycling-bins/e-waste-bin.svg" alt="e-waste-bin" />
    </template>
    <template v-else-if="binType == 'plastic'">
      <img src="../assets/recycling-bins/plastic-bin.svg" alt="plastic-bin" />
    </template>
    <p>{{ binType.toUpperCase() }}</p>
  </div>
</template>

<script>
export default {
  name: "GameRecycleBin",
  components: {},
  methods: {},
  computed: {},
  props: ["binType"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.recycleBinContainer {
  display: flex;
  width: 6.25rem;
  height: 6.5rem;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.938rem;
  padding: 1rem;
  background-color: #fff5e9;
  transition: all .2s;
}

.recycleBinContainer:hover{
    transform: translateY(-.2rem);
    box-shadow: 0 .2rem 2px #cac2b8 ;
}

p {
  font-family: "Fuzzy Bubbles", cursive;
  font-size: 0.813rem;
  color: black;
  font-weight: bold;
}

img {
  width: 100%;
  height: 100%;
}

</style>
