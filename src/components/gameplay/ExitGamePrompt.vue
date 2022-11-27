<template>
  <div class="promptBox" >
      <span>
        <h3>Are you sure you want to quite this awesome game?</h3>
        <div class="promptButtons">
          <button class="stayBtn" @click="stayInGame">Keep Playing</button>
          <button class="leaveBtn" @click="$router.go(-1)">Leave</button>
        </div>
      </span>
  </div>
</template>

<script>

export default {
  name: "ExitGamePrompt",
  methods:{
    stayInGame() {
      this.$emit('stayInGame');
    },
  },
  computed: {},
  props:{
    openPrompt: String,
  }
  ,
  data() {
    return {};
  },
};

</script>


<style scoped>
.promptBox{

  z-index:20;

  padding: 50px 35px 35px 35px ;
  height :250px;
  width: 320px;
  background-color: #F5F9E9;
  border-radius: 10px;

  display: flex;
  align-items: center;
  justify-content:center ;
}

.promptButtons{
  margin:1rem 0;
  display:flex;
  /*justify-content: space-around;*/
  justify-content: center;
}

.promptButtons button{
  width:108px;
  height:32px;
  margin:5px;
  border-radius: 8px;
  color:#F5F9E9;
  border:0;
}

.leaveBtn{
  background-color: #5AB4AB;
}


.stayBtn{
  background-color: #273D4E;

}

</style>


