<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
</script>

<template>
  <Header title="About" >

    <template class="gameIntro__content" v-slot:Desc>
      <p>We hope that you enjoy exploring our project as much as we enjoyed making it!</p>
    </template>
  </Header>

  <div class=" card left--card">
    <div class="card__content">
      <h3> this is the title </h3>
      <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. Always hungry. Curl into a furry donut purr like an angel but being gorgeous with belly side up so destroy couch.</p>
    </div>
  </div>

  <div class=" card right--card">
    <div class="card__content">
      <h3> this is the title </h3>
      <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. Always hungry. Curl into a furry donut purr like an angel but being gorgeous with belly side up so destroy couch.</p>
    </div>
  </div>

  <div class=" card left--card team--card">
    <div class="card__TM--content ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Phoenix Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Yasmina Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Stefanie Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Laurent Photo">
      <div>
        <h3>Name </h3>
        <p>Chill on the couch table wack the mini furry mouse yet purr when give birth but be superior yet lasers are tiny mice. </p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
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

.header {
  padding: 2rem;
}

.card{
  align-items: center;
  position: relative;
  width: 390px;
  margin-top: 2rem;
  padding: 1rem;
  color: white;
  background-color: #5AB4AB;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.15));
}

.left--card{
  transform: translateX(-2.5rem);
  border-radius: 8px;
  padding-left: 50px;
}

.right--card{
  transform: translateX(2.5rem);
  border-radius:  8px;
  padding-right: 50px;
}

.team--card{
  margin-bottom: 2rem;
}

.card__content {
  width: 100%;
  padding: 2rem 1.5rem;
  gap: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

/*TM stand for Team Member*/
.card__TM--content {
  display:flex;
  gap:1.5rem;
  margin-top:24px;
}


img{
  width:91px;
  height:91px;
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

a{
  margin-right: 20px;
  color: #F7C932 ;
  font-family: "Nunito-Regular", sans-serif;
  font-size: 11px;
}

</style>
