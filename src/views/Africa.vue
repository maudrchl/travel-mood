<template>
  <div class="detail-trip">
    <div class="header-trip">
      <h1 class="header-title">South Africa</h1>
      <div class="card card-article">
        <img src="../assets/img/cpt.jpeg" />
        <h2 class="title-card">Cape Town</h2>
        <h3 class="country-card">South Africa</h3>
        <h3 class="date-card">June - December 2019</h3>
      </div>
    </div>
    <div class="top-article">
      <h1>Sunny Cape Town 🌴</h1>
      <p>
        It was a humorously perilous business for both of us. For, before we
        proceed further, it must be said that the monkey-rope was fast at both
        ends; fast to Queequeg's broad canvas belt, and fast to my narrow
        leather one. So that for better or for worse, we two, for the time, were
        wedded; and should poor Queequeg sink to rise no more, then both usage
        and honour demanded.
      </p>
    </div>
    <vue-carousel></vue-carousel>
    <div class="fav-places">
      <h1>Best places</h1>
      <ul>
        Drink and Eat
        <li class="first-list">Judith & Bertil<span>Bar</span></li>
        <li>Nada Bar<span>Restaurant</span></li>
        <li>Ugglan<span>Bar</span></li>
        <li>Judith & Bertil <span>Bar</span></li>
      </ul>
      <ul>
        Discover
        <li class="first-list">Judith & Bertil<span>Bar</span></li>
        <li>Nada Bar<span>Restaurant</span></li>
        <li>Ugglan<span>Bar</span></li>
        <li>Judith & Bertil <span>Bar</span></li>
      </ul>
      <ul>
        Drink and Eat
        <li class="first-list">Judith & Bertil<span>Bar</span></li>
        <li>Nada Bar<span>Restaurant</span></li>
        <li>Ugglan<span>Bar</span></li>
        <li>Judith & Bertil <span>Bar</span></li>
      </ul>
    </div>
  </div>
</template>
<script>
// import Card from "../components/Card.vue";
import VueCarousel from "../components/Carousel.vue";

export default {
  name: "Trip",
  components: { VueCarousel }
};
</script>

<style scoped>
.header-trip {
  width: 100%;
  height: 760px;
  margin-top: -90px;
  background: #fec09b;
  float: left;
  margin-bottom: 15%;
}

.header-title {
  position: absolute;
  left: -6%;
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
  font-family: "CanelaWeb-Regular";
  padding-left: 8%;
  font-weight: normal;
}

p {
  font-family: "MaisonNeueBook", Helvetica, Arial, sans-serif;
  color: #9b9b9b;
  font-size: 1rem;
  padding-left: 8%;
  padding-right: 60%;
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
  font-family: "MaisonNeueBook", Helvetica, Arial, sans-serif;
  font-weight: bold;
  font-size: 1.2rem;
}

.first-list {
  margin-top: 30px;
}

li {
  margin: 15px 0;
  list-style: none;
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
