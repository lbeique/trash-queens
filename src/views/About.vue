<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
</script>

<template>
  <!--  <Header title="About Us" />-->
  <!-- <RouterLink to="/GamePlay-Easy">
    <Button text="Easy Mode" variant="primary" @click="startGame" />
  </RouterLink>
  <RouterLink to="/GamePlay-Hard">
    <Button text="Hard Mode" variant="primary" @click="startGame" />
  </RouterLink> -->
  <Header title="About" >

    <template class="gameIntro__content" v-slot:Desc>
      <p>We hope that you enjoy exploring our project as much as we enjoyed making it!</p>
    </template>
  </Header>

  <div class=" card card__appLeft">
    <div class="card__content">
      <h3> this is the title </h3>
      <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. Always hungry. Curl into a furry donut purr like an angel but being gorgeous with belly side up so destroy couch.</p>
    </div>
  </div>

  <div class=" card card__appRight">
    <div class="card__content">
      <h3> this is the title </h3>
      <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. Always hungry. Curl into a furry donut purr like an angel but being gorgeous with belly side up so destroy couch.</p>
    </div>
  </div>

  <div class=" card card__team">

    <div class="card__teamContent ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Phoenix Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
        <div class="links__team">
          <a href="#">social link </a>
          <a href="#">social link</a>

        </div>
      </div>
    </div>
    <div class="card__teamContent ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Yasmina Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
      </div>
    </div>

    <div class="card__teamContent ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Stefanie Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
      </div>
    </div>

    <div class="card__teamContent">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Laurent Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "About",
  methods: {

  },
  computed: {},
  props: {},
  data() {
    return {};
  },
  components: {
    Header,
    Button
  }
};
</script>

<style scoped>
/*.page {*/
/*  display: flex;*/
/*  flex-direction: column;*/
/*  align-items: center;*/
/*  height: 100%;*/
/*  !*padding: 2rem;*!*/
/*  !*gap: 1rem;*!*/

/*  row-gap: 1rem;*/
/*  margin: 3rem 2rem;*/
/*}*/


.header {
  padding: 2rem;
}
.card{

  /*display: flex;*/
  /*flex-direction: column;*/

  align-items: center;
  /*justify-content: space-between;*/

  position: relative;
  /*width: 21.875rem;*/
  width: 390px;
  /*height: 10.125rem;*/
  margin-top: 2rem;

  /*display: flex;*/
  /*flex-direction: column;*/
  /*border-radius:  8px 0 0 8px;*/
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.15));
  /*width: 100%;*/
  padding: 1rem;
  /*gap: 1rem;*/
  /*max-width: 390px;*/
  color: white;
  background-color: #5AB4AB;
}

img{
  width:91px;
  height:91px;
}

/*.links__team{*/
/*  display:flex;*/
/*  justify-content: space-around;*/


/*}*/
a{
  margin-right: 20px;
  color: #F7C932 ;
  font-family: "Nunito-Regular", sans-serif;
  font-size: 11px;
}

.gameIntro__content {
  display: flex;
  flex-direction: column;
  align-content: center;
  row-gap: 1rem;
  margin: 3rem 2rem;
}

.card__content {
  width: 100%;
  padding: 2rem 1.5rem;
  gap: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  /*align-items: center;*/
}

.card__appLeft{
  /*align-self: flex-start;*/
  transform: translateX(-2.5rem);
  border-radius: 8px;
  padding-left: 50px;
}

.card__appRight{
  /*align-self: flex-end;*/
  transform: translateX(2.5rem);

  border-radius:  8px;
  padding-right: 50px;

}

.card__team{
  /*align-self: flex-start;*/
  transform: translateX(-2.5rem);

  border-radius:  0 8px 8px 0;
  padding-left: 50px;
  margin-bottom: 2rem;
}

.card__teamContent {
  display:flex;
  gap:1.5rem;
  margin-top:24px;

}
h2 {
  font-family: "FuzzyBubbles-Regular", sans-serif;
  color: #5ab4ab;
  font-size: 1.5rem;
}

h3{
  font-family: "FuzzyBubbles-Bold", sans-serif;
}

p{
  font-family: "Nunito-Regular", sans-serif;
  font-size: 12px;
}


</style>
