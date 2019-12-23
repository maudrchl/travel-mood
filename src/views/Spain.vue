<template>
  <div class="detail-trip">
    <div class="header-trip">
        <h1 class="header-title parallax-item">Barcelona</h1>
        <div class="card card-article parallax-item">
            <img src="../assets/img/cpt2.jpg">
            <h2 class="title-card">Barcelona</h2>
            <h3 class="country-card">Spain</h3>
            <h3 class="date-card">June 2019</h3>
        </div>
    </div>
      <div class="top-article">
        <p>
          It was a humorously perilous business for both of us. For, before we
          proceed further, it must be said that the monkey-rope was fast at both
          ends; fast to Queequeg's broad canvas belt, and fast to my narrow
          leather one. So that for better or for worse, we two, for the time, were
          wedded; and should poor Queequeg sink to rise no more, then both usage
          and honour demanded.
        </p>
      </div>
      <div class="full-width-img">
        <img class="full-width-img" src="../assets/img/cptfull.jpeg">
      </div>
      <h1>Hola, que tal?</h1>
       <p>
          It was a humorously perilous business for both of us. For, before we
          proceed further, it must be said that the monkey-rope was fast at both
          ends; fast to Queequeg's broad canvas belt, and fast to my narrow
          leather one. So that for better or for worse, we two, for the time, were
          wedded; and should poor Queequeg sink to rise no more, then both usage
          and honour demanded.
        </p>
    </div>
  </div>
</template>
<script>
// import Card from "../components/Card.vue";
import VueCarousel from "../components/Carousel.vue";

export default {
  name: "Trip",

  mounted: function(){
    window.addEventListener('scroll', () => {
      let parent = document.querySelector('.detail-trip');
      let children = parent.querySelectorAll('.parallax-item');
      for(let i = 0; i < children.length; i++) {
        children[i].style.transform = 'translateY(-' + (window.pageYOffset * i / children.length) + 'px)';
      }
    }, false)
  }
  
};
</script>

<style scoped>
.header-trip {
  width: 100%;
  height: 760px;
}

.header-title
{
    position: absolute;
    top: 50%;
    text-align:center;
    font-size: 10em;
    color: white;
    z-index: 1;
    opacity:0;
}

.card-article {
  margin-top: 12%;
  position: absolute;
  margin-left: 35%;
  opacity : 1;
}

h1 {
  font-size: 3.5rem;
  font-family: 'CanelaWeb-Regular';
  padding-left: 23%;
  line-height: 1.3;
  font-weight: normal;
  color: #F9F2F7;
  margin: 15% 0 -6% 0;
}

p {
  font-family: 'CircularStd-Book', Helvetica, Arial, sans-serif;
  color: #F9F2F7;
  font-size: 1.4rem;
  font-weight: 300;
  padding-left: 23%;
  padding-right: 23%;
  line-height: 1.8;
  margin-top: 10%;
  margin-bottom: 15%;
  font-weight: 100;
  opacity: 0.6;
}

.full-width-img {
  width: 100%;
  height: 700px;
  margin: 0;
}


</style>
