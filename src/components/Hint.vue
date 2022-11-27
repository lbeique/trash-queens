<!--Component Usage: -->
<!--  <Hint garbage-name="apple"  garbage-category="organics" />-->


<script>
export default {
  props: {
    garbageName: String,
    garbageCategory:String
  },
  data() {
    return {
      listOfNotes: [
        {category:"organics", hintNote:"This is the purest form of recycling, because nature does 100% of the work for us! "},
        {category:"glass", hintNote:"We can take them and purpose them without any loss in quality."},
        {category:"metal", hintNote:"No pun intended, but some can be used to create new road signs and window frames"},
        {category:"paper", hintNote:"They can be recycled into a whole bunch of new things, including new boxes, paper towels!"},
        {category:"e-waste", hintNote:"They are a treasure trove of recyclable material!"},
        {category:"plastic", hintNote:"They can be recycled into ropes, packaging, chairs, brush bristles and even car bumpers!"},
      ],
    };
  },
  methods: {
    hintBoxClose() {
      let [hintBox] = document.getElementsByClassName("hintBox");
      hintBox.style.display = "none";
    },
    hintLampClicked(){
      let [hintBox] = document.getElementsByClassName("hintBox");
      hintBox.style.display === "none" || hintBox.style.display === ""
          ? hintBox.style.display = "flex"
          :hintBox.style.display = "none"
    }
  },
  // watch: {
  //   garbageName: function (newGarbageName, oldGarbageName) {
  //   },
  // },
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

    <div class="hintButton hintChild" @click="hintLampClicked()">
<!--      <h2>H</h2>-->
      <img src="../assets/idea.png" alt="H" >
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


