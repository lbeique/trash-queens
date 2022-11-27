<!--Component Usage: -->
<!--  <Hint garbage-name="apple"  garbage-category="organics" />-->


<script>
export default {
  methods: {
    hintBoxClose() {
      let [hintBox] = document.getElementsByClassName("hintBox");
      hintBox.style.display = "none";
    },
  },

  computed: {
    hintBoxNote: function () {
      const [NoteObject] = this.listOfNotes
          .filter( listItem => listItem.category === this.garbageCategory )
      return NoteObject.hintNote
    },
  }
};

</script>


<template>
  <div class="hintParent">

    <div class="hintBox hintChild">
      <h3>{{hintBoxNote}}</h3>
      <div class="hintX hintChild" @click="hintBoxClose()">
        <h2>x</h2>
      </div>
    </div>
  </div>
</template>


<style scoped>
.hintParent {
  z-index:9;
  margin-top: 4rem;
  /*WHY??*/
}

.hintChild {
  position: absolute;
}

.hintBox{
  bottom: 0;
  left: 0;

  padding: 40px;
  height :250px;
  width: 330px;
  background-color: #F5F9E9;
  border-radius: 10px 10px 10px 28px;

  display: none;
  align-items: center;
  justify-content:center ;
}

.hintX {
  top: 0;
  right: 0;

  height :60px;
  width: 60px;
  display: flex;
  align-items: center;
  justify-content:center ;
  z-index: 20;
}

.hintButton{
  bottom: 0;
  left: 0;

  height :60px;
  width: 60px;
  background-color: #FFD45D;
  border-radius: 40px ;
  box-shadow: 0 1px 1px 1px rgba(0, 0, 0, 0.25);

  display: flex;
  align-items: center;
  justify-content:center ;
  z-index: 20;
}

.hintButton img{

  height: 75%;
  width: 75%;
  object-fit: contain
}

</style>


