<template>
  <div class="detail-trip" ref="main">
    <div class="header-trip">
        <h1 class="header-title" ref="title">Norway</h1>
        <div class="card card-article">
            <img src="../assets/img/norway.png">
            <h2 class="title-card">Portor</h2>
            <h3 class="country-card">Norway</h3>
            <h3 class="date-card">April 2018</h3>
        </div>
    </div>
    <div class="top-article">
        <h1>Välkommen till sverige ! </h1>
        <p>It was a humorously perilous business for both of us. For, before we proceed further, it must be said that the monkey-rope was fast at both ends; fast to Queequeg's broad canvas belt, and fast to my narrow leather one. So that for better or for worse, we two, for the time, were wedded; and should poor Queequeg sink to rise no more, then both usage and honour demanded.</p>
        <vue-carousel></vue-carousel>
    </div>
    <div class="fav-places">
        <h1>Best places</h1>
        <ul>Drink and Eat
            <li class="first-list">Judith & Bertil<span>Bar</span></li>
            <li>Nada Bar<span>Restaurant</span></li>
            <li>Ugglan<span>Bar</span></li>
            <li>Judith & Bertil <span>Bar</span></li>
        </ul>
        <ul>Discover
            <li class="first-list">Judith & Bertil<span>Bar</span></li>
            <li>Nada Bar<span>Restaurant</span></li>
            <li>Ugglan<span>Bar</span></li>
            <li>Judith & Bertil <span>Bar</span></li>
        </ul>
        <ul>Drink and Eat
            <li class="first-list">Judith & Bertil<span>Bar</span></li>
            <li>Nada Bar<span>Restaurant</span></li>
            <li>Ugglan<span>Bar</span></li>
            <li>Judith & Bertil <span>Bar</span></li>
        </ul> 
    </div>
    </div>
</template>
<script>
import Card from "../components/Card.vue";
import VueCarousel from "../components/Carousel.vue";
import Vue from 'vue';
import { TimelineMax } from 'gsap'


export default {
  name: "Trip",
  components: {Card, VueCarousel}, 

methods: {
    mountAnimation: function(delay) {
      const timeline = new TimelineMax()
      timeline
        .from(this.$refs.title, .5, { y: '30px', opacity: 0, ease: Power1.easeOut }, delay + 0)
    }
  }
}

</script>

<style scoped>
.header-trip {
    width: 100%;
    height: 760px;
    margin-top: -90px;
    background: #9CABB4;
    float: left;
    margin-bottom: 10%;
}

.header-title
{
    position: absolute;
    left: -5%;
    top: 1%;
    font-size: 17em;
    color: white;
    z-index: 1;
}

.card-article {
    margin-top: 12%;
    position: absolute;
    margin-left: 35%;
}

h1 {
  font-size: 3.5rem;
  font-family: 'CanelaWeb-Regular';
  padding-left: 23%;
  padding-right: 30%;
  line-height: 1.3;
  font-weight: normal;
  color: rgb(16, 16, 16);
}

p {
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  color: rgb(16, 16, 16);
  font-size: 1.4rem;
  font-weight: 300;
  padding-left: 23%;
  padding-right: 23%;
  line-height: 1.8;
  margin-top: 3%;
  margin-bottom: 15%;
}

ul {
  display: inline-block;
  margin-top: 2%;
  margin-left: 5%;
  margin-right: 8%;
  margin-bottom: 28%;
  font-family: 'MaisonNeueBook', Helvetica, Arial, sans-serif;
  font-weight: bold;
  font-size: 1.2rem;
}

.first-list {
    margin-top: 30px;
}

li {
    margin: 15px 0;
    list-style:none;
    font-weight: normal;
}

li:hover {
    text-decoration: underline;
    cursor: pointer;
}

.fav-places {
    display: block;
    margin-top: 30%;
}


</style>