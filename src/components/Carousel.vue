<script src="/path/to/vue.js"></script>
<script src="/path/to/vue-carousel.js"></script>

<template class="carousel">
  <body>
    <div class="carousel">
      <div class="carousel-container">
        <div class="carousel-img1">
          <img class="img-carousel" src="../assets/img/cpt.jpeg" />
        </div>
        <div class="carousel-img2">
          <img class="img-carousel" src="../assets/img/cpt2.jpeg" />
        </div>
        <div class="carousel-img3">
          <img class="img-carousel" src="../assets/img/cpt.jpeg" />
        </div>
      </div>
    </div>
  </body>
</template>

<script>
import Carousel from "./Carousel.vue";

export default {
  name: "Carousel",
  components: {
    Carousel
  }
};
</script>

<style>
.carousel {
  width: 100%;
  height: 900px;
  background: #ffffff;
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;
}

.carousel-container {
  /* display: inline-block; */
  width: 280%;
  display: flex;
  margin-top: 10px;
}

.img-carousel {
  width: 1200px;
  margin: 0;
  height: 700px;
  object-fit: cover;
}

.carousel-img1 {
  width: 1200px;
  height: 700px;
  background: black;
  margin: 2% 1% 2% 2.8%;
}

.carousel-img2 {
  width: 1200px;
  height: 700px;
  margin: 2% 1% 2% 1%;
  background: black;
}

.carousel-img3 {
  width: 1200px;
  height: 700px;
  background: black;
  margin: 2% 0% 2% 1%;
}
</style>
