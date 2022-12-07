<script setup>
import Button from '../components/shared/Button.vue'
import { RouterLink, RouterView } from 'vue-router'
import Header from '../components/shared/Header.vue';
</script>

<template>
  <Header title="About" >

    <template class="aboutIntro__content" v-slot:Desc>
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
        <h3>Phoenix Lai</h3>
        <p>Full-stack web developer/ designer trying to create a better world, one less single use plastic at a time.</p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content ">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Yasmina Photo">
      <div>
        <h3>Yasmina Amirifar </h3>
        <p>Shes always wanted to be a web developer ever since she remember! Working part time in google.</p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Stefanie Photo">
      <div>
        <h3>Stefanie Taswin</h3>
        <p>An aspiring full-stack web developer. Obsessed with coffee, games, and an explorer.</p>
        <div class="card__link">
          <a href="#">social link </a>
          <a href="#">social link</a>
        </div>
      </div>
    </div>
    <div class="card__TM--content">
      <img src="https://picsum.photos/seed/picsum/91/91" alt="Laurent Photo">
      <div>
        <h3>Laurent Beique </h3>
        <p>One part web developer and three parts self-critic all wrapped up in a meat Popsicle.</p>
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
  margin:1rem 0 2rem 0;
  padding: 1rem;
  color:#F5F9E9;
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


.card__content {
  width: 100%;
  padding: 1rem ;
  gap: 1.5rem;
  /*display: flex;*/
  /*flex-direction: column;*/
  /*justify-content: space-between;*/
}

/*TM stand for Team Member*/
.card__TM--content {
  display:flex;
  gap:1.5rem;
  margin-top:24px;
  padding: 1rem;

}


.card p{
  font-size: 12px;
}

p{
  font-family: "Nunito-Regular", sans-serif;
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
  font-size: 18px ;
  margin-bottom:5px;
}

a{
  margin-right: 20px;
  color: #F7C932 ;
  font-family: "Nunito-Regular", sans-serif;
  font-size: 11px;
}

</style>
